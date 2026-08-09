# ScientiaPilot

### From research question to publication.

**ScientiaPilot** is an emerging research publication operating system designed to guide researchers through the complete scholarly workflow — from defining a research question to preparing publication-ready work.

> **Development status:** Active development — M2.5 foundation complete  
> **Current focus:** Dataset Intelligence  
> **Public repository:** Product showcase only  
> **Core implementation:** Private

---

## What is ScientiaPilot?

Scientific research is usually fragmented across many disconnected tools:

- literature databases
- reference managers
- statistical packages
- spreadsheets
- word processors
- plagiarism tools
- journal websites
- supervisor corrections
- institutional formatting requirements

ScientiaPilot is being designed to bring these activities into one guided, auditable research workspace.

The objective is not simply to generate academic text.

The objective is to help researchers move through a structured research lifecycle while preserving:

- reproducibility
- evidence provenance
- statistical integrity
- citation traceability
- document version history
- researcher control

---

# The ScientiaPilot Research Workflow

The current product architecture supports the following research lifecycle:

**01 Research Question**  
↓  
**02 Introduction**  
↓  
**03 Literature & Evidence**  
↓  
**04 Protocol / Study Design**  
↓  
**05 Ethics & Regulatory**  
↓  
**06 Data**  
↓  
**07 Analysis**  
↓  
**08 Results**  
↓  
**09 Discussion & Conclusion**  
↓  
**10 Manuscript Assembly**  
↓  
**11 Integrity & Quality Control**  
↓  
**12 Target Formatting**  
↓  
**13 Publication Preparation**  
↓  
**14 Submission / Revision / Tracking**

The workflow is intentionally **non-linear**.

Researchers may return to earlier stages when:

- supervisors request corrections
- reviewers request revisions
- objectives change
- additional literature is identified
- datasets are corrected
- analyses need to be rerun

ScientiaPilot is intended to preserve the history and impact of those changes rather than silently overwriting previous work.

---

# Current Working Build

## M1 — Application Foundation ✅

Implemented:

- Next.js frontend
- TypeScript
- Tailwind CSS
- FastAPI backend
- live frontend ↔ backend health communication
- branded ScientiaPilot dashboard
- local development environment
- secure Git/GitHub development workflow

---

## M2 — Research Project Workflow ✅

Implemented:

- create a research project from the browser
- FastAPI Project API
- structured Project schemas
- project listing
- project status
- research workflow-stage tracking
- live dashboard project count
- browser → API → application round trip

---

## M2.5 — Persistent Research Projects ✅

Implemented:

- PostgreSQL 16 database
- Docker Compose development environment
- SQLAlchemy ORM
- psycopg PostgreSQL driver
- persistent Project records
- database health monitoring
- Alembic schema migrations
- version-controlled database evolution

Persistence testing has verified:

**Create Project → Store in PostgreSQL → Restart Backend → Retrieve Same Project**

The development database has also been destroyed and successfully rebuilt from Alembic migration history, confirming reproducible schema deployment.

---

# Technology Stack

| Layer | Technology |
|---|---|
| Frontend | Next.js / React / TypeScript |
| Styling | Tailwind CSS |
| Backend API | FastAPI / Python |
| Database | PostgreSQL |
| ORM | SQLAlchemy |
| Database migrations | Alembic |
| PostgreSQL driver | psycopg |
| Development containers | Docker / Docker Compose |
| Source control | Git / GitHub |

Additional services will be introduced as the product develops.

---

# Next Milestone

## M3 — Dataset Intelligence 🚧

The next development phase will enable ScientiaPilot to understand research datasets.

Initial targets include:

- CSV upload
- Microsoft Excel upload
- SPSS `.sav` upload
- dataset metadata extraction
- variable/column detection
- variable labels where available
- data-type recognition
- row and column counts
- missing-data inspection
- dataset versioning
- dataset provenance
- connection of datasets to research projects

Dataset Intelligence will establish the foundation for the future statistical-analysis engine.

---

# Planned Statistical Engine

ScientiaPilot is being designed with its own reproducible statistical engine implemented primarily in Python.

The long-term objective is to provide validated **SPSS-compatible analytical profiles** for supported procedures without requiring researchers to depend on a paid SPSS API.

Planned initial analyses include:

- descriptive statistics
- frequency tables
- chi-square tests
- Fisher's exact test
- independent-samples tests
- odds ratios and confidence intervals
- binary logistic regression
- linear regression
- ROC / AUC analysis
- model-fit statistics
- publication-ready statistical tables

Every analysis is intended to preserve:

- software/library versions
- reference categories
- variable coding
- missing-data rules
- model settings
- analysis specification
- reproducibility information

ScientiaPilot will never claim that IBM SPSS executed an analysis when another statistical engine was actually used.

---

# Research Truth Layer

A central design principle of ScientiaPilot is that manuscript results should originate from approved analytical outputs rather than being invented during writing.

Planned architecture:

**Dataset**  
→ **Analysis Specification**  
→ **Analysis Run**  
→ **Locked Results**  
→ **Results Section**  
→ **Discussion**  
→ **Manuscript**

