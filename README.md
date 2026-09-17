# 🎬 Episode Scripts Archive

A curated archive for storing episode scripts and associated source materials (research notes, references, tooling context, and community discussions). This repository is organized for version-controlled collaboration on audiovisual and written episode content.

---

## 📁 Repository Purpose

- **Centralize** episode scripts, show notes, source materials, and production assets in a single, version-controlled location
- **Preserve** content history through Git's branching and commit tracking
- **Collaborate** by providing a clear workflow for writers, editors, producers, and guests
- **Enable reuse** — modular script components can be repurposed across episodes
- **Document provenance** — every edit and contributor is tracked
- **Anchor research** — each episode's notes tie back to real, live open-source projects and the concerns bubbling up in their issue trackers

---

## 🔬 Synthetic Biology & Biotech Software Tools (Research Survey)

This archive keeps a running snapshot of the GitHub-based **synthetic biology (synbio)** and **biotech software** ecosystem, with a live eye on each project's open issues. The projects below were surveyed as part of episode research, with several investigated in depth.

### 🏆 Synthesized Landscape (key synbio & biotech tools found on GitHub)

| Project | Stars | Language | What it does |
|---|---|---|---|
| [synthetichealth/synthea](https://github.com/synthetichealth/synthea) | 3,342 | Java | Synthetic patient population simulator for health analytics & EHR modeling |
| [mims-harvard/TDC](https://github.com/mims-harvard/TDC) | 1,283 | Jupyter Notebook | Therapeutics Data Commons — multimodal ML foundation for drug discovery |
| [websemantics/awesome-synthetic-biology](https://github.com/websemantics/awesome-synthetic-biology) | 223 | (list) | Curated directory of synbio projects, articles, and resources |
| [virtualramblas/awesome-deep-learning-4-life-sciences](https://github.com/virtualramblas/awesome-deep-learning-4-life-sciences) | 167 | — | Curated list of deep-learning resources for biotech & pharma |
| [Synbiota/GENtle2](https://github.com/Synbiota/GENtle2) | 106 | JavaScript | Web-based DNA editor for synthetic biology |
| [chaibio/chaipcr](https://github.com/chaibio/chaipcr) | 96 | C++ | Software behind Chai's open-source Real-Time PCR instrument |
| [20n/act](https://github.com/20n/act) | 92 | Java | Predictive bioengineering — discovers DNA routes to make target chemicals |
| [SynBioHub/synbiohub](https://github.com/SynBioHub/synbiohub) | 84 | JavaScript | Web platform for browsing, uploading & sharing synthetic biology designs |
| [dportik/Biotech-Job-Search-Engine](https://github.com/dportik/Biotech-Job-Search-Engine) | 81 | Python | Open-source job-discovery for biotech, genomics & bioinformatics roles |
| [JBEI/ART](https://github.com/JBEI/ART) | 66 | Jupyter Notebook | ML tool to improve strain engineering effectiveness |
| [MyersResearchGroup/iBioSim](https://github.com/MyersResearchGroup/iBioSim) | 67 | Java | CAD for genetic circuits; SBML/SBOL support |
| [Autodesk/bionano-wetLabAccelerator](https://github.com/Autodesk/bionano-wetLabAccelerator) | 32 | JavaScript | Designs robotic wet-lab protocols via visual UI (no coding) |
| [klavinslab/coral](https://github.com/klavinslab/coral) | 32 | Python | Library & framework for specifying synbio design processes |
| [SynBioDex/libSBOLj](https://github.com/SynBioDex/libSBOLj) | 43 | Java | Java library for the Synthetic Biology Open Language (SBOL) |
| [Gardner-BinfLab/TISIGNER-ReactJS](https://github.com/Gardner-BinfLab/TISIGNER-ReactJS) | 30 | JavaScript | TISIGNER: interactive synbio design tool |
| [KOSASIH/ecobio-remediatech-core](https://github.com/KOSASIH/ecobio-remediatech-core) | 26 | Python | EcoBio Remediatech — environmental bioengineering algorithms |
| [SynBioCad/biocad](https://github.com/SynBioCAD/biocad) | 16 | JavaScript | Web-based CAD tool for synthetic biology built on SBOL standard |
| [BIOFAB/ClothoBiofabEdition](https://github.com/BIOFAB/ClothoBiofabEdition) | 9 | Java | Synthetic Biology Computer-Aided Design tool |

---

### 🧬 In-Depth Investigation (active repos, open issues reviewed)

#### synthetichealth/synthea — Synthetic Patient Population Simulator (3,342 ⭐)

The largest and most active project in this survey. Synthea generates synthetic patient populations and corresponding electronic health records (EHRs) for research, benchmarking, and software testing. It models demographics, comorbidities, medications, labs, and clinical encounters using a modular, parameterized architecture.

**Recent open issues (as of September 2026):**

| Issue | Summary | Theme |
|---|---|---|
| #1700 | Proposal: stable de-identified export manifest for downstream benchmarks | Feature — standardization for benchmarking |
| #1703 | CSV SYSTEM column depends on whether FHIR export is enabled | Bug — data consistency across export formats |
| #1702 | FHIR R4 allergy export loses reaction severity by mutating a HashMap key | Bug — data corruption in FHIR export |
| #1365 | US Core 3.1 | Feature — compliance with latest US Core FHIR spec |

**Takeaway:** Synthea's issues reveal a community focused on **data consistency across export formats** (CSV vs FHIR), **standardization for benchmarking** (stable export manifests), and **regulatory compliance** (US Core 3.1). The HashMap key mutation bug (#1702) is particularly concerning — it silently corrupts allergy reaction severity data in FHIR R4 exports, which could affect downstream clinical research. The relatively small number of open issues (4) vs. the project's massive adoption (3,342 stars) suggests a small, efficient maintainer team, but also potentially thin coverage for edge cases.

---

#### mims-harvard/TDC — Therapeutics Data Commons (1,283 ⭐)

The largest AI-for-drug-discovery project in this survey. TDC is a coordinated initiative to access and evaluate AI capability across therapeutic modalities and stages of discovery. It provides ready-to-use datasets, data functions, leaderboards, and benchmarks for ML-driven drug discovery.

**Recent open issues (as of September 2026):**

| Issue | Summary | Theme |
|---|---|---|
| #399 | Leaderboard submission for Catalyst-V4-Turbo (ADMET Group 22/22) | Benchmark — active community participation |
| #394 | Score discrepancy and data contamination in Bioavailability_Ma leaderboard | Bug — data integrity in benchmarks |
| #392 | `convert_y_unit` applies p-to-nM conversion twice; nM-to-p is incorrect | Bug — unit-conversion logic |
| #390 | Buchwald-Hartwig dataset size mismatch | Bug — dataset curation |
| #389 | Dataset download failed | Infra — Dataverse availability |
| #387 | Question about mixing Hepatocyte clearance datasets (rat vs human) | Data — cross-species consistency |
| #386 | Pip install fails: "Compiler cl cannot compile programs" | DevOps — Windows build environment |

**Takeaway:** TDC has a vibrant, active community. Issues range from data curation bugs and unit-conversion errors to cross-species dataset mixing questions. The reliance on Harvard Dataverse for dataset hosting introduces a single point of failure. The 1,283-star count and 223 forks reflect strong adoption in the AI-for-drug-discovery community.

---

#### SynBioHub/synbiohub — Design sharing platform (84 ⭐, actively maintained)

SynBioHub is the community's primary web-based repository for sharing synthetic biology designs, supporting SBOL import/export and deployment via Docker. It hosts the complete iGEM Registry of Standard Biological Parts via a public instance at synbiohub.org.

**Recent open issues:**

| Issue | Summary | Theme |
|---|---|---|
| #1756 | SubCollections does not report members in public graph | Bug — data integrity in shared collections |
| #1755 | Recursive download does not follow linked collections | Bug — user workflow gap |
| #1754 | Legacy data in Virtuoso should be deleted | Maintenance — technical debt from DB migrations |
| #1753 | OMEX download missing SBML file (only downloads SBOL) | Bug — export completeness |
| #1752 | Changing private collection to public shifts prefix from `localhost:3333` to `synbiohub.org` | Bug — deployment/shareability friction |

**Takeaway:** The community is focused on **data integrity** (collections, exports), **technical-debt cleanup** (legacy DB data), and **deployment friction** (prefix/URL issues when sharing local designs publicly). These are classic growing-pains for a platform bridging academic research and real-world deployment.

---

#### 20n/act — Predictive bioengineering (92 ⭐)

20n/act is a platform for **computational synthetic biology** that predicts DNA insertions into cells (e.g., *E. coli*, *S. cerevisiae*) that modify the cell to produce a target molecule via fermentation. It famously predicted the first bio-route to Acetaminophen. The stack includes: predictive modeling (reaction-operator inference, SAR, reachables computation, cascade enumeration, DNA design), analytics (LCMS untargeted metabolomics via deep learning), and unit-economics modeling for bioproduction.

**Recent open issues:** No open issues as of the last check — suggesting the project is in a stable, production-ready state, with the core predictive pipeline considered finished. Contact is required for enterprise licensing and pre-packaged databases.

**Takeaway:** The sheer scope of the platform (10+ modules from NLP to patent search to cost modeling) makes it one of the most ambitious open-source bioengineering projects, but it also means the community is small and enterprise-oriented rather than broadly contributor-friendly.

---

#### Synbiota/GENtle2 — Web DNA editor (106 ⭐)

GENtle2 is a re-thought-for-the-web version of the classic GENtle desktop DNA editor. Core features are being extracted into modules.

**Recent open issues:**

| Issue | Summary | Theme |
|---|---|---|
| #253 | Jumping annotations | UI bug |
| #252 | Anchor and Cap selections won't change | UI bug |
| #251 | Spacing button doesn't work | UI bug |
| #250 | BLAST show button doesn't do anything | UI / integration bug |

**Takeaway:** These issues are quite old (created 2015) and point to long-standing UI interaction bugs that haven't been addressed — a common pattern in academic tools that lose active maintainers. The project is still listed as "in development" with recent updates, but the open issues suggest a gap between roadmap and bug triage.

---

#### MyersResearchGroup/iBioSim — CAD for genetic circuits (67 ⭐)

iBioSim is a CAD tool for modeling, analysis, and design of genetic circuits, with SBML/SBOL support.

**Recent open issues:**

| Issue | Summary | Theme |
|---|---|---|
| #640 | A Java exception has occurred | Stability / runtime |
| #639 | Can't upload SynBioHub design | Integration with design-sharing platforms |
| #638 | Unable to run iBioSim 3.2.0 on Mac | Cross-platform compatibility |

**Takeaway:** Issues center on cross-platform compatibility (Mac), runtime stability (Java exceptions), and interoperability with SynBioHub — reinforcing a key theme that synbio tools struggle with smooth integration across the networked ecosystem.

---

#### SynBioDex/libSBOLj — SBOL Java Library (43 ⭐, actively maintained)

libSBOLj provides the core Java interfaces and implementation for the Synthetic Biology Open Language (SBOL) specification. It offers an API for working with SBOL objects, read/write SBOL documents as XML/RDF, and a validator for checking the correctness of SBOL models. It is the reference Java implementation for SBOL and underpins many other tools in the ecosystem.

**Recent open issues:**

| Issue | Summary | Theme |
|---|---|---|
| #623 | Opaque failure while reading GenBank | Bug — unclear error messages when parsing malformed GenBank files |
| #621 | Invalid reporting of error sbol-11003 | Bug — validation error reporting is incorrect/misleading |
| #620 | displayID truncation in LOCUS field of GenBank conversions | Bug — data loss during format conversion |

**Takeaway:** All three open issues are from 2021 and center on **GenBank format handling** — parsing failures with poor error messages, validation error codes that don't accurately describe the problem, and data truncation during conversion. This reveals a pattern: libSBOLj's weakest point is **interoperability with external format converters** (GenBank in particular). Since libSBOLj is the reference implementation for SBOL, bugs here ripple across the entire ecosystem. TheApache-2.0 license and active maintainers (jakebeal) suggest these will eventually be fixed, but the nearly 5-year-old open issues indicate slow progress.

---

#### Autodesk/bionano-wetLabAccelerator — Visual wet-lab protocol designer (32 ⭐)

A tool for researchers working in synthetic biology and virology to design robotic wet lab protocols using a visual UI without coding. Users create protocols from scratch or use templates, set up each step with graphical visualizations of wet lab containers, and interact with results through dynamic visualizations. Generates vendor-specific code and verifies it.

**Recent open issues:**

| Issue | Summary | Theme |
|---|---|---|
| #4 | Update versions of dependencies | Maintenance — outdated stack (AngularJS, D3.js from 2017–2018) |
| #2 | Demo moved from wla.bionano.autodesk.com to wla.lifesciences.autodesk.com | Infrastructure — org rebranding / URL migration |

**Takeaway:** Only 2 open issues, both very old (2017–2018), suggesting the project is in maintenance mode. The dependency-update issue hints at technical debt from the old AngularJS stack. Autodesk's involvement shows surprising big-design-interest in synbio protocol automation, but the project appears to have been left in a semi-deprecated state.

---

#### SynBioCAD/biocad — Web-based SBOL CAD tool (16 ⭐)

An open-source, web-based computer-aided design tool for synthetic biology built on the SBOL standard and Parametric SBOLv. Supports visualization of SBOL3 designs, drag-and-drop modification, and sequence editing.

**Recent open issues:**

| Issue | Summary | Theme |
|---|---|---|
| #60 | Should ungroup preserve positions of child objects? | UI interaction |
| #59 | Export not valid SBOL2? | Standards compliance / export bug |
| #57 | Labels above glyphs | UI / visualization |
| #56 | Search for parts | Feature request — part discovery |
| #55 | Delete connection | UI interaction |
| #54 | Edit sequence → import file | Feature request — file import |
| #53 | Module sequence | Feature request — module-level editing |
| #52 | TypeError: Not allowed to request resource when exporting as GenBank | Bug — CORS / export integration |
| #51 | If I try to import a SBOL2 file, the tool freezes | Bug — import stability |
| #50 | Things aren't always deselected on mouse up | UI interaction bug |

**Takeaway:** A significant cluster of open issues (10+, all from 2019) suggests the project stalled after an initial burst of development. The issues span UI interaction bugs, export/import stability, and missing features like part search and module editing. The SBOL2 export bug (#59) and import freeze (#51) are particularly concerning for a CAD tool that claims SBOL compliance. This project illustrates the challenge of maintaining open-source academic tools beyond a proof-of-concept phase.

---

#### sysu-software/BiArkit — Integrated synbio toolkit (1 ⭐)

A versatile Java toolkit that integrates multiple modules for synthetic biology research: GenomeBrowser for genome visualization, Biobrick for part registry search, Riboswitch and SiRNA for regulatory element design, MetaNetwork for pathway database scanning, Simulator for metabolic network analysis, and G-Circle for genome expression illustration. Localized for offline use.

**Recent open issues:** No open issues found — the repository appears to be inactive, with no recent commits or issue activity. The last release included a Windows installer and compiled binaries, suggesting distribution through traditional academic channels rather than continuous open-source collaboration.

**Takeaway:** BiArkit represents an earlier era of synbio software — comprehensive feature set but packaged as a desktop application with a Windows installer, lacking modern CI/CD, issue tracking engagement, or community contribution workflows. The lack of open issues isn't a sign of health; it's a sign of dormancy.

---

#### SASTRA-iGEM2019/ToeholdSwitchDesign — RNA device design tools (0 ⭐)

Three open-source tools for machine-learning-based design of RNA devices (toehold switches): GrammarParser for sequence domain parsing, predict_linear for efficacy prediction using engineered features, and nn_model for neural-network-based prediction. Includes an end-to-end bash pipeline and a curated dataset of 228 toehold instances. Published in *Synthetic and Systems Biotechnology* (2022).

**Recent open issues:** No open issues found — the repository is very small and appears to be a completed academic project (iGEM 2019). The tools are well-documented with a video demo and published paper reference.

**Takeaway:** A clean example of an iGEM-team-built tool that does one thing well — predicting toehold switch efficacy — and ships with documentation, example data, and a published citation. While not actively maintained, it's a good reference for how to structure a small, focused scientific computing tool with proper documentation and reproducibility.

---

#### BIOFAB/Studio — Experimental web-based CAD tool (21 ⭐)

An experimental synthetic biology CAD tool based on open web standards (JavaScript, HTML 5, CSS 3). A platform for rapid deployment of CAD algorithms being developed at the BIOFAB. Also houses the Data Access Client for BIOFAB's electronic datasheets.

**Recent open issues:** No issues found. The repository appears to be in a stable or archived state, with no active issue tracking.

**Takeaway:** BIOFAB's experimental approach to web-based CAD tooling didn't sustain long-term community engagement. The lack of issues could mean the project was absorbed into other BIOFAB tools or superseded by more modern frameworks.

---

#### chaibio/chaipcr — Open-source qPCR instrument software (96 ⭐)

The software platform powering Chai's line of Real-Time PCR Thermocyclers, including the Open qPCR instrument. Released as open source to facilitate development of open-source qPCR instruments. Includes bioinformatics processing, device control (C++ realtime), web backend (Ruby on Rails), and frontend (JavaScript/HTML5).

**Recent open issues:**

| Issue | Summary | Theme |
|---|---|---|
| #105 | Website is down | Infrastructure — project web presence |
| #104 | No screen after factory reset | Device firmware / hardware |
| #102 | Can't set up a new account after factory reset | User management / device setup |
| #101 | Can I use PuTTY to login to the instrument? | Feature request — developer access |
| #44 | Open Hardware Schematics | Feature request — hardware openness |
| #1–#3 | Feature requests (early exit from cycling, pause, lid-opening safety) | Feature request — device control (unimplemented since 2016) |

**Takeaway:** The issues reveal a tension between the open-source software philosophy and the physical hardware reality. Issues #1–#3 (from 2016) are feature requests that were never implemented, while #104–#105 (from 2026) are infrastructure problems. The open-hardware schematics request (#44) remains unanswered — a gap between the open-source software and the closed hardware design. Chai Bio's commercial venture (Open qPCR) doesn't seem to give back to the open-source community proportionally.

---

#### dportik/Biotech-Job-Search-Engine — Open-source biotech career discovery (81 ⭐)

A personalized job-search engine for biotech and life-science careers that searches company career pages directly, ranks openings against your background, and learns from the jobs you actually apply to. Built for people in bioinformatics, computational biology, genomics, sequencing, data science, microbiome, translational research, diagnostics, and adjacent life-science fields.

**How it works:** Resume → Search Profile → Company Career Sites → ATS Collectors + Normalization → Scoring Engine → Ranked Matches + SQLite History → Human Calibration → Improved Profile / Scoring.

**Key features:**
- Searches major ATS platforms (Workday, Greenhouse, Lever, Ashby, Oracle, iCIMS, SmartRecruiters, Jobvite, ADP, etc.)
- Personalized scoring based on role fit, seniority, scientific domains, technical skills, geography, and explicit positive/negative signals
- Calibration workflow: rate real jobs (1–5 interest, Yes/Maybe/No apply), then back-test scoring changes against actual decisions
- SQLite history for deduplication across searches
- GitHub Actions workflow for automated daily searches with email alerts

**Recent open issues:**

| Issue | Summary | Theme |
|---|---|---|
| #3 | HTML Descriptions are multiline which confuses CSV | Bug — data parsing / output format |
| #2 | Is score supposed to be in ranked_jobs.csv? | UX — output clarity / documentation gap |

**Takeaway:** Only 2 open issues, both from the initial user feedback phase — the tool is relatively mature for its niche. The issues point to a need for better output documentation and CSV handling for multi-line HTML descriptions. This project fills a unique niche: it's not a synbio *design* tool, but it addresses the biotech talent pipeline that feeds the entire ecosystem.

---

### 🌐 Broader GitHub Issues Landscape

A wider search across GitHub for `synthetic biology bioinformatics is:issue is:open` returned **104 results**, revealing additional community activity patterns:

| Theme | Examples | What it tells us |
|---|---|---|
| **Daily paper / literature tracking** | Multiple repos auto-posting daily ArXiv paper digests (protein structure AI, multimodal, bioRxiv) | The community is saturated with ML-for-biology preprints; tools to filter and prioritize are in demand |
| **Gene regulatory network inference** | [DeCovarT](https://github.com/bastienchassagnol/DeCovarT) — "in silico inference of gene regulatory networks" (enhancement label, active) | Computational biology methods for GRN inference are still actively developing |
| **Protein structure & conformational landscapes** | [SKM](https://github.com/delalamo/SKM) — "synthetic sequence alignments as programmable probes of learned conformational landscapes" | Deep learning protein structure prediction is being probed with synthetic sequences — a synthetic biology + ML crossover |
| **Sequence design & editing** | [pydurma](https://github.com/buda-base/pydurma) — "reolocation (transposition) mode: detect and represent moved blocks" | Genomic sequence manipulation tooling is expanding beyond simple editing |
| **Job market & career resources** | [phjobs](https://github.com/pmuangpi-creator/phjobs) — daily biotech/pharma job digests with 88 comments | The biotech talent market is a hot topic; community sustains active discussion |

---

### 📊 Community Themes (from issue surveys across all projects)

Across these projects, the synbio/biotech open-source community is currently focused on:

1. **Interoperability & integration friction** — iBioSim can't upload to SynBioHub; OMEX exports miss SBML files; collection prefixes shift when changing visibility. The dream of a connected synbio toolchain is still hampered by format/URL/API mismatches.
2. **Data integrity in shared collections** — SubCollections not reporting members, recursive downloads not following links, legacy DB data piling up — these are growing-pains for platforms that host community-wide design registries.
3. **Long-standing UI bugs in academic tools** — GENtle2's 2015-era interaction bugs remain unfixed; SynBioCAD/biocad's 2019-era UI issues persist. A common pattern in academic tools that lose active maintainers.
4. **Cross-platform compatibility** — iBioSim's Mac issue persists, a reminder that Java "write once" is aspirational, not guaranteed.
5. **Stable enterprise-oriented platforms vs. community-friendly ones** — 20n/act has zero open issues but requires enterprise licensing; Chai Bio's open-source software doesn't extend to hardware schematics. This tension between open-source ideals and practical deployment runs throughout the ecosystem.
6. **Deployment & DevOps gaps** — Virtuoso database migrations, Docker image complexity (SynBioHub requires Virtuoso, Maven, Node, etc.) — these barriers push away potential contributors and users who just want to run the tool.
7. **Stalled academic projects** — BiArkit, BIOFAB Studio, and SynBioCAD/biocad all show signs of dormancy with zero open issues but no active maintenance. The "publish and abandon" pattern is prevalent in university synbio software.
8. **ML + sequence design convergence** — ART's ML for strain engineering, iBioSim's circuit design, TDC's therapeutic benchmarks, SKM's conformational landscape probing, and the broader ecosystem point to an accelerating intersection of machine learning and biological design automation.
9. **Open hardware vs. open software divide** — Chai Bio released qPCR software as open source but keeps hardware schematics closed, revealing a gap in the open-science philosophy when commercial interests are involved.
10. **Information overload & literature tracking** — The explosion of daily ArXiv/bioRxiv preprints in ML-for-biology has created demand for automated paper digests, filtering tools, and prioritized reading lists. Multiple community-maintained daily-paper repos indicate this is a real pain point.
11. **Biotech talent pipeline** — The Biotech-Job-Search-Engine and phjobs repos show that career discovery and job market navigation are active concerns for the community, especially as roles span "Computational Biologist," "Bioinformatics Scientist," "Data Scientist," and more.
12. **FHIR/health-data standardization** — Synthea's issues around FHIR R4 export bugs and US Core compliance point to healthcare data interoperability as a live concern even in synthetic data generation tools, with implications for any tool that touches clinical or health-related data.

---

### 🏛️ Key Organizations & Communities

- **SynBioHub (SynBioHub org)** — Maintains the primary design-sharing platform and the SBOL Java library (libSBOLj)
- **SynBioDex** — Publishes the SBOL specification and related tools; community-driven standards effort
- **Myers Research Group** — Academic lab behind iBioSim; representative of university synbio CAD efforts
- **JBEI (Joint BioEnergy Institute)** — DOE-funded lab; produces ART for strain engineering
- **20n** — Startup that produced act; bridges academic research and commercial bioengineering
- **Autodesk Bio/Nano/Protospace** — Surprise entry! Autodesk's wet-lab-accelerator tool shows big-design-interest in synbio protocol automation
- **klavinslab** — University of Washington lab; contributes Coral framework for synbio design processes
- **MIMS/Harvard (Marinka Zitnik's lab)** — Produces TDC; the largest and most active community in therapeutics ML
- **synthetichealth** — Produces Synthea; the largest synbio-adjacent project by stars, focused on synthetic patient data
- **Chai Bio** — Produces chaipcr; open-hardware science instrumentation (with limitations)
- **websemantics** — Curates the awesome-synthetic-biology list; community front door for the field
- **BIOFAB** — Early contributor to web-based synbio CAD tools; experimental but historically significant
- **SynBioCAD** — Community effort around SBOL-based web CAD tooling; stalled but conceptually important
- **SASTRA-iGEM** — iGEM team example of small, focused, well-documented scientific computing tools
- **Sysu Software** — Chinese academic group; produced the comprehensive BiArkit toolkit

---

## 🏛️ Key Resources & Curated Lists

| Resource | Stars | Description |
|---|---|---|
| [websemantics/awesome-synthetic-biology](https://github.com/websemantics/awesome-synthetic-biology) | 223 | Curated list of synbio projects, articles, and resources |
| [virtualramblas/awesome-deep-learning-4-life-sciences](https://github.com/virtualramblas/awesome-deep-learning-4-life-sciences) | 167 | Curated list of deep-learning resources for biotech & pharma |
| [mims-harvard/TDC](https://github.com/mims-harvard/TDC) | 1,283 | Therapeutics Data Commons — ML benchmark suite for drug discovery |
| [synthetichealth/synthea](https://github.com/synthetichealth/synthea) | 3,342 | Synthetic patient population simulator for EHR modeling & health analytics |
| [llSourcell/Learn_Synthetic_Biology](https://github.com/llSourcell/Learn_Synthetic_Biology) | 157 | Educational resources for getting started in synbio |
| [dportik/Biotech-Job-Search-Engine](https://github.com/dportik/Biotech-Job-Search-Engine) | 81 | Open-source job-discovery for biotech, genomics & bioinformatics roles |

---

## 📂 Archive Structure

```
episode-scripts-archive/
├── episodes/
│   └── EPXXX-title/
│       ├── script.md
│       ├── sources.md
│       └── assets/
├── research/
│   ├── synbio-tools-survey-2026-09.md
│   └── community-issues-snapshot-2026-09.md
├── templates/
│   ├── episode-script-template.md
│   └── sources-template.md
└── README.md
```

---

## 🔗 Quick Reference Links

- [SynBioHub](https://synbiohub.org) — Hosted design-sharing platform (public instance)
- [SynBioHub Wiki](https://wiki.synbiohub.org) — Installation & API docs
- [20n/act Wiki](https://github.com/20n/act/wiki) — Predictive bioengineering docs
- [TDC Website](https://tdcommons.ai) — Therapeutics Data Commons portal
- [Synthea](https://synthetichealth.github.io/synthea/) — Synthetic patient population simulator
- [iBioSim](http://www.ibiosim.org/) — Genetic circuit CAD tool
- [SBOL Specification](https://sbolstandard.org/) — Synthetic Biology Open Language standard
- [TISIGNER](http://tignamer.com/) — Interactive synbio design
- [GENtle2](https://synbiota.com) — Web DNA editor
- [Autodesk Wet Lab Accelerator](https://wla.bionano.autodesk.com) — Visual wet-lab protocol designer

---

*Last research update: September 2026*