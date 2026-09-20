<div align="center">

# 🎓 Summer 2027 Tech Internships — Singapore & Southeast Asia

**A self-updating engine that tracks tech internships so you don't have to.**

[![CI](https://img.shields.io/github/actions/workflow/status/CrunchyBiscuit19/Automated-List-Of-Summer-2027-and-Fall-2026-Tech-Internships/ci.yml?branch=main&label=tests&style=flat-square&color=3fb950)](https://github.com/CrunchyBiscuit19/Automated-List-Of-Summer-2027-and-Fall-2026-Tech-Internships/actions/workflows/ci.yml)&nbsp;[![Open roles](https://img.shields.io/badge/dynamic/json?label=open%20roles&query=open_total&url=https%3A%2F%2Fcrunchybiscuit19.github.io%2FAutomated-List-Of-Summer-2027-and-Fall-2026-Tech-Internships%2Fapi%2Fstats.json&color=2f81f7&style=flat-square)](https://crunchybiscuit19.github.io/Automated-List-Of-Summer-2027-and-Fall-2026-Tech-Internships/)&nbsp;![Updates](https://img.shields.io/badge/updates-every%2030%20min-3fb950?style=flat-square)&nbsp;[![RSS](https://img.shields.io/badge/RSS-subscribe-e67e22?style=flat-square)](https://crunchybiscuit19.github.io/Automated-List-Of-Summer-2027-and-Fall-2026-Tech-Internships/feed.xml)

### 109 open roles (82 listed below) · 32 new this week

4,401 employers tracked · data as of Sep 20, 2026 at 13:17 UTC

_35 have a cycle the employer stated · 74 are recent postings whose cycle isn't stated (listed separately, never mixed in)._

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

## Summer 2027  (19 employer-stated)

| Company | Role | Category | Location | Skills | Posted | Apply |
|---|---|---|---|---|---|---|
| Autodesk | Intern, Software Development Engineer [PSET-Access-ENG] _(4 openings)_ | Software | Singapore, SGP | Python, C++, Rust, Bash | Sep 15, 2026 | [Apply](https://autodesk.wd1.myworkdayjobs.com/uni/job/Singapore-SGP/Intern--Software-Development-Engineer--PSET-Access-ENG-_26WD100985) [#2](https://autodesk.wd1.myworkdayjobs.com/uni/job/Singapore-SGP/Intern--Software-Development-Engineer--PSET-Access-ENG-_26WD100986) [#3](https://autodesk.wd1.myworkdayjobs.com/uni/job/Singapore-SGP/Intern--Software-Development-Engineer--PSET-Access-ENG-_26WD100988) [#4](https://autodesk.wd1.myworkdayjobs.com/uni/job/Singapore-SGP/Intern--Software-Development-Engineer--PSET-Access-ENG-_26WD100989) |
| Autodesk | Intern, Software Development Engineer [PSET-Connected Delivery] | Software | Singapore, SGP | Python, C++, React, Angular | Sep 15, 2026 | [Apply](https://autodesk.wd1.myworkdayjobs.com/uni/job/Singapore-SGP/Intern--Software-Development-Engineer--PSET-Connected-Delivery-_26WD100995) |
| Autodesk | Intern, Software Development Engineer [PSET-Localization] _(2 openings)_ | Software | Singapore, SGP | Python, Java, JavaScript, SQL | Sep 15, 2026 | [Apply](https://autodesk.wd1.myworkdayjobs.com/uni/job/Singapore-SGP/Intern--Software-Development-Engineer--PSET-Localization-_26WD100997) [#2](https://autodesk.wd1.myworkdayjobs.com/uni/job/Singapore-SGP/Intern--Software-Development-Engineer--PSET-Localization-_26WD100998-1) |
| AppLovin | Machine Learning Engineering Intern (2027 Summer Internship) | Data & ML/AI | Singapore | Python, PyTorch, TensorFlow | Sep 14, 2026 | [Apply](https://boards.greenhouse.io/applovin/jobs/4713038006?gh_jid=4713038006) |
| JPMorganChase | 2027 Markets Quantitative Trading & Research Associate Program – Off-Cycle Internship - Singapore | Quant | Singapore | Python, Java, C++, C# | Sep 13, 2026 | [Apply](https://jpmc.fa.oraclecloud.com/hcmUI/CandidateExperience/en/sites/CX_1/job/210784061) |
| JPMorganChase | 2027 Markets Quantitative Trading & Research Analyst Program – Off-Cycle Internship - Singapore | Quant | Singapore | Python, Java, C++, C# | Sep 13, 2026 | [Apply](https://jpmc.fa.oraclecloud.com/hcmUI/CandidateExperience/en/sites/CX_1/job/210784366) |
| Sierra | Software Engineer Intern, Agent (Summer 2027) | Software | Singapore | TypeScript, LLMs, React | Sep 07, 2026 | [Apply](https://jobs.ashbyhq.com/sierra/eb8e8b58-394b-43f0-b9bd-4f1407d9aa17) |
| Mastercard | Software Engineer Intern, Summer 2027 - Singapore | Software | Singapore | Python, Java, C#, JavaScript | Sep 04, 2026 | [Apply](https://mastercard.wd1.myworkdayjobs.com/Campus/job/Singapore/Software-Engineer-Intern--Summer-2027---Singapore_R-287574) |
| JPMorganChase | 2027 Data & AI Program - Summer Internship - Singapore | Data & ML/AI | Singapore, Singapore | Python, SQL, LLMs, AWS | Aug 27, 2026 | [Apply](https://jpmc.fa.oraclecloud.com/hcmUI/CandidateExperience/en/sites/CX_1/job/210783022) |
| AppLovin | Mobile Engineering Intern (2027 Summer Internship) | Software | Singapore | Java, Swift, Kotlin | Aug 25, 2026 | [Apply](https://boards.greenhouse.io/applovin/jobs/4708448006?gh_jid=4708448006) |
| AppLovin | Backend Engineering Intern (2027 Summer Internship) | Software | Singapore | Python, Java, Linux, Kafka | Aug 25, 2026 | [Apply](https://boards.greenhouse.io/applovin/jobs/4708449006?gh_jid=4708449006) |
| Airwallex | Software Engineer Intern (Summer 2027) | Software | SG - Singapore | Kotlin, LLMs, React, Kubernetes | Aug 05, 2026 | [Apply](https://jobs.ashbyhq.com/airwallex/6cdb0f39-234a-4234-b1f1-cb48a1fa2795) |
| Shopback 2 | Software Engineer Intern (H1 2027) | Software | Singapore, Singapore | No skills listed | Aug 03, 2026 | [Apply](https://jobs.lever.co/shopback-2/1804a30e-2d2e-4631-9e85-614c91806ddf) |
| Hudson River Trading | Algorithm Development (Quant Research & Trading) Internship – Summer 2027 | Quant | London +5 more | Python, C++, MATLAB, Pandas | Jul 13, 2026 | [Apply](https://www.hudsonrivertrading.com/careers/job/?gh_jid=7964062) |
| Hudson River Trading | Software Engineering Internship (C++ or Python) – Summer 2027 | Software | Austin +11 more | Python, C++ | Jul 13, 2026 | [Apply](https://www.hudsonrivertrading.com/careers/job/?gh_jid=8052083) |
| Shopback 2 | Data Analyst (Internship) (H1 2027) | Data & ML/AI | Singapore, Singapore | Python, SQL, LLMs | Jun 22, 2026 | [Apply](https://jobs.lever.co/shopback-2/b216d68c-48b0-4fa5-8f1e-9e0375b993e1) |
| Squarepoint Capital | Intern Software Developer - Singapore - 2027 | Software | Singapore | Python, Java, C++, Rust | Aug 28, 2024 | [Apply](https://www.squarepoint-capital.com/open-opportunities?id=6201998&gh_jid=6201998) |
| Virtu Financial | 2027 Internship – Software Engineer | Software | Singapore | Python, Java, C++, JavaScript | Aug 31, 2021 | [Apply](https://job-boards.greenhouse.io/virtu/jobs/5513756002) |
| Virtu Financial | 2027 Internship - Quantitative Trading | Quant | Singapore | Python, Java, C++, SQL | Apr 16, 2021 | [Apply](https://job-boards.greenhouse.io/virtu/jobs/5208637002) |

## Fall 2026  (6 employer-stated)

| Company | Role | Category | Location | Skills | Posted | Apply |
|---|---|---|---|---|---|---|
| Autodesk | Intern, Software Development Engineer [PSET-Access-ENG] | Software | Singapore, SGP | Python, Java, C++, C# | Sep 15, 2026 | [Apply](https://autodesk.wd1.myworkdayjobs.com/uni/job/Singapore-SGP/Intern--Software-Development-Engineer--PSET-Access-ENG-_26WD100987-1) |
| Bosch | Internship in IT Solution Developer | Software | Batu Kawan, Penang, Malaysia | Python, JavaScript, SQL | Sep 09, 2026 | [Apply](https://jobs.smartrecruiters.com/BoschGroup/744000148364924) |
| Cantina | Machine Learning Intern | Data & ML/AI | Singapore | Python, Computer Vision, AWS, GCP | Sep 07, 2026 | [Apply](https://jobs.ashbyhq.com/cantina/16c7915e-9fd7-413f-b7ee-590589fbdc01) |
| Procter & Gamble (P&G) | Data Science Intern (Semester 2026) - P&G Management Internship Program - Bachelor's Degree or above | Data & ML/AI | SINGAPORE GENERAL OFFICE | Python | Aug 16, 2026 | [Apply](https://pg.wd5.myworkdayjobs.com/1000/job/SINGAPORE-GENERAL-OFFICE/Data-Science-Intern--Semester-2026----P-G-Management-Internship-Program---Bachelor-s-Degree-or-above_R000157419) |
| Bosch | [Internship Program Q4] Embedded Software Intern (C/C++/Linux) _(3 openings)_ | Software | Ho Chi Minh, , Vietnam | C++, Python | Aug 13, 2026 | [Apply](https://jobs.smartrecruiters.com/BoschGroup/744000143206979) [#2](https://jobs.smartrecruiters.com/BoschGroup/744000148366240) [#3](https://jobs.smartrecruiters.com/BoschGroup/744000149236759) |
| Bosch | [Internship Program Q4] AI Engineer Intern | Data & ML/AI | Ho Chi Minh, , Vietnam | Python, C++, PyTorch, TensorFlow | Aug 07, 2026 | [Apply](https://jobs.smartrecruiters.com/BoschGroup/744000142038898) |

## Recently posted — cycle not stated  (50 roles)

These postings never name a cycle — not in the title, not in the posting text — so neither do we. They're recent tech internships (posted within the last few weeks), often exactly the early drops worth applying to first; we just can't tell you which cycle they're for, and we'd rather say so than guess. The moment a posting's own text states a cycle, the role moves up into that section automatically.

| Company | Role | Category | Location | Skills | Posted | Apply |
|---|---|---|---|---|---|---|
| qode.world | Full Stack Engineering Intern | Software | Ho Chi Minh City, Ho Chi Minh, Vietnam | TypeScript, JavaScript, SQL, Next.js | Sep 18, 2026 | [Apply](https://apply.workable.com/qodeworld/j/E833248FA2/) |
| Williams-Sonoma | Data Analyst (Finance) Intern (6 months) | Data & ML/AI | Singapore | Python, SQL | Sep 18, 2026 | [Apply](https://ehac.fa.us6.oraclecloud.com/hcmUI/CandidateExperience/en/sites/CX_1/job/20431) |
| Bosch | Intern, AI Research | Data & ML/AI | Singapore, , Singapore | Python, C++, TensorFlow | Sep 17, 2026 | [Apply](https://jobs.smartrecruiters.com/BoschGroup/744000150014319) |
| Marinabaysands | Intern, Software Quality Assurance | Software | Marina Bay Sands, Singapore | No skills listed | Sep 17, 2026 | [Apply](https://marinabaysands.wd102.myworkdayjobs.com/external/job/Marina-Bay-Sands-Singapore/Inter--Software-Quality-Assurance_JR10006968) |
| Micron Technology | Intern, Facilities AI Engineering | Data & ML/AI | Fab 10N/X, Singapore | Python, LLMs, Tableau | Sep 17, 2026 | [Apply](https://micron.wd1.myworkdayjobs.com/External/job/Fab-10NX-Singapore/Intern--Facilities-AI-Engineering_JR111170) |
| PricewaterhouseCoopers (PwC) | Risk Services - Program Management (AI Hub) Off-Cycle Internship (Jan - Jun 27) | Data & ML/AI | Singapore - Marina One | Java, C++, LLMs | Sep 17, 2026 | [Apply](https://pwc.wd3.myworkdayjobs.com/Global_Campus_Careers/job/Singapore---Marina-One/Risk-Services---AI-Factory-Data-Scientist-Off-Cycle-Internship--Jan---Jun-27-_741281WD) |
| Goventi | C++ Software Engineer Intern (Control) | Software | Singapore | C++, Linux | Sep 16, 2026 | [Apply](https://jobs.ashbyhq.com/goventi/52c162ad-20c4-4db0-ae4f-cc4d1218bc67) |
| Tencent | Backend Development Intern (6 months) | Software | Singapore-CapitaSky | Java, SQL, LLMs, Spring | Sep 15, 2026 | [Apply](https://tencent.wd1.myworkdayjobs.com/Tencent_Careers/job/Singapore-CapitaSky/Backend-Development-Intern--6-months-_R108169) |
| Micron Technology | Intern - NAND Device Engineering AI | Data & ML/AI | Fab 10N/X, Singapore | Python, PyTorch, TensorFlow, scikit-learn | Sep 15, 2026 | [Apply](https://micron.wd1.myworkdayjobs.com/External/job/Fab-10NX-Singapore/Intern---NAND-Device-Engineering-AI_JR112107) |
| Razer | AI Data Engineer Intern | Data & ML/AI | Singapore | Python, SQL, AWS, GCP | Sep 15, 2026 | [Apply](https://razer.wd3.myworkdayjobs.com/Careers/job/Singapore/AI-Data-Engineer-Intern_JR2026007475-1) |
| Bosch | [EAA] Embedded Test Engineer Intern | Software | Ho Chi Minh, , Vietnam | C++ | Sep 14, 2026 | [Apply](https://jobs.smartrecruiters.com/BoschGroup/744000149241480) |
| Hitachi Energy | AI-Driven Cloud/ DevOps Intern | Data & ML/AI | Ho Chi Minh City, Ho Chi Minh, Vietnam | No skills listed | Sep 14, 2026 | [Apply](https://hitachi.wd1.myworkdayjobs.com/hitachi/job/Ho-Chi-Minh-City-Ho-Chi-Minh-Vietnam/AI-Driven-Cloud--DevOps-Intern_R0144780) |
| Tencent | AI Compute Intern | Data & ML/AI | Singapore-CapitaSky | Python, Bash, LLMs, Linux | Sep 14, 2026 | [Apply](https://tencent.wd1.myworkdayjobs.com/Tencent_Careers/job/Singapore-CapitaSky/AI-Compute-Intern_R108149) |
| Tencent | Data Engineer Intern | Data & ML/AI | Singapore-CapitaSky | Python, Java, SQL, Kafka | Sep 14, 2026 | [Apply](https://tencent.wd1.myworkdayjobs.com/Tencent_Careers/job/Singapore-CapitaSky/Data-Engineer-Intern_R108146) |
| Bosch | [BD] Software Test Engineer Intern (6-month Internship) | Software | Thành phố Hồ Chí Minh +2 more | No skills listed | Sep 14, 2026 | [Apply](https://jobs.smartrecruiters.com/BoschGroup/744000149233579) |
| Motorola | Software Engineer Intern _(2 openings)_ | Software | Penang, Malaysia | Python, C++, Linux | Sep 11, 2026 | [Apply](https://motorolasolutions.wd5.myworkdayjobs.com/Careers/job/Penang-Malaysia/Software-Engineer-Intern_R68790) [#2](https://motorolasolutions.wd5.myworkdayjobs.com/Careers/job/Penang-Malaysia/Software-Engineer-Intern_R68829) |
| Razer | AI Engineer Intern | Data & ML/AI | Singapore | Python, LLMs | Sep 11, 2026 | [Apply](https://razer.wd3.myworkdayjobs.com/Careers/job/Singapore/AI-Engineer-Intern_JR2026006947) |
| Razer | Product Developer Intern | Software | Singapore | LLMs, Tableau | Sep 11, 2026 | [Apply](https://razer.wd3.myworkdayjobs.com/Careers/job/Singapore/Product-Developer-Intern_JR2026007822) |
| Mufgub | Cyber Security Architecture & Engineering Intern | Security | Singapore Office OCC | LLMs | Sep 10, 2026 | [Apply](https://mufgub.wd3.myworkdayjobs.com/MUFG-EarlyCareers/job/Singapore-Office-OCC/Cyber-Security-Architecture---Engineering-Intern_10079342-WD) |
| Mufgub | Cyber Security Threat Detection & Incident Response Intern | Security | Singapore Office OCC | Python, LLMs | Sep 10, 2026 | [Apply](https://mufgub.wd3.myworkdayjobs.com/MUFG-EarlyCareers/job/Singapore-Office-OCC/Cyber-Security-Threat-Detection---Incident-Response-Intern_10079338-WD) |
| Thales | Software Engineer Intern | Software | Singapore | Java, TypeScript, Angular, HTML/CSS | Sep 09, 2026 | [Apply](https://thales.wd3.myworkdayjobs.com/careers/job/Singapore/Software-Engineer-Intern_R0339658) |
| Trend Micro | Cybersecurity Intern | Security | Manila | Python | Sep 09, 2026 | [Apply](https://trendmicro.wd3.myworkdayjobs.com/External/job/Manila/Cybersecurity-Intern_R0005760) |
| Trend Micro | Global Infrastructure Services Intern | Software | Manila | No skills listed | Sep 09, 2026 | [Apply](https://trendmicro.wd3.myworkdayjobs.com/External/job/Manila/Global-Infrastructure-Services-Intern_R0009489) |
| Grab | Intern, Software Engineer Mobile | Software | Petaling Jaya, , Malaysia | Python, Java, C++, Swift | Sep 09, 2026 | [Apply](https://jobs.smartrecruiters.com/grab/744000148399141) |
| Intel | System Software Engineering Intern | Software | Malaysia, Kulim | Python, C++ | Sep 09, 2026 | [Apply](https://intel.wd1.myworkdayjobs.com/external/job/Malaysia-Kulim/System-Software-Engineering-Intern_JR0286933) |
| Hewlett Packard (HP) | College Intern - AI Transformation | Data & ML/AI | Singapore, South West, Singapore | No skills listed | Sep 08, 2026 | [Apply](https://hp.wd5.myworkdayjobs.com/ExternalCareerSite/job/Singapore-South-West-Singapore/College-Intern---AI-Transformation_UNI4908-1) |
| Intel | DevOps and Software Engineering Intern | Software | Malaysia, Kulim | Python, Java, C#, JavaScript | Sep 08, 2026 | [Apply](https://intel.wd1.myworkdayjobs.com/external/job/Malaysia-Kulim/DevOps-and-Software-Engineering-Intern_JR0286934) |
| Applied Materials | Customer Engineer - Data Science / ML DevOps Internship | Data & ML/AI | Singapore,SGP | Python | Sep 08, 2026 | [Apply](https://amat.wd1.myworkdayjobs.com/External/job/SingaporeSGP/Customer-Engineer---Data-Science---ML-DevOps-Internship_R2626447) |
| Hewlett Packard Enterprise | AI and Machine Learning Intern | Data & ML/AI | Singapore, Central Singapore, Singapore | LLMs | Sep 08, 2026 | [Apply](https://hpe.wd5.myworkdayjobs.com/Jobsathpe/job/Singapore-Central-Singapore-Singapore/AI-and-Machine-Learning-Intern_1213583) |
| Hewlett Packard Enterprise | Embedded Software (Firmware) Internship | Hardware | Singapore, Central Singapore, Singapore | No skills listed | Sep 08, 2026 | [Apply](https://hpe.wd5.myworkdayjobs.com/Jobsathpe/job/Singapore-Central-Singapore-Singapore/Embedded-Software--Firmware--Internship_1213618) |
| Micron Technology | Intern - STPG PE Firmware | Hardware | MSB, Singapore | Python, C++, LLMs | Sep 08, 2026 | [Apply](https://micron.wd1.myworkdayjobs.com/External/job/MSB-Singapore/Intern---STPG-PE-FIrmware_JR111318) |
| Stripe | Software Engineer, Intern | Software | Singapore | Java, JavaScript, Scala, Ruby | Sep 07, 2026 | [Apply](https://stripe.com/jobs/search?gh_jid=8130883) |
| Intel | Intern System Software Development Engineer | Software | Malaysia, Kulim | Python, C#, SQL, Angular | Sep 07, 2026 | [Apply](https://intel.wd1.myworkdayjobs.com/external/job/Malaysia-Kulim/Intern-System-Software-Development-Engineer_JR0286935) |
| PricewaterhouseCoopers (PwC) | Risk Services - AI Factory Data Scientist Off-Cycle Internship (Jan - Jun 27) | Data & ML/AI | Singapore - Marina One | Python, Java, C++, LLMs | Sep 07, 2026 | [Apply](https://pwc.wd3.myworkdayjobs.com/Global_Campus_Careers/job/Singapore---Marina-One/Risk-Services---AI-Factory-Data-Scientist-Off-Cycle-Internship--Jan---Jun-27-_741280WD) |
| Hitachi Energy | AI-Driven Full Stack Intern | Data & ML/AI | Ho Chi Minh City, Ho Chi Minh, Vietnam | Python, Java, C#, LLMs | Sep 07, 2026 | [Apply](https://hitachi.wd1.myworkdayjobs.com/hitachi/job/Ho-Chi-Minh-City-Ho-Chi-Minh-Vietnam/AI-Driven-Full-Stack-Intern_R0142916) |
| BP | Summer Internship-Technology-Data & AI- Malaysia | Data & ML/AI | Malaysia - Kuala Lumpur | Python, Java, C#, SQL | Sep 07, 2026 | [Apply](https://bpinternational.wd3.myworkdayjobs.com/bpCareers/job/Malaysia---Kuala-Lumpur/Summer-Internship-Technology-Data---AI--Malaysia_RQ115469-2) |
| Thales | Software Development and Integration Engineer (Intern) | Software | Singapore | Java, TypeScript, Angular, HTML/CSS | Sep 04, 2026 | [Apply](https://thales.wd3.myworkdayjobs.com/careers/job/Singapore/Software-Development-and-Integration-Engineer--Intern-_R0339158) |
| Thales | Software Engineer Intern - Middleware (IBS) | Software | Singapore | Java, Swift, Kotlin | Sep 02, 2026 | [Apply](https://thales.wd3.myworkdayjobs.com/careers/job/Singapore/Software-Engineer-Intern---Middleware--IBS-_R0334782) |
| Tower Research Capital | Quantitative Researcher Intern, Bachelor's or Master's | Quant | Singapore, Hong Kong, Shanghai, Sydney | Python, C++, Linux | Sep 01, 2026 | [Apply](https://www.tower-research.com/open-positions/?gh_jid=8168750) |
| Mufgub | Cybersecurity Awareness & Training Intern | Security | Singapore Office OCC | No skills listed | Sep 01, 2026 | [Apply](https://mufgub.wd3.myworkdayjobs.com/MUFG-EarlyCareers/job/Singapore-Office-OCC/Cybersecurity-Awareness---Training-Intern_10078999-WD) |
| Marinabaysands | Intern, Cyber Security | Security | Marina Bay Sands, Singapore | No skills listed | Aug 28, 2026 | [Apply](https://marinabaysands.wd102.myworkdayjobs.com/external/job/Marina-Bay-Sands-Singapore/Intern--Cyber-Security_JR10000208) |
| Marinabaysands | Intern, Developer (Middleware) | Software | Perennial Business City, Singapore | Java, SQL, Spring, Git | Aug 28, 2026 | [Apply](https://marinabaysands.wd102.myworkdayjobs.com/external/job/Perennial-Business-City-Singapore/Intern--Developer--Middleware-_JR10007967) |
| Swift | Site Reliability Engineering (SRE) Intern | Software | Kuala Lumpur, Malaysia | Swift, Tableau | Aug 28, 2026 | [Apply](https://swift.wd3.myworkdayjobs.com/join-swift/job/Kuala-Lumpur-Malaysia/Site-Reliability-Engineering--SRE--Intern_2026-16467) |
| Trend Micro | GRID DEVOPS INTERN | Software | Manila | No skills listed | Aug 27, 2026 | [Apply](https://trendmicro.wd3.myworkdayjobs.com/External/job/Manila/GRID-DEVOPS-INTERN_R0010148) |
| Hitachi Energy | Embedded Engineering Software Internship | Software | Ho Chi Minh City, Ho Chi Minh, Vietnam | C++, Linux | Aug 26, 2026 | [Apply](https://hitachi.wd1.myworkdayjobs.com/hitachi/job/Ho-Chi-Minh-City-Ho-Chi-Minh-Vietnam/Embedded-Internship_R0142038) |
| Jump Trading | Campus AI/ML Researcher (Intern) | Data & ML/AI | Hong Kong; Shanghai; Singapore | Python, C++, PyTorch, TensorFlow | Aug 24, 2026 | [Apply](https://www.jumptrading.com/hr/job?gh_jid=8027938) |
| Western Digital | Intern - AI Information Technology (Studying Master's and Bachelor Degree) | Data & ML/AI | BangPa-in +2 more | Python, Java, C++, C# | Aug 24, 2026 | [Apply](https://jobs.smartrecruiters.com/WesternDigital/744000145156358) |
| Tower Research Capital | Quantitative Developer Intern | Quant | Singapore | Python, C++, Bash, Pandas | Aug 18, 2026 | [Apply](https://www.tower-research.com/open-positions/?gh_jid=8138524) |
| DRW | Software Engineer Intern (Data Engineering) | Data & ML/AI | Singapore | Python, Pandas, Kubernetes, PostgreSQL | Aug 13, 2026 | [Apply](https://job-boards.greenhouse.io/drweng/jobs/8127242) |
| Western Digital | Intern, Firmware Engineering | Hardware | Petaling Jaya, Selangor, Malaysia | Python, C++, Linux | Aug 06, 2026 | [Apply](https://jobs.smartrecruiters.com/WesternDigital/744000141840819) |

---

## Hiring timeline

Internships posted per week, from each role's real published date - redrawn automatically on every run. When this line takes off, recruiting season is open:

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="docs/trends-dark.svg">
  <img alt="Internships posted per week, drawn from real published dates" src="docs/trends-light.svg">
</picture>

## How it stays current

A small Python engine reads public company hiring feeds directly, keeps the roles that match the scope above, de-duplicates across sources, records each role's published date once (so it never shifts), and regenerates this page through GitHub Actions. It polls every company concurrently (async) with retry/backoff and per-host rate limits. The full source is in this repo.

_Engine (last run): 4,356 of 4,651 registered boards returned successfully across 12 ATS platforms (99% of boards attempted, 93% of the full registry) · completed in 980.4s · 613 board(s) returned a capped result set, so their roles were not eligible to be closed this run · employer or source-derived date on 100% of open roles._

## How this list is built

[METHODOLOGY.md](METHODOLOGY.md) documents exactly what every label claims — what separates a stated cycle from an inferred one, what the ✓ H-1B badge does and doesn't mean, how a role gets closed, and which limitations are known. Anything on this page that doesn't match the code is a bug worth reporting.

## Contributing

Adding a company takes one line, see [CONTRIBUTING.md](CONTRIBUTING.md), or just [open a request](../../issues/new?template=add-company.yml) with the board URL. **Spotted something wrong?** [Report the exact field](../../issues/new?template=wrong-data.yml) — wrong country, wrong cycle, closed role, bad sponsorship flag. Those reports usually fix a rule, which fixes every other role too.

Also here: [PRIVACY.md](PRIVACY.md) (what the email list stores — an address and nothing else) · [SECURITY.md](SECURITY.md) · [ARCHITECTURE.md](ARCHITECTURE.md) · [MIT licensed](LICENSE).

Built by one student with AI assistance, in the open. The part that matters isn't who typed it — it's that the rules, the tests, and every run's output are all public and checkable.

## Note on dates

The **Posted** column shows when a role was published, with the newest at the top. I pull the posting date straight from each job portal, but a lot of them don't expose one publicly, so those rows show a dash (—) for now instead of a guessed date. The ones that do publish a date are dated. Know the real date for a dashed role? Open a PR and I'll merge it.

Roles can close at any time, so always confirm on the company's own site before applying.
