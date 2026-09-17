# 🎬 Episode Scripts Archive

> A curated archive for storing episode scripts, source materials, transcripts, and production assets related to **synthetic biology** and **biotech software tools**.

---

## 📁 Purpose

This repository serves as a **version-controlled reference library** for anyone producing educational or research content about the synthetic biology and biotech software ecosystem. It captures:

- **Episode scripts** — structured, modular scripts for audio/video episodes on synbio topics
- **Source materials** — research notes, datasets, presentations, and reference documents
- **Community snapshots** — live surveys of open-source project health, captured from GitHub issue trackers
- **Production assets** — slides, diagrams, recordings, and show notes

The archive is organized so that each episode is self-contained but cross-referenced, enabling reuse of script components and easy navigation for producers, editors, and collaborators.

---

## 🧬 Research Survey: Synbio & Biotech Software Tools

This section summarizes findings from a detailed survey of GitHub-hosted synthetic biology and biotech software projects, including analysis of active open issues to identify what the community is currently concerned about or working on.

### 🏆 Top Projects by Community Activity

| Project | ⭐ Stars | Language | What It Does | Link |
|---|---|---|---|---|
| **synthea** | 3,342 | Java | Synthetic patient population simulator for health analytics & EHR modeling | [synthetichealth/synthea](https://github.com/synthetichealth/synthea) |
| **TDC** | 1,283 | Jupyter | Therapeutics Data Commons — multimodal ML foundation for drug discovery | [mims-harvard/TDC](https://github.com/mims-harvard/TDC) |
| **poly** | 737 | Go | Go package for engineering organisms — codon optimization, primer design, sequence hashing | [bebop/poly](https://github.com/bebop/poly) |
| **DnaChisel** | 281 | Python | Versatile DNA sequence optimizer — codon optimization, GC tuning, constraint satisfaction | [Edinburgh-Genome-Foundry/DnaChisel](https://github.com/Edinburgh-Genome-Foundry/DnaChisel) |
| **awesome-synthetic-biology** | 223 | — | Curated directory of synbio projects, articles, and resources | [websemantics/awesome-synthetic-biology](https://github.com/websemantics/awesome-synthetic-biology) |
| **GENtle2** | 106 | JavaScript | Web-based DNA editor for synthetic biology | [Synbiota/GENtle2](https://github.com/Synbiota/GENtle2) |
| **act (20n)** | 92 | Java/Scala | Predictive bioengineering — discovers DNA routes to make target chemicals | [20n/act](https://github.com/20n/act) |
| **SynBioHub** | 84 | JavaScript/Java | Web platform for browsing, uploading & sharing synthetic biology designs | [SynBioHub/synbiohub](https://github.com/SynBioHub/synbiohub) |
| **iBioSim** | 67 | Java | CAD for genetic circuits; SBML/SBOL support | [MyersResearchGroup/iBioSim](https://github.com/MyersResearchGroup/iBioSim) |
| **ART (JBEI)** | 66 | Jupyter Notebook | ML tool for automated strain engineering recommendations | [JBEI/ART](https://github.com/JBEI/ART) |
| **Coral** | 32 | Python | Library & framework for specifying synthetic biology design processes | [klavinslab/coral](https://github.com/klavinslab/coral) |
| **ClothoBiofabEdition** | 9 | Java | Synthetic Biology Computer-Aided Design tool | [BIOFAB/ClothoBiofabEdition](https://github.com/BIOFAB/ClothoBiofabEdition) |

---

### 🔬 Deep Dives — Most Active Repos & Their Open Issues

#### 1. SynBioHub (84 ⭐) — The Interoperability Hub

**Scope:** Web application enabling users and software to browse, upload, and share synthetic biology designs. Hosts the iGEM Registry of Standard Biological Parts and enriched *B. subtilis* and *E. coli* data. Stack: JavaScript (Node.js) + Java (Maven) + OpenLink Virtuoso (RDF triplestore). BSD-2-Clause license. PR-based development with CI (Travis + Docker integration tests via SBOLTestSuite); automatic Docker Hub publishing via GitHub Actions.

**Current Open Issues (Milestone SBH 1.6.2):**

| Issue | Title | Theme | Date |
|---|---|---|---|
| [#1756](https://github.com/SynBioHub/synbiohub/issues/1756) | SubCollections does not report members in public graph | Bug — data integrity | Sep 2026 |
| [#1755](https://github.com/SynBioHub/synbiohub/issues/1755) | Recursive download does not follow linked collections | Bug — workflow gap | Aug 2026 |
| [#1754](https://github.com/SynBioHub/synbiohub/issues/1754) | Legacy data in Virtuoso should be deleted | Maintenance — tech debt | Aug 2026 |
| [#1753](https://github.com/SynBioHub/synbiohub/issues/1753) | OMEX download missing SBML file attachments | Bug — export completeness | Aug 2026 |
| [#1752](https://github.com/SynBioHub/synbiohub/issues/1752) | Private→public visibility shifts URL prefix | Bug — deployment friction | Aug 2026 |
| [#1746](https://github.com/SynBioHub/synbiohub/issues/1746) | Incremental updates not working with SBOLExplorer | Bug — tool integration | Jul 2026 |
| [#1744](https://github.com/SynBioHub/synbiohub/issues/1744) | Backend lacks OR request parsing mechanism | Bug — query capability | Jul 2026 |

**Takeaway:** The community is **seriously focused on data portability and interoperability**. OMEX bundle integrity, recursive collection resolution, and database hygiene are the pain points. This signals the ecosystem is maturing — users need dependable data pipelines.

---

#### 2. iBioSim (67 ⭐) — The CAD Tool Striving for Modern Compatibility

**Scope:** Computer-aided design (CAD) tool for modeling, analysis, and design of genetic circuits. Imports/exports SBML (all levels/versions) and supports SBOL. Includes multi-cellular and spatial modeling support. Active developers: Lukas Buecherl, Pedro Fontanarrosa, Chris Myers. Apache-2.0 license. Stack: Java + libSBML + reb2sac + GeneNet + Yosys.

**Current Open Issues:**

| Issue | Title | Theme | Date |
|---|---|---|---|
| [#640](https://github.com/MyersResearchGroup/iBioSim/issues/640) | A Java exception has occurred | Stability / runtime | Aug 2025 |
| [#639](https://github.com/MyersResearchGroup/iBioSim/issues/639) | Can't upload SynBioHub design | Integration failure | May 2025 |
| [#638](https://github.com/MyersResearchGroup/iBioSim/issues/638) | Unable to run iBioSim 3.2.0 on Mac | Cross-platform | May 2025 |
| [#637](https://github.com/MyersResearchGroup/iBioSim/issues/637) | Unable to generate models (NoClassDefFoundError: Apache Jena/Xerces) | Bug — Java dependency | Jan 2025 |
| [#635](https://github.com/MyersResearchGroup/iBioSim/issues/635) | Cannot open iBioSim on Windows 11 | Cross-platform | Jan 2025 |
| [#632](https://github.com/MyersResearchGroup/iBioSim/issues/632) | Can't connect to LCP Synbiohub | Integration failure | Apr 2024 |

**Key error from #637 (most discussed):**
```
java.lang.NoClassDefFoundError: Could not initialize class org.apache.jena.query.ARQ
Caused by: java.lang.NoClassDefFoundError: org/apache/xerces/util/XMLChar
```
A transitive dependency conflict — Apache Jena can't initialize because Xerces is missing or conflicting.

**Takeaway:** Desktop-based synbio CAD tools struggle with **Java dependency management and OS-specific behavior**. This signals a strong opportunity for containerized or web-based alternatives.

---

#### 3. GENtle2 (106 ⭐) — The Web DNA Editor With Legacy Debt

**Scope:** Web-based DNA editor for synthetic biology. A re-think of the original GENtle desktop application for the web. Written in JavaScript (Node.js + Express + Gulp).

**Current Open Issues (organized under "Refactor — Canvas events & RES/annotation cards" milestone):**

| Issue | Title | Theme | Date |
|---|---|---|---|
| #164 | Display feature details when hovering | UI / Refactor | Jul 2023 |
| #163 | Tracking mouse events in `Artist` | Feature / Refactor | Jul 2023 |
| #162 | Selection disappears when copied via context menu | Bug | Jul 2023 |
| #161 | Selection disappears with hotkeys without shift | Bug | Jul 2023 |
| #159 | Tracking shapes in `Artist` | Feature / Refactor (6 comments) | Jul 2023 |
| #158 | Creating a feature clears plasmid map but doesn't redraw | Bug / Refactor | Jul 2023 |

**Takeaway:** GENtle2's issues trace back to 2014-era interaction bugs that persist in the backlog. The refactor milestone signals the maintainer is attempting a **clean-slate architecture** rather than patching the old codebase — a story worth telling about technical debt in scientific software.

---

#### 4. DnaChisel (281 ⭐) — The Python-First DNA Optimizer

**Scope:** Python library for optimizing DNA sequences with respect to constraints and objectives. 15+ classes of sequence specifications: codon-optimization, GC-content tuning, restriction site avoidance, homology removal, and more. Part of the EGF Codons suite from the Edinburgh Genome Foundry.

**Current Open Issues:**

| Issue | Title | Theme |
|---|---|---|
| [#114](https://github.com/Edinburgh-Genome-Foundry/DnaChisel/issues/114) | Produce multiple different optimized results | Feature — diversity in output |
| [#113](https://github.com/Edinburgh-Genome-Foundry/DnaChisel/issues/113) | Low Codon Adaptation Index on optimized sequence | Bug — optimization quality |
| [#107](https://github.com/Edinburgh-Genome-Foundry/DnaChisel/issues/107) | Support for Uridine Depletion (UD) optimization | Feature — new target (5 comments) |
| [#111](https://github.com/Edinburgh-Genome-Foundry/DnaChisel/issues/111) | Unexpected Mutation of `codon_usage_table` During Optimization | Bug — data integrity |
| [#100](https://github.com/Edinburgh-Genome-Foundry/DnaChisel/issues/100) | How to get under-optimal sequences during optimization? | Question — fitness landscape |

**Takeaway:** Users want to **explore the fitness landscape**, not just find the single best sequence. The `codon_usage_table` mutation bug (#111) is concerning because it could silently produce incorrect optimization results. This has direct implications for episodes about "optimal vs. good enough" in biological sequence design.

---

#### 5. Coral (32 ⭐) — Design-as-Code for Synthetic Biology

**Scope:** Python library for encoding the process of designing synthetic DNA constructs. Mirrors traditional GUI-based design steps (ApE, j5, Benchling) as operations on data structures. Enables iterative design through analysis modules. MIT license. Stack: Python (works with PyPy + numpy), Biopython.

**Current Open Issues:** Only 1 open issue ([#37](https://github.com/klavinslab/coral/issues/37) — Ubuntu 22.04 Python 3 compatibility). Actively maintained, recent updates (June 2026).

**Takeaway:** Coral is a rare example of a **well-maintained, open-source Python library** for synbio design automation. It's a great reference for how to structure design-as-code workflows.

---

### 📊 Emerging Themes from the Community

Based on open-issue triage across all surveyed projects, these are the themes dominating community attention right now:

| # | Theme | What It Means |
|---|---|---|
| 1 | **Interoperability & integration friction** | iBioSim can't upload to SynBioHub; OMEX exports miss SBML files; collection prefixes shift when changing visibility. The connected synbio toolchain is still hampered by format/URL/API mismatches. |
| 2 | **Data integrity in shared collections** | SubCollections not reporting members, recursive downloads not following links, legacy DB data piling up. Growing-pains for platforms hosting community-wide design registries. |
| 3 | **Long-standing UI bugs in academic tools** | GENtle2's 2014-era interaction bugs remain unfunded; SynBioCAD/biocad's 2019-era UI issues persist. A common pattern in academic tools that lose active maintainers. |
| 4 | **Cross-platform compatibility** | iBioSim's Mac and Windows 11 issues, TDC's Windows pip install failures. Java "write once, run anywhere" remains aspirational. |
| 5 | **Optimization depth vs. usability** | DnaChisel users want to explore sub-optimal solutions (fitness landscapes), not just get the single best answer. A fundamental UX challenge in computational biology. |
| 6 | **Modern language adoption** | The success of **poly** (Go, 737⭐) and **DnaChisel** (Python, 281⭐) vs. aging Java tools (iBioSim, GENtle2) suggests the community is gravitating toward modern, fast, easy-to-deploy languages. |
| 7 | **ML + sequence design convergence** | ART's ML for strain engineering, iBioSim's circuit design, TDC's therapeutic benchmarks, and the broader ecosystem point to an accelerating intersection of ML and biological design automation. |
| 8 | **Stalled academic projects** | BiArkit, BIOFAB Studio, and SynBioCAD/biocad all show signs of dormancy. The "publish and abandon" pattern is prevalent in university synbio software. |

---

## 📂 Archive Structure

```
episode-scripts-archive/
├── episodes/
│   ├── EP001-interoperability-crisis/     # The SynBioHub data-portability story
│   ├── EP002-desktop-tool-bottleneck/     # iBioSim & GENtle2 cross-platform struggles
│   ├── EP003-from-hand-engineering-to-ml/ # ART, 20n/act, and computational design
│   ├── EP004-dna-optimization-deep-dive/  # DnaChisel, poly, and sequence design
│   ├── EP005-standards-maturation/        # SBOL, SBML, and the state of interoperability
│   ├── EP006-academic-tool-dormancy/      # The "publish and abandon" pattern
│   └── ...
├── research/
│   ├── synbio-tools-survey-2026-09.md     # Full survey data
│   ├── community-issues-snapshot-2026-09.md # Curated issue list
│   └── references/
├── source-materials/
│   ├── presentations/
│   ├── datasets/
│   └── tooling-context/
├── scripts/
│   ├── episode-template.md
│   └── show-notes-template.md
├── production-assets/
│   ├── slides/
│   ├── diagrams/
│   └── recordings/
└── README.md
```

---

## 🔗 Key Resources & Communities

### Tools & Platforms

| Resource | Link | Description |
|---|---|---|
| [SynBioHub](https://synbiohub.org) | [SynBioHub/synbiohub](https://github.com/SynBioHub/synbiohub) | Design repository & sharing platform |
| [iBioSim](http://www.ibiosim.org/) | [MyersResearchGroup/iBioSim](https://github.com/MyersResearchGroup/iBioSim) | Genetic circuit CAD tool |
| [DnaChisel](https://edinburgh-genome-foundry.github.io/DnaChisel/) | [EGF/DnaChisel](https://github.com/Edinburgh-Genome-Foundry/DnaChisel) | Python DNA sequence optimizer |
| [poly](https://github.com/bebop/poly) | [bebop/poly](https://github.com/bebop/poly) | Go package for engineering organisms |
| [GENtle2](https://synbiota.com) | [Synbiota/GENtle2](https://github.com/Synbiota/GENtle2) | Web-based DNA editor |
| [Coral](https://github.com/klavinslab/coral) | [klavinslab/coral](https://github.com/klavinslab/coral) | Synbio design-as-code framework |
| [act](https://github.com/20n/act) | [20n/act](https://github.com/20n/act) | Predictive bioengineering platform |
| [TDC](https://tdcommons.ai) | [mims-harvard/TDC](https://github.com/mims-harvard/TDC) | Therapeutics Data Commons |
| [Synthea](https://synthetichealth.github.io/synthea/) | [synthetichealth/synthea](https://github.com/synthetichealth/synthea) | Synthetic patient simulator |

### Standards & Registries

| Resource | Link |
|---|---|
| [SBOL Specification](https://sbolstandard.org/) | [SynBioDex/SBOL-specification](https://github.com/SynBioDex/SBOL-specification) |
| [libSBOLj](https://github.com/SynBioDex/libSBOLj) | Java library for SBOL |
| [SBML](https://sbml.org/) | Systems Biology Markup Language |
| [iGEM Registry](http://parts.igem.org) | Standard Biological Parts |
| [BioModels](https://www.ebi.ac.uk/biomodels) | Database of mathematical models |

### Communities & Curated Lists

| Resource | Link | Stars |
|---|---|---|
| [awesome-synthetic-biology](https://github.com/websemantics/awesome-synthetic-biology) | Websemantic's curated list | 223 |
| [awesome-deep-learning-4-life-sciences](https://github.com/virtualramblas/awesome-deep-learning-4-life-sciences) | DL resources for biotech & pharma | 167 |
| [Learn_Synthetic_Biology](https://github.com/llSourcell/Learn_Synthetic_Biology) | Educational resources for synbio | 157 |
| [Biotech-Job-Search-Engine](https://github.com/dportik/Biotech-Job-Search-Engine) | Open-source biotech job discovery | 81 |

### Organizations to Follow

- **SynBioHub** — Primary design-sharing platform & SBOL standards
- **SynBioDex** — SBOL specification & related tools
- **Edinburgh Genome Foundry** — DnaChisel & EGF Codons suite
- **Myers Research Group** — iBioSim (academic CAD tool)
- **JBEI** — ART for strain engineering
- **20n** — Commercial bioengineering (act platform)
- **Autodesk Bio/Nano/Protospace** — Wet-lab protocol automation
- **klavinslab** — Coral design framework
- **BIOFAB** — Early web-based synbio CAD tools

---

## 📝 Contributing

Contributions are welcome! To add materials:

1. Fork this repository
2. Create a new branch for your episode or addition (`git checkout -b ep-episode-XXX-topic`)
3. Add your script, source materials, or transcript under the appropriate directory
4. Update the research survey if you've surveyed new projects or issues
5. Submit a pull request with a clear description of your additions

### Naming Conventions

- Episode directories: `EPXXX-short-descriptive-title/` (zero-padded, sequential)
- Script files: `script.md` (primary), `show-notes.md` (supplementary)
- Research files: `topic-year-month.md` (e.g., `interoperability-2026-09.md`)
- Assets: place in `production-assets/` with descriptive filenames

---

## 📜 License

This archive is released under the [Creative Commons Attribution 4.0 International License](http://creativecommons.org/licenses/by/4.0/), same as the awesome-synthetic-biology list. Individual episode scripts may carry their own licenses — check each episode directory for details.

---

*Last research update: September 2026 — Surveyed 15+ GitHub projects, reviewed 30+ open issues, compiled community themes across the synthetic biology & biotech software ecosystem.*
