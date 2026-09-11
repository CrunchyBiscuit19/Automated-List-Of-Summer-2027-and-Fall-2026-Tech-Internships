<div align="center">

# 🎓 Summer 2027 Tech Internships — Singapore & Southeast Asia

**A self-updating engine that tracks tech internships so you don't have to.**

[![CI](https://img.shields.io/github/actions/workflow/status/CrunchyBiscuit19/Automated-List-Of-Summer-2027-and-Fall-2026-Tech-Internships/ci.yml?branch=main&label=tests&style=flat-square&color=3fb950)](https://github.com/CrunchyBiscuit19/Automated-List-Of-Summer-2027-and-Fall-2026-Tech-Internships/actions/workflows/ci.yml)&nbsp;[![Open roles](https://img.shields.io/badge/dynamic/json?label=open%20roles&query=open_total&url=https%3A%2F%2Fcrunchybiscuit19.github.io%2FAutomated-List-Of-Summer-2027-and-Fall-2026-Tech-Internships%2Fapi%2Fstats.json&color=2f81f7&style=flat-square)](https://crunchybiscuit19.github.io/Automated-List-Of-Summer-2027-and-Fall-2026-Tech-Internships/)&nbsp;![Updates](https://img.shields.io/badge/updates-every%2030%20min-3fb950?style=flat-square)&nbsp;[![RSS](https://img.shields.io/badge/RSS-subscribe-e67e22?style=flat-square)](https://crunchybiscuit19.github.io/Automated-List-Of-Summer-2027-and-Fall-2026-Tech-Internships/feed.xml)

### 98 open roles (73 listed below) · 96 new this week

4,401 employers tracked · data as of Sep 11, 2026 at 04:48 UTC

_21 have a cycle the employer stated · 77 are recent postings whose cycle isn't stated (listed separately, never mixed in)._

**[🖥️ Live dashboard](https://crunchybiscuit19.github.io/Automated-List-Of-Summer-2027-and-Fall-2026-Tech-Internships/)** · **[📡 RSS](https://crunchybiscuit19.github.io/Automated-List-Of-Summer-2027-and-Fall-2026-Tech-Internships/feed.xml)** · **[⚙️ JSON API](https://crunchybiscuit19.github.io/Automated-List-Of-Summer-2027-and-Fall-2026-Tech-Internships/api/jobs.json)** · **[✉️ Email alerts](https://crunchybiscuit19.github.io/Automated-List-Of-Summer-2027-and-Fall-2026-Tech-Internships/#subscribe)**

</div>

> [!TIP]
> **⭐ Star this repo** to save it and get updates when new roles are added.

Instead of refreshing a dozen career pages by hand, it reads company hiring feeds directly and keeps one live list — newest roles on top, refreshed automatically throughout the day.

**🔔 New roles in your inbox:** [subscribe by email](https://crunchybiscuit19.github.io/Automated-List-Of-Summer-2027-and-Fall-2026-Tech-Internships/#subscribe) - one email a day, only when new internships actually appeared, unsubscribe from any email in two clicks. (Prefer RSS-to-email? [Feedrabbit works too](https://feedrabbit.com/subscriptions/new?url=https%3A%2F%2Fraw.githubusercontent.com%2FCrunchyBiscuit19%2FAutomated-List-Of-Summer-2027-and-Fall-2026-Tech-Internships%2Fmain%2Fdocs%2Ffeed.xml).)

---

## What this is

This is an engine, not a hand-kept list. It polls company career feeds every 30 minutes, finds the internships, removes duplicates, and rebuilds this page on its own.

Every link comes straight from the source — so it's real and current, not a stale list someone forgot to update. Speed matters.

## What makes this different

| | |
|---|---|
| 🌏 **Built for Singapore & Southeast Asia** | Every role is filtered to the region above, from the posting's own location. Country-prefixed and city-only postings are both understood, so a bare "Kuala Lumpur" or "SG-Singapore" is never missed. |
| 📆 **A real date on nearly every role** | Taken from the job portal itself wherever the portal states one, so newest-first actually means newest. The exact coverage figure is printed at the bottom of this page every run. |
| 🧰 **Skill tags + pay, extracted** | Every posting's text is scanned for the stack it wants (Python, C++, PyTorch, …) and the pay it states — searchable on the [dashboard](https://crunchybiscuit19.github.io/Automated-List-Of-Summer-2027-and-Fall-2026-Tech-Internships/), and included in the CSV and API. |
| 🔔 **Alerts your way** | [Email digests](https://crunchybiscuit19.github.io/Automated-List-Of-Summer-2027-and-Fall-2026-Tech-Internships/#subscribe) or [RSS](https://crunchybiscuit19.github.io/Automated-List-Of-Summer-2027-and-Fall-2026-Tech-Internships/feed.xml) — point any reader, or a Slack/Discord RSS integration, at it. Plus a [live dashboard](https://crunchybiscuit19.github.io/Automated-List-Of-Summer-2027-and-Fall-2026-Tech-Internships/) with search, filters, and a saved-roles list that never leaves your browser. |
| ⚙️ **An engine, not a spreadsheet** | 4,651 job-board endpoints (4,401 distinct employers; some run more than one board) polled every 30 minutes across 12 ATS platforms. Full source and tests in this repo. |

## Scope

| | |
|---|---|
| **Roles** | Software Engineering, Data Science & Machine Learning (and closely related technical internships) |
| **Region** | Singapore & Southeast Asia |
| **Cycles** | Summer 2027 and Fall 2026 |

## About

I built this for the search I'm doing myself, so it tracks Singapore & Southeast Asia — that's where I'm applying. Everything is filtered from each posting's own stated location, and the same engine can be pointed at another region by editing one line of [`data/config.json`](data/config.json).

Use it to spot roles early and apply before they fill up. Being first genuinely helps.

## Where this is going

I'm building this in the open and adding to it as it grows.

**Recently shipped:** email alerts · the live dashboard · Singapore & Southeast Asia coverage

**Next up:** personalized alerts (pick your categories) · per-company hiring pages · a ghost-posting detector

If it helps you, a star means a lot and tells me to keep going.

## How to use

<details>
<summary><b>Reading the table — flags, dates, and the cycle split</b> (click to expand)</summary>

- Roles are grouped by cycle below - **newest posting on top, oldest at the bottom.**
- A cycle section holds only roles whose **employer stated that cycle** - in the title, or in the posting's own text. Postings that name no cycle anywhere are in *Recently posted — cycle not stated* further down, with **no cycle guessed for them**. Same quality bar, different amount of evidence.
- The **Posted** column is the date the company published the role.
- **_(3 openings)_ after a role title** = the employer has that many separate live requisitions for the same job, in the same place, for the same cycle. They're all real and each takes its own application, so they're linked individually (**Apply**, then **#2**, **#3**) instead of repeating the row. Counts still count requisitions, and the CSV export is never grouped.
- **🆁 after a company name** = **this role is remote** — the posting's own location or title says so. It marks the role on that row, not the whole company.
- **🆕 after a role title** = spotted in the last 48 hours.
- **Work passes:** most roles here are open to students studying in the country concerned; in Singapore a non-resident intern normally needs a Work Holiday Pass or a Training Employment Pass, which the employer applies for. Postings rarely say either way, so confirm before you count on it.
- Track your applications with [`data/internships.csv`](data/internships.csv) (opens in Excel / Google Sheets).
- Missing a company? Adding one takes a single line, see [CONTRIBUTING.md](CONTRIBUTING.md).

</details>

---

## Summer 2027  (12 employer-stated)

| Company | Role | Category | Location | Skills | Posted | Apply |
|---|---|---|---|---|---|---|
| Sierra | Software Engineer Intern, Agent (Summer 2027) 🆕 | Software | Singapore | TypeScript, LLMs, React | Sep 07, 2026 | [Apply](https://jobs.ashbyhq.com/sierra/eb8e8b58-394b-43f0-b9bd-4f1407d9aa17) |
| Mastercard | Software Engineer Intern, Summer 2027 - Singapore | Software | Singapore | Python, Java, C#, JavaScript | Sep 04, 2026 | [Apply](https://mastercard.wd1.myworkdayjobs.com/Campus/job/Singapore/Software-Engineer-Intern--Summer-2027---Singapore_R-287574) |
| AppLovin | Mobile Engineering Intern (2027 Summer Internship) | Software | Singapore | Java, Swift, Kotlin | Aug 25, 2026 | [Apply](https://boards.greenhouse.io/applovin/jobs/4708448006?gh_jid=4708448006) |
| AppLovin | Backend Engineering Intern (2027 Summer Internship) | Software | Singapore | Python, Java, Linux, Kafka | Aug 25, 2026 | [Apply](https://boards.greenhouse.io/applovin/jobs/4708449006?gh_jid=4708449006) |
| Airwallex | Software Engineer Intern (Summer 2027) | Software | SG - Singapore | Kotlin, LLMs, React, Kubernetes | Aug 05, 2026 | [Apply](https://jobs.ashbyhq.com/airwallex/6cdb0f39-234a-4234-b1f1-cb48a1fa2795) |
| Shopback 2 | Software Engineer Intern - Backend (H1 2027) | Software | Singapore, Singapore | No skills listed | Aug 03, 2026 | [Apply](https://jobs.lever.co/shopback-2/1804a30e-2d2e-4631-9e85-614c91806ddf) |
| Hudson River Trading | Algorithm Development (Quant Research & Trading) Internship – Summer 2027 | Quant | London +5 more | Python, C++, MATLAB, Pandas | Jul 13, 2026 | [Apply](https://www.hudsonrivertrading.com/careers/job/?gh_jid=7964062) |
| Hudson River Trading | Software Engineering Internship (C++ or Python) – Summer 2027 | Software | Austin +11 more | Python, C++ | Jul 13, 2026 | [Apply](https://www.hudsonrivertrading.com/careers/job/?gh_jid=8052083) |
| Shopback 2 | Data Analyst (Internship) (H1 2027) | Data & ML/AI | Singapore, Singapore | Python, SQL, LLMs | Jun 22, 2026 | [Apply](https://jobs.lever.co/shopback-2/b216d68c-48b0-4fa5-8f1e-9e0375b993e1) |
| Squarepoint Capital | Intern Software Developer - Singapore - 2027 | Software | Singapore | Python, Java, C++, Rust | Aug 28, 2024 | [Apply](https://www.squarepoint-capital.com/open-opportunities?id=6201998&gh_jid=6201998) |
| Virtu Financial | 2027 Internship – Software Engineer | Software | Singapore | Python, Java, C++, JavaScript | Aug 31, 2021 | [Apply](https://job-boards.greenhouse.io/virtu/jobs/5513756002) |
| Virtu Financial | 2027 Internship - Quantitative Trading | Quant | Singapore | Python, Java, C++, SQL | Apr 16, 2021 | [Apply](https://job-boards.greenhouse.io/virtu/jobs/5208637002) |

## Fall 2026  (5 employer-stated)

| Company | Role | Category | Location | Skills | Posted | Apply |
|---|---|---|---|---|---|---|
| Bosch | Internship in IT Solution Developer 🆕 | Software | Batu Kawan, Penang, Malaysia | Python, JavaScript, SQL | Sep 09, 2026 | [Apply](https://jobs.smartrecruiters.com/BoschGroup/744000148364924) |
| Cantina | Machine Learning Intern | Data & ML/AI | Singapore | Python, Computer Vision, AWS, GCP | Sep 07, 2026 | [Apply](https://jobs.ashbyhq.com/cantina/16c7915e-9fd7-413f-b7ee-590589fbdc01) |
| Procter & Gamble (P&G) | Data Science Intern (Semester 2026) - P&G Management Internship Program - Bachelor's Degree or above | Data & ML/AI | SINGAPORE GENERAL OFFICE | Python | Aug 16, 2026 | [Apply](https://pg.wd5.myworkdayjobs.com/1000/job/SINGAPORE-GENERAL-OFFICE/Data-Science-Intern--Semester-2026----P-G-Management-Internship-Program---Bachelor-s-Degree-or-above_R000157419) |
| Bosch | [Internship Program Q4] Embedded Software Intern (C/C++/Linux) 🆕 _(2 openings)_ | Software | Ho Chi Minh, , Vietnam | C++, Python | Aug 13, 2026 | [Apply](https://jobs.smartrecruiters.com/BoschGroup/744000143206979) [#2](https://jobs.smartrecruiters.com/BoschGroup/744000148366240) |
| Bosch | [Internship Program Q4] AI Engineer Intern | Data & ML/AI | Ho Chi Minh, , Vietnam | Python, C++, PyTorch, TensorFlow | Aug 07, 2026 | [Apply](https://jobs.smartrecruiters.com/BoschGroup/744000142038898) |

## Recently posted — cycle not stated  (52 roles)

These postings never name a cycle — not in the title, not in the posting text — so neither do we. They're recent tech internships (posted within the last few weeks), often exactly the early drops worth applying to first; we just can't tell you which cycle they're for, and we'd rather say so than guess. The moment a posting's own text states a cycle, the role moves up into that section automatically.

| Company | Role | Category | Location | Skills | Posted | Apply |
|---|---|---|---|---|---|---|
| Razer | AI Engineer Intern 🆕 | Data & ML/AI | Singapore | Python, LLMs | Sep 11, 2026 | [Apply](https://razer.wd3.myworkdayjobs.com/Careers/job/Singapore/AI-Engineer-Intern_JR2026006947) |
| Razer | Product Developer Intern 🆕 | Software | Singapore | LLMs, Tableau | Sep 11, 2026 | [Apply](https://razer.wd3.myworkdayjobs.com/Careers/job/Singapore/Product-Developer-Intern_JR2026007822) |
| Razer | Software Engineer Intern 🆕 | Software | Singapore | Python, TypeScript, JavaScript, React | Sep 11, 2026 | [Apply](https://razer.wd3.myworkdayjobs.com/Careers/job/Singapore/Software-Engineer-Intern_JR2026007809) |
| Mufgub | Cyber Security Architecture & Engineering Intern 🆕 | Security | Singapore Office OCC | LLMs | Sep 10, 2026 | [Apply](https://mufgub.wd3.myworkdayjobs.com/MUFG-EarlyCareers/job/Singapore-Office-OCC/Cyber-Security-Architecture---Engineering-Intern_10079342-WD) |
| Mufgub | Cyber Security Threat Detection & Incident Response Intern 🆕 | Security | Singapore Office OCC | Python, LLMs | Sep 10, 2026 | [Apply](https://mufgub.wd3.myworkdayjobs.com/MUFG-EarlyCareers/job/Singapore-Office-OCC/Cyber-Security-Threat-Detection---Incident-Response-Intern_10079338-WD) |
| Thales | Software Engineer Intern 🆕 | Software | Singapore | Java, TypeScript, Angular, HTML/CSS | Sep 09, 2026 | [Apply](https://thales.wd3.myworkdayjobs.com/careers/job/Singapore/Software-Engineer-Intern_R0339658) |
| Trend Micro | Cybersecurity Intern 🆕 | Security | Manila | Python | Sep 09, 2026 | [Apply](https://trendmicro.wd3.myworkdayjobs.com/External/job/Manila/Cybersecurity-Intern_R0005760) |
| Trend Micro | Global Infrastructure Services Intern 🆕 | Software | Manila | No skills listed | Sep 09, 2026 | [Apply](https://trendmicro.wd3.myworkdayjobs.com/External/job/Manila/Global-Infrastructure-Services-Intern_R0009489) |
| Grab | Intern, Software Engineer Mobile 🆕 | Software | Petaling Jaya, , Malaysia | Python, Java, C++, Swift | Sep 09, 2026 | [Apply](https://jobs.smartrecruiters.com/grab/744000148399141) |
| Intel | System Software Engineering Intern 🆕 | Software | Malaysia, Kulim | Python, C++ | Sep 09, 2026 | [Apply](https://intel.wd1.myworkdayjobs.com/external/job/Malaysia-Kulim/System-Software-Engineering-Intern_JR0286933) |
| Hewlett Packard (HP) | College Intern - AI Transformation 🆕 | Data & ML/AI | Singapore, South West, Singapore | No skills listed | Sep 08, 2026 | [Apply](https://hp.wd5.myworkdayjobs.com/ExternalCareerSite/job/Singapore-South-West-Singapore/College-Intern---AI-Transformation_UNI4908-1) |
| Intel | DevOps and Software Engineering Intern | Software | Malaysia, Kulim | Python, Java, C#, JavaScript | Sep 08, 2026 | [Apply](https://intel.wd1.myworkdayjobs.com/external/job/Malaysia-Kulim/DevOps-and-Software-Engineering-Intern_JR0286934) |
| Applied Materials | Customer Engineer - Data Science / ML DevOps Internship | Data & ML/AI | Singapore,SGP | Python | Sep 08, 2026 | [Apply](https://amat.wd1.myworkdayjobs.com/External/job/SingaporeSGP/Customer-Engineer---Data-Science---ML-DevOps-Internship_R2626447) |
| Hewlett Packard Enterprise | AI and Machine Learning Intern | Data & ML/AI | Singapore, Central Singapore, Singapore | LLMs | Sep 08, 2026 | [Apply](https://hpe.wd5.myworkdayjobs.com/Jobsathpe/job/Singapore-Central-Singapore-Singapore/AI-and-Machine-Learning-Intern_1213583) |
| Hewlett Packard Enterprise | Embedded Software (Firmware) Internship | Hardware | Singapore, Central Singapore, Singapore | No skills listed | Sep 08, 2026 | [Apply](https://hpe.wd5.myworkdayjobs.com/Jobsathpe/job/Singapore-Central-Singapore-Singapore/Embedded-Software--Firmware--Internship_1213618) |
| Micron Technology | Intern - STPG PE Firmware | Hardware | MSB, Singapore | Python, C++, LLMs | Sep 08, 2026 | [Apply](https://micron.wd1.myworkdayjobs.com/External/job/MSB-Singapore/Intern---STPG-PE-FIrmware_JR111318) |
| Stripe | Software Engineer, Intern | Software | Singapore | Java, JavaScript, Scala, Ruby | Sep 07, 2026 | [Apply](https://stripe.com/jobs/search?gh_jid=8130883) |
| Intel | Intern System Software Development Engineer | Software | Malaysia, Kulim | Python, C#, SQL, Angular | Sep 07, 2026 | [Apply](https://intel.wd1.myworkdayjobs.com/external/job/Malaysia-Kulim/Intern-System-Software-Development-Engineer_JR0286935) |
| PricewaterhouseCoopers (PwC) | Risk Services - AI Factory Data Scientist Off-Cycle Internship (Jan - Jun 27) | Data & ML/AI | Singapore - Marina One | Python, Java, C++, LLMs | Sep 07, 2026 | [Apply](https://pwc.wd3.myworkdayjobs.com/Global_Campus_Careers/job/Singapore---Marina-One/Risk-Services---AI-Factory-Data-Scientist-Off-Cycle-Internship--Jan---Jun-27-_741280WD) |
| Bosch | [Bosch HcP - Internship] Industrial AI Engineer Intern | Data & ML/AI | An Phuoc Commune, Dong Nai, Vietnam | Python, SQL, PyTorch, TensorFlow | Sep 07, 2026 | [Apply](https://jobs.smartrecruiters.com/BoschGroup/744000147750000) |
| Hitachi Energy | AI-Driven Full Stack Intern | Data & ML/AI | Ho Chi Minh City, Ho Chi Minh, Vietnam | Python, Java, C#, LLMs | Sep 07, 2026 | [Apply](https://hitachi.wd1.myworkdayjobs.com/hitachi/job/Ho-Chi-Minh-City-Ho-Chi-Minh-Vietnam/AI-Driven-Full-Stack-Intern_R0142916) |
| Micron Technology | Intern - NAND Product Engineering - Probe AI/ML | Data & ML/AI | Fab 10N/X, Singapore | Python, PyTorch, TensorFlow, scikit-learn | Sep 07, 2026 | [Apply](https://micron.wd1.myworkdayjobs.com/External/job/Fab-10NX-Singapore/Intern---NAND-Product-Engineering---Probe-AI-ML_JR110821) |
| BP | Summer Internship-Technology-Data & AI- Malaysia | Data & ML/AI | Malaysia - Kuala Lumpur | Python, Java, C#, SQL | Sep 07, 2026 | [Apply](https://bpinternational.wd3.myworkdayjobs.com/bpCareers/job/Malaysia---Kuala-Lumpur/Summer-Internship-Technology-Data---AI--Malaysia_RQ115469-2) |
| Bosch | [BD] AI Software QA Intern (Next-Gen & AI-Driven Testing / 6-month Internship) | Data & ML/AI | Ho Chi Minh, , Vietnam | Python, TypeScript, SQL, LLMs | Sep 04, 2026 | [Apply](https://jobs.smartrecruiters.com/BoschGroup/744000147398230) |
| Bosch | [SX/BSV-VN] Embedded Test Engineer Intern 🆕 _(2 openings)_ | Software | Ha Noi, , Vietnam | Python, Linux | Sep 04, 2026 | [Apply](https://jobs.smartrecruiters.com/BoschGroup/744000147458139) [#2](https://jobs.smartrecruiters.com/BoschGroup/744000148655057) |
| Tencent | Data Science Intern (Analytics), 6-month internship | Data & ML/AI | Singapore-CapitaSky | Python, SQL, LLMs | Sep 04, 2026 | [Apply](https://tencent.wd1.myworkdayjobs.com/Tencent_Careers/job/Singapore-CapitaSky/Data-Science-Intern--Analytics---6-month-internship_R107974) |
| Thales | Software Development and Integration Engineer (Intern) | Software | Singapore | Java, TypeScript, Angular, HTML/CSS | Sep 04, 2026 | [Apply](https://thales.wd3.myworkdayjobs.com/careers/job/Singapore/Software-Development-and-Integration-Engineer--Intern-_R0339158) |
| Western Digital | Internship - Software Development (Embedded) | Software | Petaling Jaya, Selangor, Malaysia | Python, C++ | Sep 02, 2026 | [Apply](https://jobs.smartrecruiters.com/WesternDigital/744000146883869) |
| Thales | Software Engineer Intern - Middleware (IBS) | Software | Singapore | Java, Swift, Kotlin | Sep 02, 2026 | [Apply](https://thales.wd3.myworkdayjobs.com/careers/job/Singapore/Software-Engineer-Intern---Middleware--IBS-_R0334782) |
| Tower Research Capital | Quantitative Researcher Intern, Bachelor's or Master's | Quant | Singapore, Hong Kong, Shanghai, Sydney | Python, C++, Linux | Sep 01, 2026 | [Apply](https://www.tower-research.com/open-positions/?gh_jid=8168750) |
| Mufgub | Cybersecurity Awareness & Training Intern | Security | Singapore Office OCC | No skills listed | Sep 01, 2026 | [Apply](https://mufgub.wd3.myworkdayjobs.com/MUFG-EarlyCareers/job/Singapore-Office-OCC/Cybersecurity-Awareness---Training-Intern_10078999-WD) |
| Marinabaysands | Intern, Cyber Security | Security | Marina Bay Sands, Singapore | No skills listed | Aug 28, 2026 | [Apply](https://marinabaysands.wd102.myworkdayjobs.com/external/job/Marina-Bay-Sands-Singapore/Intern--Cyber-Security_JR10000208) |
| Marinabaysands | Intern, Developer (Middleware) | Software | Perennial Business City, Singapore | Java, SQL, Spring, Git | Aug 28, 2026 | [Apply](https://marinabaysands.wd102.myworkdayjobs.com/external/job/Perennial-Business-City-Singapore/Intern--Developer--Middleware-_JR10007967) |
| Marinabaysands | Intern, Developer A.I | Software | Perennial Business City, Singapore | Python, Java, C#, JavaScript | Aug 28, 2026 | [Apply](https://marinabaysands.wd102.myworkdayjobs.com/external/job/Perennial-Business-City-Singapore/Intern--Developer-AI_JR10007970) |
| Swift | Site Reliability Engineering (SRE) Intern | Software | Kuala Lumpur, Malaysia | Swift, Tableau | Aug 28, 2026 | [Apply](https://swift.wd3.myworkdayjobs.com/join-swift/job/Kuala-Lumpur-Malaysia/Site-Reliability-Engineering--SRE--Intern_2026-16467) |
| Trend Micro | GRID DEVOPS INTERN | Software | Manila | No skills listed | Aug 27, 2026 | [Apply](https://trendmicro.wd3.myworkdayjobs.com/External/job/Manila/GRID-DEVOPS-INTERN_R0010148) |
| Hitachi Energy | Embedded Engineering Software Internship | Software | Ho Chi Minh City, Ho Chi Minh, Vietnam | C++, Linux | Aug 26, 2026 | [Apply](https://hitachi.wd1.myworkdayjobs.com/hitachi/job/Ho-Chi-Minh-City-Ho-Chi-Minh-Vietnam/Embedded-Internship_R0142038) |
| Jump Trading | Campus AI/ML Researcher (Intern) | Data & ML/AI | Hong Kong; Shanghai; Singapore | Python, C++, PyTorch, TensorFlow | Aug 24, 2026 | [Apply](https://www.jumptrading.com/hr/job?gh_jid=8027938) |
| Western Digital | Intern - AI Information Technology (Studying Master's and Bachelor Degree) | Data & ML/AI | BangPa-in +2 more | Python, Java, C++, C# | Aug 24, 2026 | [Apply](https://jobs.smartrecruiters.com/WesternDigital/744000145156358) |
| Hitachi Energy | Embedded Software Engineer Internship | Software | Da Nang, Đà Nẵng, Vietnam | C++, Linux | Aug 20, 2026 | [Apply](https://hitachi.wd1.myworkdayjobs.com/hitachi/job/Da-Nang--Nng-Vietnam/Embedded-Software-Engineer-Internship_R0142219) |
| Swift | Software/Systems Engineer - Intern | Software | Kuala Lumpur, Malaysia | Java, JavaScript, Swift, HTML/CSS | Aug 20, 2026 | [Apply](https://swift.wd3.myworkdayjobs.com/join-swift/job/Kuala-Lumpur-Malaysia/Software-Systems-Engineer---Intern_2026-16387) |
| Tencent | Software Engineering Intern (Overseas AdTech Data Systems) | Data & ML/AI | Singapore-CapitaSky | Java, AWS, Kubernetes, Docker | Aug 19, 2026 | [Apply](https://tencent.wd1.myworkdayjobs.com/Tencent_Careers/job/Singapore-CapitaSky/Software-Engineering-Intern--Overseas-AdTech-Data-Systems-_R108000) |
| Tower Research Capital | Quantitative Developer Intern | Quant | Singapore | Python, C++, Bash, Pandas | Aug 18, 2026 | [Apply](https://www.tower-research.com/open-positions/?gh_jid=8138524) |
| Huntsman | Business Intelligence & AI Analytics Intern | Data & ML/AI | Malaysia - Kuala Lumpur | SQL, LLMs, Databricks | Aug 18, 2026 | [Apply](https://huntsman.wd1.myworkdayjobs.com/Huntsman/job/Malaysia---Kuala-Lumpur/Business-Intelligence---AI-Analytics-Intern_J-020202) |
| Tencent | Cloud Engineer Intern | Software | Singapore-CapitaSky | Python, PyTorch, LLMs, AWS | Aug 18, 2026 | [Apply](https://tencent.wd1.myworkdayjobs.com/Tencent_Careers/job/Singapore-CapitaSky/Cloud-Engineer-Intern_R107771) |
| DRW | Software Engineer Intern (Data Engineering) | Data & ML/AI | Singapore | Python, Pandas, Kubernetes, PostgreSQL | Aug 13, 2026 | [Apply](https://job-boards.greenhouse.io/drweng/jobs/8127242) |
| Jump Trading | Campus Quantitative Researcher (Intern) | Quant | Singapore | Python, C++ | Aug 03, 2026 | [Apply](https://www.jumptrading.com/hr/job?gh_jid=8027939) |
| Jump Trading | Campus Quantitative Trader (Intern) | Quant | Singapore | No skills listed | Aug 03, 2026 | [Apply](https://www.jumptrading.com/hr/job?gh_jid=8027941) |
| Western Digital | Intern Firmware Engineering _(3 openings)_ | Hardware | Petaling Jaya, Selangor, Malaysia | Python, C++ | Aug 03, 2026 | [Apply](https://jobs.smartrecruiters.com/WesternDigital/744000141227773) [#2](https://jobs.smartrecruiters.com/WesternDigital/744000141229499) [#3](https://jobs.smartrecruiters.com/WesternDigital/744000141840819) |
| Xendit | Full Stack Developer Intern | Software | Jakarta, Indonesia | TypeScript, JavaScript, SQL, React | Jul 30, 2026 | [Apply](https://job-boards.greenhouse.io/xendit/jobs/7821207003) |
| Xendit | Data / ML Automation Intern | Data & ML/AI | Jakarta, Indonesia | Python, TypeScript, SQL, PyTorch | Jul 30, 2026 | [Apply](https://job-boards.greenhouse.io/xendit/jobs/7821208003) |
| Simular | Data Analyst Intern | Data & ML/AI | Singapore | Python, SQL, dbt | Jul 29, 2026 | [Apply](https://jobs.ashbyhq.com/simular/7147a575-c7da-44d3-a6d6-2cdd4d24b94a) |

<details>
<summary><strong>Recently closed</strong> — 40 roles that left the list in the last 14 days</summary>

_Why each one left is in the last column, because the two reasons carry different evidence. **Gone from feed** = two consecutive complete reads of the employer's board no longer returned it (strong, but not the employer telling us directly). **Out of scope** = still posted, but it no longer passes our filters — our call, not theirs. **Not recorded** = closed before we started tracking the reason._

| Company | Role | Cycle | Closed | Why |
|---|---|---|---|---|
| Amazon | Software Development Engineer Intern, AWS Data Services - Fall 2026 (US) | Fall 2026 | 2026-09-06 | out of scope |
| Amazon | Robotics - Software Development Engineer Fall Intern/Co-op - 2026 | Fall 2026 | 2026-09-06 | out of scope |
| Amazon | Software Development Engineer Intern, Annapurna Labs - 2027 | Summer 2027 | 2026-09-06 | out of scope |
| Amazon | Robotics - Applied Scientist II Intern / Co-op - 2026 (Robotics, Manipulation, Perception, Motion Planning, Autonomous Mobile Robots, Computer Vision, Machine Learning, Controls, and more) | Fall 2026 | 2026-09-06 | out of scope |
| Beacon Software | Software Engineering Intern | Fall 2026 | 2026-09-06 | out of scope |
| Ellipsis Labs | Software Engineer - 2027 Interns | Summer 2027 | 2026-09-06 | out of scope |
| Hadrian | Software Engineer Intern | Fall 2026 | 2026-09-06 | out of scope |
| Hadrian | Data Science/ Data Engineer Intern | Fall 2026 | 2026-09-06 | out of scope |
| Heliux | Software Engineer (Internship, Summer 2027) | Summer 2027 | 2026-09-06 | out of scope |
| Junior | Software Engineering Intern — Fall 2026 | Fall 2026 | 2026-09-06 | out of scope |
| Melius | Software Engineering Intern [Fall/Winter 2026] | Fall 2026 | 2026-09-06 | out of scope |
| Melius | Software Engineering Intern [Spring/Summer 2027] | Summer 2027 | 2026-09-06 | out of scope |
| Northwood Space | Software Engineering Intern (2027 Summer Internship) | Summer 2027 | 2026-09-06 | out of scope |
| Northwood Space | Embedded Software Engineering Intern (2027 Summer Internship) | Summer 2027 | 2026-09-06 | out of scope |
| Notion | Software Engineer Intern (Summer 2027) | Summer 2027 | 2026-09-06 | out of scope |
| Phoebe | Software Engineering Intern | Fall 2026 | 2026-09-06 | out of scope |
| Quadrillion | Software Engineering Intern (Summer 2027) | Summer 2027 | 2026-09-06 | out of scope |
| Rivet Industries | Software Engineer Intern, XR Team (Fall 2026) | Fall 2026 | 2026-09-06 | out of scope |
| The Voleon Group | Software Engineer Intern - (Summer 2027) | Summer 2027 | 2026-09-06 | out of scope |
| Wavetronix | Computer Science Internship Summer 2027 | Summer 2027 | 2026-09-06 | out of scope |
| Advanced Space | 2027 Software Engineering Summer Internship | Summer 2027 | 2026-09-06 | out of scope |
| Advanced Space | 2027 Machine Learning Summer Internship | Summer 2027 | 2026-09-06 | out of scope |
| Advanced Space | 2027 DevOps Summer Internship | Summer 2027 | 2026-09-06 | out of scope |
| Akuna Capital | Software Engineer Intern - C++, Summer 2027 | Summer 2027 | 2026-09-06 | out of scope |
| Akuna Capital | Software Engineer Intern - Python, Summer 2027 | Summer 2027 | 2026-09-06 | out of scope |
| Akuna Capital | Platform Engineer Intern, Summer 2027 | Summer 2027 | 2026-09-06 | out of scope |
| Akuna Capital | Software Engineer Intern - C# .NET Desktop, Summer 2027 | Summer 2027 | 2026-09-06 | out of scope |
| Akuna Capital | Software Engineer Intern - Full Stack Web, Summer 2027 | Summer 2027 | 2026-09-06 | out of scope |
| Akuna Capital | Quantitative Research Intern, Summer 2027 | Summer 2027 | 2026-09-06 | out of scope |
| Anduril | 2027 Software Engineer Intern | Summer 2027 | 2026-09-06 | out of scope |
| Appian | Software Engineering Intern | Summer 2027 | 2026-09-06 | out of scope |
| Appian | Information Security Engineer Intern | Summer 2027 | 2026-09-06 | out of scope |
| Awetomaton | Platform Engineering Intern | Summer 2027 | 2026-09-06 | out of scope |
| Axon | 2027 US Firmware Engineering Internship | Summer 2027 | 2026-09-06 | out of scope |
| BTI360 | Software Engineering Intern | Summer 2027 | 2026-09-06 | out of scope |
| Charles River Associates (CRA) | (2028 Bachelor's/Master's graduates) Cyber and Forensic Technology Consulting Analyst/Associate Intern (Summer 2027) | Summer 2027 | 2026-09-06 | out of scope |
| Chicago Trading Company | Quant Trading Internship - Summer 2027 | Summer 2027 | 2026-09-06 | out of scope |
| Chicago Trading Company | Software Engineering Internship - Summer 2027 | Summer 2027 | 2026-09-06 | out of scope |
| Dev Technology Group | AI/ML Intern (Summer 2027) | Summer 2027 | 2026-09-06 | out of scope |
| Dev Technology Group | React/Node Developer Intern (Summer 2027) | Summer 2027 | 2026-09-06 | out of scope |

</details>

---

## Hiring timeline

Internships posted per week, from each role's real published date - redrawn automatically on every run. When this line takes off, recruiting season is open:

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="docs/trends-dark.svg">
  <img alt="Internships posted per week, drawn from real published dates" src="docs/trends-light.svg">
</picture>

## How it stays current

A small Python engine reads public company hiring feeds directly, keeps the roles that match the scope above, de-duplicates across sources, records each role's published date once (so it never shifts), and regenerates this page through GitHub Actions. It polls every company concurrently (async) with retry/backoff and per-host rate limits. The full source is in this repo.

_Engine (last run): 4,253 of 4,651 registered boards returned successfully across 12 ATS platforms (97% of boards attempted, 91% of the full registry) · completed in 1118.7s · 568 board(s) returned a capped result set, so their roles were not eligible to be closed this run · employer or source-derived date on 100% of open roles._

## How this list is built

[METHODOLOGY.md](METHODOLOGY.md) documents exactly what every label claims — what separates a stated cycle from an inferred one, what the ✓ H-1B badge does and doesn't mean, how a role gets closed, and which limitations are known. Anything on this page that doesn't match the code is a bug worth reporting.

## Contributing

Adding a company takes one line, see [CONTRIBUTING.md](CONTRIBUTING.md), or just [open a request](../../issues/new?template=add-company.yml) with the board URL. **Spotted something wrong?** [Report the exact field](../../issues/new?template=wrong-data.yml) — wrong country, wrong cycle, closed role, bad sponsorship flag. Those reports usually fix a rule, which fixes every other role too.

Also here: [PRIVACY.md](PRIVACY.md) (what the email list stores — an address and nothing else) · [SECURITY.md](SECURITY.md) · [ARCHITECTURE.md](ARCHITECTURE.md) · [MIT licensed](LICENSE).

Built by one student with AI assistance, in the open. The part that matters isn't who typed it — it's that the rules, the tests, and every run's output are all public and checkable.

## Note on dates

The **Posted** column shows when a role was published, with the newest at the top. I pull the posting date straight from each job portal, but a lot of them don't expose one publicly, so those rows show a dash (—) for now instead of a guessed date. The ones that do publish a date are dated. Know the real date for a dashed role? Open a PR and I'll merge it.

Roles can close at any time, so always confirm on the company's own site before applying.