If an analysis changes, dependent Results and Discussion content can be flagged for review.

---

# Citation & Evidence Layer

Citation management is designed to operate throughout the research process rather than being added only at the end.

ScientiaPilot is planned to maintain a structured internal reference library supporting:

- literature discovery
- DOI / PMID metadata
- source verification
- citation-to-claim linkage
- duplicate detection
- bibliography generation
- journal-specific referencing styles
- EndNote-compatible exchange

Future interoperability may also include other reference-management ecosystems.

---

# Human and Supervisor Intervention

ScientiaPilot is being designed for real-world academic supervision.

Researchers will be able to:

- download work at intermediate stages
- edit manuscripts outside ScientiaPilot
- submit documents to physical supervisors
- upload corrected versions
- preserve document versions
- review requested corrections
- trace changes
- return to earlier workflow stages

The researcher remains the final scientific decision-maker.

---

# Manuscript Portability

ScientiaPilot is planned to support manuscript preparation for multiple destinations from the same underlying research project.

Examples include:

### University / School requirements

Theses, dissertations and institutional research formats.

### Journal requirements

Formatting according to the selected journal's author instructions.

### Examination and professional bodies

Support is planned for structured requirements from postgraduate and professional examination bodies in different countries.

The underlying scientific content should remain reusable while presentation rules change.

---

# Integrity & Quality Control

Planned manuscript-quality controls include:

- citation verification
- reference reconciliation
- similarity / plagiarism reporting
- AI-content assessment where technically supportable
- reporting-guideline checks
- internal numerical consistency checks

Similarity and AI-detection scores will be presented as assessment signals rather than absolute proof of misconduct or authorship.

ScientiaPilot will not provide functionality intended to defeat plagiarism or AI-detection systems.

---

# Research Reconstruction & Reuse

A future advanced capability of ScientiaPilot is being designed around structured reconstruction of research information from existing scholarly outputs.

Potential sources may include:

- published articles
- tables
- statistical outputs
- supplementary material
- available datasets
- legacy research documents

The system will distinguish between:

- original data
- directly recoverable data
- mathematically derived information
- reconstructed aggregate information
- synthetic or indeterminate data

Provenance and reconstruction limitations will be retained.

The goal is to help researchers recover scientifically defensible value from dormant or fragmented research and identify legitimate opportunities for new analyses and research questions.

---

# Usage-Based Commercial Model

ScientiaPilot is being designed around a **credit / unit model** rather than requiring researchers to purchase traditional monthly or annual subscriptions.

Conceptually:

**Research function → Credit cost → User approval → Execution**

Credits will have an internationally consistent base value while payment infrastructure may support appropriate local currencies.

Planned payment-provider abstraction may support services such as:

- Paystack
- PayPal
- additional regional/international gateways

The objective is simple:

> **Researchers pay for research work performed, not for time spent subscribed.**

---

# Publication-Ready Does Not Mean Publication-Guaranteed

ScientiaPilot aims to help researchers produce scientifically rigorous, well-structured and publication-ready scholarly work.

However:

> **ScientiaPilot cannot guarantee acceptance by any journal, university, examination body or publisher.**

Publication decisions remain the responsibility of editors, peer reviewers, institutions and other external authorities.

---

# Development Philosophy

ScientiaPilot is being developed around several principles:

1. **Researcher control**
2. **Scientific reproducibility**
3. **Evidence provenance**
4. **Transparent statistical methods**
5. **Human-supervisor compatibility**
6. **Versioned research artifacts**
7. **Secure handling of research information**
8. **Modular architecture**
9. **Auditable workflows**
10. **No fabricated scientific evidence**

---

# Development Roadmap

| Milestone | Status |
|---|---|
| M0 — Secure development foundation | ✅ Complete |
| M1 — Frontend/backend application shell | ✅ Complete |
| M2 — Research project workflow | ✅ Complete |
| M2.5 — PostgreSQL persistence | ✅ Complete |
| M2.5 — Alembic migrations | ✅ Complete |
| M3 — Dataset Intelligence | 🚧 Next |
| M4 — Research workflow/version engine | Planned |
| M5 — Evidence & citation system | Planned |
| M6 — Statistical engine | Planned |
| M7 — Results & Discussion vertical slice | Planned |
| M8 — Manuscript assembly & formatting | Planned |
| M9 — Credits & payment infrastructure | Planned |
| M10 — Private beta / end-to-end workflow | Planned |

---

# Repository Architecture

This repository is the **public ScientiaPilot showcase**.

It intentionally does **not** contain the proprietary ScientiaPilot application source code, internal algorithms, credentials, research-integrity logic or production infrastructure.

The private development repository remains the engineering source of truth.

This repository exists to document:

- product direction
- verified development milestones
- public screenshots
- demonstrations
- selected architecture concepts
- release progress

---

# Project Status

**ScientiaPilot is under active development and is not currently a production medical or research service.**

Features shown as *planned* or *under development* should not be interpreted as currently available functionality.

---

## ScientiaPilot

### From research question to publication.

**Research. Analyse. Write. Publish.**