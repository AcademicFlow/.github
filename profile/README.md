<p align="center">
  <img src="https://avatars.githubusercontent.com/u/271215497?s=200&v=4" alt="AcademicFlow" width="100" />
</p>

<h1 align="center">AcademicFlow</h1>

<p align="center">
  <strong>Intelligente Forschung. Souveräne Daten.</strong><br/>
  Privacy-first citation verification for academic writing — powered by on-device AI.
</p>

<p align="center">
  <a href="https://academicflow.studio">Website</a>
</p>

---

**AcademicFlow** is a Microsoft Word Add-in that verifies citations, detects unsupported claims, discovers sources, and checks formatting in university theses — while keeping thesis text local and private.

### How it works

| Stage | What it does |
|-------|-------------|
| **Document Understanding** | Extracts paragraphs, classifies sections, detects claims — all client-side |
| **Claim Classification** | Subtypes claims and extracts qualifiers via cloud LLM |
| **Citation Verification** | Validates citations against CrossRef, OpenAlex, DNB with 21 fabrication signals |
| **Source Search** | Discovers relevant sources with bilingual retrieval and reranking |
| **Claim-Source Alignment** | Matches claims to evidence passages with NLI verdicts |
| **Format Verification** | Checks styles, fonts, spacing, headings, and citation format consistency |

### Repositories

| Repo | Purpose |
|------|---------|
| [academicflow-spec](https://github.com/AcademicFlow/academicflow-spec) | Product specification, ADRs, and research |
| [academicflow-addin](https://github.com/AcademicFlow/academicflow-addin) | Word add-in (TypeScript, Preact, Office.js) |
| [academicflow-web](https://github.com/AcademicFlow/academicflow-web) | Marketing website (Next.js, Sanity CMS) |
| [academicflow-brand](https://github.com/AcademicFlow/academicflow-brand) | Brand guidelines, logo, and presentation |

---

<p align="center">
  <sub>Die erste KI-Schreibassistenz für den DACH-Raum &mdash; <a href="https://academicflow.studio">academicflow.studio</a></sub>
</p>
