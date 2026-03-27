# [TRansparent, sUStainable and Transferable (TRUST) best-practice guidelines for visual word recognition research](https://trust-guidelines-v01.readthedocs.io/en/latest/)

> **Version:** v02 — Guideline version after three rounds of expert feedback, including importance ratings 
> **Published docs:** [trust-network-guidelines-v01.readthedocs.io](https://trust-guidelines-v01.readthedocs.io/en/latest/)

---

## About

This repository contains the living guideline document open for everyone to fork and adapt for a differen language, group, task or measurement method. 

The documentation is built with [MkDocs](https://www.mkdocs.org/) using the Material theme and is automatically deployed to ReadTheDocs.

---

## Adapting the Guidelines to a Different Language

The guidelines were developed specifically for **German single-word lexical decisions** including a expert importance rating. When forking this repository for a different target language (e.g., English, French, Dutch), the following content must be reviewed and adapted throughout all pages (`docs/*.md`). Furthermore, it would be advised to collect importance ratings and feedback from reading researchers working in the field/language.

### Repository Structure

```
trust-network-guidelines-v02/
├── docs/
│   ├── index.md          # Home / Overview
│   ├── procedure.md      # Procedural guidelines
│   ├── materials.md      # Materials guidelines
│   ├── analysis.md       # Analysis guidelines
│   └── reporting.md      # Reporting guidelines
├── admin/                # Administrative files
├── mkdocs.yml            # MkDocs site configuration
├── .readthedocs.yml      # ReadTheDocs build configuration
├── requirements.txt      # Python dependencies
└── readme.md             # This file
```

### Materials (`materials.md`)

- **Word resources** — Psycholinguistic corpora (e.g., SUBTLEX-DE, dlexDB) are specific to German. These **must** be replaced with the equivalent resources for the target language (e.g., SUBTLEX-US/UK for English, LEXIQUE for French, SUBTLEX-NL for Dutch).

### Analysis (`analysis.md`)

- **Language-specific covariates** — control variables such as word length effects, syllable structure, or stress assignment interact differently across languages and may need to be added, removed, or reweighted in analysis pipelines.

---

## Technical Setup for Adaptation

| File | What to change |
|---|---|
| `mkdocs.yml` → `site_name` | Replace with your network's name |
| `mkdocs.yml` → `theme.language` | Add e.g. `language: en` to enable MkDocs Material's built-in UI translations |
| `mkdocs.yml` → `theme.font` | Roboto covers Latin scripts well; swap for a different web font if targeting non-Latin scripts (CJK, Arabic, Devanagari, etc.) |
| `docs/stylesheets/extra.css` | Add `direction: rtl` for right-to-left languages |
| `.readthedocs.yml` | Update the ReadTheDocs project slug to match your new project |
| `readme.md` | Update "Forked from", version label, and network description |

