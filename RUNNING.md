# Running the engine

This repo is a fork of [zshah101/Automated-List-Of-Summer-2027-and-Fall-2026-Tech-Internships](https://github.com/zshah101/Automated-List-Of-Summer-2027-and-Fall-2026-Tech-Internships), retargeted from the United States to **Singapore & Southeast Asia** (`data/config.json` → `"regions": ["SEA"]`).

There are two ways to run it:

- **[Part A — Locally](#part-a--run-it-locally)**: a one-off run on your machine. Good for checking the retarget, testing filter changes, or regenerating the README and dashboard.
- **[Part B — On GitHub Actions](#part-b--let-github-actions-refresh-it-for-you)**: the way the upstream repo runs. A scheduled workflow refreshes the list every 30 minutes and commits the result back to the repo. This is what you want for a list that keeps itself current.

---

## Part A — Run it locally

### 1. Prerequisites

**Python 3.11 or newer.** The code uses `datetime.UTC`, which was added in 3.11 — Python 3.10 and older fail on import with `ImportError: cannot import name 'UTC'`. CI pins 3.11; 3.12 works too.

```bash
python --version
```

On Windows with several Pythons installed, use the launcher to pick one:

```bash
py -3.12 --version
```

### 2. Clone and enter the repo

```bash
git clone https://github.com/CrunchyBiscuit19/Automated-List-Of-Summer-2027-and-Fall-2026-Tech-Internships.git
```

```bash
cd Automated-List-Of-Summer-2027-and-Fall-2026-Tech-Internships
```

### 3. Create a virtual environment and install dependencies

```bash
python -m venv .venv
```

Activate it — **Windows (PowerShell)**:

```bash
.\.venv\Scripts\Activate.ps1
```

**macOS / Linux**:

```bash
source .venv/bin/activate
```

Then install:

```bash
pip install -r requirements.txt
```

To run the tests and linter as well, install the dev set instead (it includes `requirements.txt`):

```bash
pip install -r requirements-dev.txt
```

### 4. Check the region config

Everything about the region is decided by one file. Open [`data/config.json`](data/config.json) and confirm:

```json
{
  "cycles": ["Summer 2027", "Fall 2026"],
  "regions": ["SEA"],
  "role_scope": "tech"
}
```

`"SEA"` is a group token that expands to Singapore, Malaysia, Indonesia, Thailand, Vietnam and the Philippines. You can also list countries individually (`["singapore", "malaysia"]`), or switch back to the US with `["us"]`. Unknown values are a fatal config error rather than a silent no-op, so a typo fails loudly.

You can confirm what the engine resolved without doing a full run:

```bash
python -c "import sys; sys.path.insert(0,'src'); from intern_engine import config; c=config.load_config(); print(config.wanted_regions(c), '|', config.region_label(c))"
```

Expected output:

```
['sea'] | Singapore & Southeast Asia
```

### 5. Run the update

```bash
python run.py update
```

This is the main command. It polls every job board in `data/companies.json` (~4,650 endpoints across 12 ATS platforms), keeps the tech internships in the configured region and cycles, enriches them, writes them to the store, and regenerates every published artifact.

**Expect roughly 20–40 minutes** on a home connection — it is thousands of HTTP requests. Progress prints as `Fetched boards: N/4651`. A summary of counts prints at the end.

The other commands:

| Command | What it does |
|---|---|
| `python run.py update` | Fetch → filter → enrich → store → rebuild all artifacts. **The main one.** |
| `python run.py render` | Rebuild README/CSV/API/dashboard from the existing store. No network, takes seconds. |
| `python run.py discover` | Mine public datasets for new company/ATS tokens; grows `data/companies.json`. |
| `python run.py harvest` | Probe the curated candidates in `data/candidates.json` and detect which ATS each lives on. |
| `python run.py notify` | Send Discord/Telegram/email alerts for what was published. Run **only after** the data is pushed live. |
| `python run.py all` | `discover` + `harvest` + `update`. |

> **On `notify`:** an alert promises a role is on the list, so it must not run before the data is published. That is why the workflow runs it as a separate later step, and why you should not run it locally unless you have already pushed.

### 6. Look at the output

The run rewrites these:

| File | What it is |
|---|---|
| `README.md` | The rendered list — the page people read |
| `docs/index.html` | The live dashboard (search, filters, saved roles) |
| `data/jobs.json` | The store — every requisition the engine knows about |
| `data/internships.csv`, `docs/internships.csv` | CSV export |
| `docs/feed.xml` | RSS/Atom feed |
| `docs/api/jobs.json`, `docs/api/stats.json` | JSON API |
| `data/stats.json` | Run metrics (`fetched_at`, `rendered_at`, counts) |

Open `README.md` and check the **Scope** table reads `Region: Singapore & Southeast Asia`, then look at the locations in the listing table.

To count what actually landed, by location:

```bash
python -c "import json,collections; d=json.load(open('data/jobs.json',encoding='utf-8')); c=collections.Counter(v.get('location','?') for v in d.values() if v.get('is_open')); [print(f'{n:4}  {k}') for k,n in c.most_common(20)]"
```

Or open `docs/index.html` in a browser to preview the dashboard.

### 7. Run the checks

```bash
python -m pytest -q
```

One test fails on `main` today and is **not** caused by the retarget: `tests/test_publish.py::test_feed_never_folds_a_closed_requisition_into_a_live_one`. It fails identically on the commit before the retarget, so treat `584 passed, 1 failed` as the current baseline.

```bash
python tools/verify_accuracy.py
```

`verify_accuracy.py` is the gate between "we produced output" and "the world sees it". It checks every open role against the accuracy invariants and the run as a whole (volume floor, fetch collapse). Two optional env vars tune it:

- `MIN_OPEN_ROLES` — fail if fewer open roles than this (the workflow uses `70`; **that floor is far too high for a SEA list and must be lowered** — see Part B step 5)
- `MAX_STATS_AGE_HOURS` — fail if the stats are older than this (default 12)

Lint, if you are changing code:

```bash
ruff check src tests tools run.py
```

---

## Part B — Let GitHub Actions refresh it for you

This is how the upstream repo keeps its list current: no server, no cron on your laptop. GitHub runs the engine on a schedule, and the runner **commits the refreshed README and data straight back to `main`**. GitHub Pages then serves `docs/` as the live dashboard.

### The workflows already in this repo

| Workflow | Schedule | What it does |
|---|---|---|
| [`update.yml`](.github/workflows/update.yml) | `7,37 * * * *` — every 30 min | The main loop: run the engine, verify, commit, wait for Pages, send alerts |
| [`discover.yml`](.github/workflows/discover.yml) | `47 8 * * *` — daily | Mine new companies, grow `data/companies.json` |
| [`audit.yml`](.github/workflows/audit.yml) | `17 9 * * 4` — Thursdays | Re-check date-inferred cycles against the posting text |
| [`retry.yml`](.github/workflows/retry.yml) | on workflow failure | Re-runs a job GitHub never gave a runner |
| [`ci.yml`](.github/workflows/ci.yml) | on push / PR | Lint + tests + artifact verification |

They are cron-scheduled at odd minutes on purpose. GitHub queues scheduled workflows globally and drops runs at busy times; minutes 7 and 37 get dropped far less often than 0 and 30.

### 1. Enable Actions on the fork

Forked repos have scheduled workflows **disabled by default** — this is the step people miss.

1. Go to the **Actions** tab of your fork.
2. Click **"I understand my workflows, go ahead and enable them"**.

Scheduled workflows on a fork also stop firing after 60 days of repository inactivity. Any push resets that clock.

### 2. Give the workflow permission to push

The engine commits its own output, so the token needs write access.

1. **Settings → Actions → General**
2. Under **Workflow permissions**, select **Read and write permissions**
3. **Save**

(The workflows already declare `permissions: contents: write`, but the repo-level setting caps what that can grant.)

### 3. Turn on GitHub Pages

1. **Settings → Pages**
2. **Source**: *Deploy from a branch*
3. **Branch**: `main`, folder **`/docs`**
4. **Save**

Your dashboard will be at `https://crunchybiscuit19.github.io/Automated-List-Of-Summer-2027-and-Fall-2026-Tech-Internships/`. The engine works this URL out from the git remote (`config.repo_slug()`), so every link it renders points at your fork automatically — no find-and-replace needed.

This matters beyond hosting: `update.yml` will not send alerts until it has fetched `api/stats.json` from the live Pages URL and seen this run's exact `rendered_at`. With Pages off, the publish step still commits, but alerts stay queued.

### 4. Merge the retarget onto `main`

The scheduled workflows all check out `main`. The SEA retarget currently lives on the `retarget-singapore-sea` branch, so until it is on `main` the bot will keep publishing a US list.

```bash
git checkout main
```

```bash
git merge retarget-singapore-sea
```

```bash
git push origin main
```

### 5. Lower the accuracy floor for a SEA-sized list

**Do this before the first scheduled run.** [`update.yml`](.github/workflows/update.yml) sets `MIN_OPEN_ROLES: "70"` and [`audit.yml`](.github/workflows/audit.yml) sets `"60"`. Those floors were calibrated against a US list of ~500 open roles. A Singapore/SEA list is much smaller, so the gate will fail the run and nothing will ever publish.

Run the engine once (Part A), see what the real open-role count is, and set the floor safely below it — the point of the floor is to catch a *collapse*, not to assert a target.

```yaml
      - name: Verify accuracy before publishing
        env:
          MIN_OPEN_ROLES: "10"     # was 70 — calibrated for the US list
          MAX_STATS_AGE_HOURS: "2"
        run: python tools/verify_accuracy.py
```

### 6. Trigger a run by hand

Every workflow has `workflow_dispatch`, so you do not have to wait for the schedule.

1. **Actions** tab → **Update internships** in the left sidebar
2. **Run workflow** → branch `main` → **Run workflow**

Watch the run. The steps that matter:

- **Run the engine** — the actual fetch
- **Verify accuracy before publishing** — the gate; if this fails nothing publishes and the previous good build stays live
- **Commit & push if changed** — where the refreshed README lands on `main`
- **Wait for Pages to serve this build** — polls the live URL for this run's `rendered_at`; a timeout here is a warning, not a failure (alerts stay queued for the next run)
- **Send alerts for what was published** — no-ops silently if you have set no alert secrets

Once it goes green, your fork's README is the refreshed SEA list and the dashboard is live.

### 7. (Optional) Alert channels and the Postgres mirror

All of these are optional and unset-safe: with no secret set the engine skips that channel and the run still succeeds. Add them under **Settings → Secrets and variables → Actions → New repository secret**.

| Secret | Enables |
|---|---|
| `DISCORD_WEBHOOK_URL` | Posts each run's new roles to a Discord channel |
| `TELEGRAM_BOT_TOKEN` + `TELEGRAM_CHAT_ID` | Phone push per drop (make a bot with @BotFather) |
| `BREVO_API_KEY` + `MAIL_FROM` | The daily email digest to the subscriber list |
| `SUPABASE_URL` + `SUPABASE_SERVICE_KEY` | Mirrors each run into Postgres; also backs the email subscriber list |
| `WORKDAY_PROXY` | Lets the runner reach Workday tenants that block datacenter IPs |

Note that `data/config.json` also carries a `supabase_url` and a **publishable** key — those are the public, browser-side ones the dashboard's subscribe form uses. They are not secrets, and not the same thing as `SUPABASE_SERVICE_KEY`. If you are running your own fork seriously, point them at your own Supabase project.

### 8. Tuning the cadence

Every 30 minutes is peak-season cadence and burns Actions minutes. To slow it down, edit the cron in [`update.yml`](.github/workflows/update.yml):

```yaml
on:
  schedule:
    - cron: "7 */4 * * *"   # every 4 hours instead of every 30 minutes
```

Keep the odd minute. Public repos get unlimited Actions minutes, so this only matters if your fork is private.

---

## Troubleshooting

**`ImportError: cannot import name 'UTC' from 'datetime'`** — you are on Python 3.10 or older. Use 3.11+.

**`No data/companies.json yet — run 'python run.py harvest' first.`** — the file is committed to the repo, so this means you are running from outside the repo root or the file was deleted. `git checkout data/companies.json`.

**The run finishes but the README still says `Region: United States`** — you are on `main` without the retarget merged, or `data/config.json` still says `"regions": ["us"]`.

**Actions never fires on schedule** — Actions not enabled on the fork (Part B step 1), or the repo has been inactive for 60 days. Push anything to reset it.

**The workflow fails at "Verify accuracy before publishing"** — most likely `MIN_OPEN_ROLES` is above your real SEA open-role count. See Part B step 5. This gate failing is the system working: the previous good build stays live rather than being replaced by a bad one.

**`main changed after generation; refusing to rebase stale artifacts`** — two writers raced. The workflows share a `concurrency` group to prevent this; it usually means someone pushed to `main` by hand mid-run. Harmless — the next scheduled run regenerates from fresh data.

**Alerts never arrive** — check the "Wait for Pages to serve this build" step. Nothing is announced until the data is provably live on Pages. Queued alerts are durable (`data/outbox.json`) and go out on a later run.
