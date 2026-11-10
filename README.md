<!-- Editorial profile landing page · banner and portrait are embedded in assets/profile-banner.svg -->

<a href="https://khushi-kundoor.vercel.app/"><img src="assets/bannerGithub.png" alt="Khushi Kundoor — hi, I’m khushi — Software Engineer" width="100%" /></a>

<div align="center">
  <b><a href="#about">about ↓</a> &nbsp; / &nbsp; <a href="#selected-work">selected work ↓</a> &nbsp; / &nbsp; <a href="https://github.com/kkundoor?tab=repositories">all repositories ↗</a> &nbsp; / &nbsp; <a href="https://khushi-kundoor.vercel.app/">personal website ↗</a></b>
</div>

---

## about

I’m Khushi, a software engineer who studied computer science at the University of Michigan. I like building tools that make it easier to find what you’re looking for and understand how you got there.

I’ve worked on software and AI-related projects at **Amazon** and **Intel**. I’m drawn to problems where figuring out what to build matters as much as building it.

**[website ↗](https://khushi-kundoor.vercel.app/)** &nbsp; · &nbsp; **[LinkedIn ↗](https://www.linkedin.com/in/khushi-kundoor)**

---

## selected work

<sub><b>01 / FULL-STACK PLACE RESOLUTION · LLM-ASSISTED EXTRACTION + EVIDENCE-BASED RANKING</b></sub>

### Place Memory

Find the real places in screenshots and notes you saved.

**[try the live demo ↗](https://place-memory-caxs.onrender.com)** &nbsp; · &nbsp; **[view source ↗](https://github.com/kkundoor/place-memory)**

<a href="https://github.com/kkundoor/place-memory"><img src="https://raw.githubusercontent.com/kkundoor/place-memory/main/docs/screenshots/homepage.png" alt="Place Memory resolving a saved location with supporting evidence" width="100%" /></a>

**One lake, two names.** A screenshot said Stow Lake; the map said Blue Heron Lake. I added provider-backed historical names, filtered incompatible candidates, and kept the match explanation visible. The updated resolver identified the correct lake automatically.

**Engineering:** Gemini extracts clues from notes and screenshots; Photon/OSM retrieves place candidates; a separate resolver applies category filters, deduplication, evidence scores, and an abstain/review path. The decision is not delegated to the language model.

<sub>REACT · TYPESCRIPT · FASTAPI · PYTHON · GEMINI · PHOTON/OSM · SQLITE · PYTEST</sub>

[architecture ↗](https://github.com/kkundoor/place-memory/blob/main/docs/architecture.md) &nbsp; · &nbsp; [field test ↗](https://github.com/kkundoor/place-memory/blob/main/docs/field-test-2026-09-17.md) &nbsp; · &nbsp; [evaluations ↗](https://github.com/kkundoor/place-memory#evaluations)

---

<sub><b>02 / RELATIONAL DATA PIPELINE · COHORT STATISTICS + INTERACTIVE ANALYTICS</b></sub>

### Immune Cell Population Analysis

A reproducible analysis of clinical-trial cell counts, from validated CSV data to cohort comparisons and an interactive dashboard.

**Engineering:** Normalizes subjects, samples, and cell counts into SQLite; calculates population frequencies with SQL; aggregates repeated samples at the subject level; compares response groups using Mann–Whitney U tests with Benjamini–Hochberg correction.

<sub>PYTHON · SQLITE/SQL · SCIPY · PANDAS · STREAMLIT · PLOTLY · UNITTEST</sub>

**[open dashboard ↗](https://teiko-immune-cell-dashboard.streamlit.app)** &nbsp; · &nbsp; **[view source + methodology ↗](https://github.com/kkundoor/teiko-technical)**

---

<sub><b>03 / ACCESSIBLE FITNESS APP · RULE-BASED WORKOUT PERSONALIZATION</b></sub>

### eGym

An accessible workout prototype that selects exercises based on mobility, goals, time, and available equipment, with voice guidance and locally saved sessions.

<sub>REACT NATIVE · EXPO · JAVASCRIPT · ASYNCSTORAGE</sub>

[view on my website ↗](https://khushi-kundoor.vercel.app/)

---

<div align="center">
  <sub>MADE BY KHUSHI · <a href="https://khushi-kundoor.vercel.app/">KHUSHI-KUNDOOR.VERCEL.APP</a></sub>
</div>
