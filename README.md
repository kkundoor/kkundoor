<!-- Portfolio source of truth: https://khushi-kundoor.vercel.app/ -->

<a href="https://khushi-kundoor.vercel.app/"><img src="assets/KhushiGitPortfolioBanner.png" alt="Khushi Kundoor — hi, I'm Khushi — Software Engineer" width="100%" /></a>

<div align="center">
  <b><a href="#about">about ↓</a> &nbsp; / &nbsp; <a href="#work-experience">work experience ↓</a> &nbsp; / &nbsp; <a href="#projects">projects ↓</a> &nbsp; / &nbsp; <a href="https://khushi-kundoor.vercel.app/">website ↗</a> &nbsp; / &nbsp; <a href="https://github.com/kkundoor?tab=repositories">repositories ↗</a></b>
</div>

---

## about

I’m Khushi, a computer science graduate from the University of Michigan. I like building useful software and figuring out the technical decisions behind it → especially where AI interfaces meet real data and user workflows.

My recent projects have pushed me to think more deliberately about **context boundaries, evaluation, failure handling, and what should stay deterministic**. [More about me ↗](https://khushi-kundoor.vercel.app/) · [LinkedIn ↗](https://www.linkedin.com/in/khushi-kundoor)

---

## Work Experience

<sub><b>01 / LLM TOOL INTEGRATION · MCP · CONTEXT-EFFICIENT DATA RETRIEVAL</b></sub>

### Amazon — Software Development Engineer Intern

**QueryQuencher** · TypeScript · AWS · Amazon Q · Model Context Protocol (MCP)

Built an internal natural-language investigation workflow for engineers navigating complex contract-processing systems.

- Connected the LLM interface to operational tooling through **MCP**, making data from workflows involving 20+ services easier to investigate.
- Reworked the data path when full responses (~100 KB to 10 MB+) overwhelmed memory and model context: **summary-first retrieval, selective deeper inspection, and incremental processing** instead of sending everything to the model.
- Reduced representative analysis effort from **150 to 45 hours per cycle (~70%)** in a workflow supporting 300+ monthly users.

**Engineering focus:** tool-backed LLM workflows, context selection, API/service integration, large-response processing, iterative validation. *This is MCP/tool retrieval, not a claimed vector-embedding RAG implementation.*

---

<sub><b>02 / PYTHON AUTOMATION · DATA ACCESS · LLM EVALUATION · COMPUTER VISION</b></sub>

### Intel — Software Engineering Intern

Worked on distinct internal engineering projects spanning:

- **Data and manufacturing automation:** Python workflows, preprocessing, and data integration to reduce repetitive engineering tasks; estimated **15% efficiency improvement**.
- **Natural-language data access:** A Python-based internal chatbot/service connecting user requests with engineering information; estimated **760 hours saved annually**.
- **LLM experimentation:** A Python web interface for exploring prompt and model outputs with Microsoft Prompt Flow.
- **Computer vision and robotics:** Image annotation and evaluation work supporting a Boston Dynamics robot inspection initiative; the broader effort targeted **$6.9M in five-year savings**.

**Engineering focus:** Python, SQL/data access, APIs, automation, prompt evaluation, computer-vision workflows.

---

## Projects

<sub><b>01 / FULL-STACK CLOUD-DEPLOYED APP · MULTIMODAL EXTRACTION + DETERMINISTIC PLACE RESOLUTION</b></sub>

### Place Memory

Find the real places in screenshots and notes you saved.

**[live demo ↗](https://place-memory-caxs.onrender.com)** · **[source ↗](https://github.com/kkundoor/place-memory)**

<a href="https://github.com/kkundoor/place-memory"><img src="https://raw.githubusercontent.com/kkundoor/place-memory/main/docs/screenshots/homepage.png" alt="Place Memory demo" width="100%" /></a>

**System design:** React/TypeScript UI → FastAPI endpoints → Gemini clue extraction → Photon/OSM candidate search with Nominatim fallback → explicit ranking and confidence gates → SQLite memory storage in local mode. The public Render demo runs the pipeline without saving visitor inputs or results.

**Context and trust:** The model extracts names, locations, and clues, but does **not** decide canonical identity. Provider results are normalized, filtered by category, deduplicated, scored against evidence, and routed to **resolve / human review / abstain**. Candidate provenance and score components stay inspectable.

**What changed through testing:** A Stow Lake screenshot exposed a renamed-place alias and incompatible road results. I added provider-backed historical names and stronger candidate filtering. Separate synthetic and field regression checks track ranking and **false automatic resolutions**, rather than relying on a convincing demo alone. Later live-provider failures led to explicit fallback behavior.

<sub>REACT · TYPESCRIPT · FASTAPI · PYTHON · GEMINI · PHOTON/OSM · SQLITE · PYTEST · GITHUB ACTIONS · RENDER</sub>

[architecture ↗](https://github.com/kkundoor/place-memory/blob/main/docs/architecture.md) · [field test ↗](https://github.com/kkundoor/place-memory/blob/main/docs/field-test-2026-09-17.md) · [evaluation ↗](https://github.com/kkundoor/place-memory#evaluations) · [design decisions ↗](https://github.com/kkundoor/place-memory/blob/main/docs/decisions.md)

---

<sub><b>02 / RELATIONAL DATA PIPELINE · COHORT ANALYSIS + STATISTICAL DASHBOARD</b></sub>

### Immune Cell Population Analysis

A reproducible CSV → SQLite → analytics → Streamlit workflow for comparing clinical-trial immune-cell populations.

**System design:** Python validation and normalized `subjects`, `samples`, `cell_counts` tables; SQL joins and sample-level frequencies; per-subject aggregation before responder/non-responder comparisons; Mann–Whitney U tests with Benjamini–Hochberg false-discovery correction. Streamlit and Plotly expose the results for inspection. A 27-test suite covers validation, calculations, and cohort filters.

<sub>PYTHON · SQLITE/SQL · SCIPY · PANDAS · STREAMLIT · PLOTLY · UNITTEST</sub>

**[dashboard ↗](https://teiko-immune-cell-dashboard.streamlit.app)** · **[source + methodology ↗](https://github.com/kkundoor/immune-cell-analysis-dashboard)**

---

<sub><b>03 / ACCESSIBLE MOBILE APP · RULE-BASED PERSONALIZATION</b></sub>

### eGym

An Expo/React Native prototype that selects workout routines from mobility, goals, time, and equipment constraints, with spoken exercise instructions and session history stored locally.

<sub>REACT NATIVE · EXPO · JAVASCRIPT · ASYNCSTORAGE</sub>

The prototype uses mock sign-in. The source repository is private.

[read the case study ↗](https://khushi-kundoor.vercel.app/#egym)

---

**On the engineering tradeoffs:** Place Memory uses SQLite and lightweight application caching today; it **does not use Redis, a vector database, or embedding-based RAG**. Those would be justified by measured latency, concurrency, or retrieval-quality needs—not added for a technology checklist. The clearest recent development work has been improving evaluation, provenance, API boundaries, deployment reliability, and provider fallbacks.

<div align="center">
  <sub><a href="https://khushi-kundoor.vercel.app/">KHUSHI-KUNDOOR.VERCEL.APP</a> · <a href="https://github.com/kkundoor?tab=repositories">ALL REPOSITORIES</a></sub>
</div>
