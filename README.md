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
| [bebop/poly](https://github.com/bebop/poly) | 737 | Go | Go package for engineering organisms — codon optimization, primer design, sequence hashing |
| [Edinburgh-Genome-Foundry/DnaChisel](https://github.com/Edinburgh-Genome-Foundry/DnaChisel) | 281 | Python | Versatile DNA sequence optimizer — codon optimization, GC tuning, constraint satisfaction |
| [websemantics/awesome-synthetic-biology](https://github.com/websemantics/awesome-synthetic-biology) | 223 | (list) | Curated directory of synbio projects, articles, and resources |
| [virtualramblas/awesome-deep-learning-4-life-sciences](https://github.com/virtualramblas/awesome-deep-learning-4-life-sciences) | 167 | — | Curated list of deep-learning resources for biotech & pharma |
| [llSourcell/Learn_Synthetic_Biology](https://github.com/llSourcell/Learn_Synthetic_Biology) | 157 | — | Educational resources for getting started in synbio |
| [Synbiota/GENtle2](https://github.com/Synbiota/GENtle2) | 106 | JavaScript | Web-based DNA editor for synthetic biology |
| [chaibio/chaipcr](https://github.com/chaibio/chaipcr) | 96 | C++ | Software behind Chai's open-source Real-Time PCR instrument |
| [20n/act](https://github.com/20n/act) | 92 | Java | Predictive bioengineering — discovers DNA routes to make target chemicals |
| [SynBioHub/synbiohub](https://github.com/SynBioHub/synbiohub) | 84 | JavaScript | Web platform for browsing, uploading & sharing synthetic biology designs |
| [dportik/Biotech-Job-Search-Engine](https://github.com/dportik/Biotech-Job-Search-Engine) | 81 | Python | Open-source job-discovery for biotech, genomics & bioinformatics roles |
| [MyersResearchGroup/iBioSim](https://github.com/MyersResearchGroup/iBioSim) | 67 | Java | CAD for genetic circuits; SBML/SBOL support |
| [JBEI/ART](https://github.com/JBEI/ART) | 66 | Jupyter Notebook | ML tool to improve strain engineering effectiveness |
| [SynBioDex/libSBOLj](https://github.com/SynBioDex/libSBOLj) | 43 | Java | Java library for the Synthetic Biology Open Language (SBOL) |
| [Autodesk/bionano-wetLabAccelerator](https://github.com/Autodesk/bionano-wetLabAccelerator) | 32 | JavaScript | Designs robotic wet-lab protocols via visual UI (no coding) |
| [klavinslab/coral](https://github.com/klavinslab/coral) | 32 | Python | Library & framework for specifying synbio design processes |
| [SynBioCAD/biocad](https://github.com/SynBioCAD/biocad) | 16 | JavaScript | Web-based CAD tool for synthetic biology built on SBOL standard |
| [BIOFAB/ClothoBiofabEdition](https://github.com/BIOFAB/ClothoBiofabEdition) | 9 | Java | Synthetic Biology Computer-Aided Design tool |

---

### 🧬 In-Depth Investigation (active repos, open issues reviewed)

#### bebop/poly — Go Package for Engineering Organisms (737 ⭐)

The largest and most actively developed pure synbio software tool in this survey. (Poly)merase is a modern, fast Go library for computational synthetic biology — from codon optimization and primer design to circular sequence hashing. It targets industrial, academic, and hobbyist settings with a strong emphasis on reproducibility and speed.

**Repository structure:** Alphabet handling, checks, clone operations, data, folding, I/O, primers, random generation, search, sequence hashing, synthesis, and transform modules.

**Key features:**
- Codon optimization and primer design
- Circular sequence hashing
- Well-tested with CI and coverage badges
- Discord community for real-time discussion
- Extensive tutorial system and "How to Synbio" learning resources
- MIT license with active sponsorship

**Why it matters:** Poly represents a new generation of synbio tools — fast, modern, community-oriented, and designed for programmatic pipelines. Unlike aging Java-based CAD tools, Go's simplicity and performance make it ideal for high-throughput DNA design workflows. The project explicitly aims to be "the most complete, open, and well-used collection of computational synthetic biology tools ever assembled."

---

#### Edinburgh-Genome-Foundry/DnaChisel — DNA Sequence Optimizer (281 ⭐)

A Python library for optimizing DNA sequences with respect to constraints and optimization objectives. Can be used via CLI, Python API, or a web application. Comes with 15+ classes of sequence specifications: codon-optimization, GC-content tuning, avoidance of restriction sites, homology removal, and more. Users can define custom specifications in Python.

**Recent open issues (as of September 2026):**

| Issue | Summary | Theme |
|---|---|---|
| [#114](https://github.com/Edinburgh-Genome-Foundry/DnaChisel/issues/114) | Produce multiple different optimized results | Feature — diversity in optimization output |
| [#113](https://github.com/Edinburgh-Genome-Foundry/DnaChisel/issues/113) | Low Codon Adaptation Index on optimized sequence | Bug — optimization quality |
| [#107](https://github.com/Edinburgh-Genome-Foundry/DnaChisel/issues/107) | Support for Uridine Depletion (UD) optimization objectives | Feature — new optimization target (5 comments) |
| [#111](https://github.com/Edinburgh-Genome-Foundry/DnaChisel/issues/111) | Unexpected Mutation of `codon_usage_table` During Optimization | Bug — data integrity (assigned to veghp) |
| [#110](https://github.com/Edinburgh-Genome-Foundry/DnaChisel/issues/110) | Minimize CG | Feature — additional GC optimization |
| [#105](https://github.com/Edinburgh-Genome-Foundry/DnaChisel/issues/105) | Include CONTRIBUTING in documentation | Maintenance — docs gap |
| [#102](https://github.com/Edinburgh-Genome-Foundry/DnaChisel/issues/102) | PDF report generation optional during optimize_with_report | Enhancement — modular reporting (assigned to veghp) |
| [#100](https://github.com/Edinburgh-Genome-Foundry/DnaChisel/issues/100) | How to get under-optimal sequences during optimization? | Question — fitness landscape exploration |

**Takeaway:** DnaChisel's issues reveal a community actively pushing the tool's capabilities — requesting new optimization objectives (Uridine Depletion, CG minimization), diversity in output solutions, and better reporting. The `codon_usage_table` mutation bug (#111) is concerning because it could silently produce incorrect optimization results. The #100 issue (how to get sub-optimal solutions) points to a deeper need: users want to explore the fitness landscape, not just find the single best sequence. This has direct implications for episode content about the difference between "optimal" and "good enough" in biological sequence design.

**Part of the EGF Codons suite** — a broader synthetic biology software ecosystem from the Edinburgh Genome Foundry including Geneblocks and other tools.

---

#### synthetichealth/synthea — Synthetic Patient Population Simulator (3,342 ⭐)

The largest and most active project in this survey. Synthea generates synthetic patient populations and corresponding electronic health records (EHRs) for research, benchmarking, and software testing.

**Recent open issues:**

| Issue | Summary | Theme |
|---|---|---|
| #1700 | Proposal: stable de-identified export manifest for downstream benchmarks | Feature — standardization for benchmarking |
| #1703 | CSV SYSTEM column depends on whether FHIR export is enabled | Bug — data consistency across export formats |
| #1702 | FHIR R4 allergy export loses reaction severity by mutating a HashMap key | Bug — data corruption in FHIR export |
| #1365 | US Core 3.1 | Feature — compliance with latest US Core FHIR spec |

**Takeaway:** Synthea's issues reveal a community focused on **data consistency across export formats** (CSV vs FHIR), **standardization for benchmarking** (stable export manifests), and **regulatory compliance** (US Core 3.1). The HashMap key mutation bug (#1702) is particularly concerning — it silently corrupts allergy reaction severity data in FHIR R4 exports, which could affect downstream clinical research.

---

#### mims-harvard/TDC — Therapeutics Data Commons (1,283 ⭐)

The largest AI-for-drug-discovery project in this survey. TDC provides ready-to-use datasets, data functions, leaderboards, and benchmarks for ML-driven drug discovery.

**Recent open issues:**

| Issue | Summary | Theme |
|---|---|---|
| #399 | Leaderboard submission for Catalyst-V4-Turbo (ADMET Group 22/22) | Benchmark — active community participation |
| #394 | Score discrepancy and data contamination in Bioavailability_Ma leaderboard | Bug — data integrity in benchmarks |
| #392 | `convert_y_unit` applies p-to-nM conversion twice; nM-to-p is incorrect | Bug — unit-conversion logic |
| #390 | Buchwald-Hartwig dataset size mismatch | Bug — dataset curation |
| #389 | Dataset download failed | Infra — Dataverse availability |
| #387 | Question about mixing Hepatocyte clearance datasets (rat vs human) | Data — cross-species consistency |
| #386 | Pip install fails: "Compiler cl cannot compile programs" | DevOps — Windows build environment |

**Takeaway:** TDC has a vibrant, active community. Issues range from data curation bugs and unit-conversion errors to cross-species dataset mixing questions. The reliance on Harvard Dataverse for dataset hosting introduces a single point of failure.

---

#### SynBioHub/synbiohub — Design sharing platform (84 ⭐, actively maintained)

SynBioHub is the community's primary web-based repository for sharing synthetic biology designs, supporting SBOL import/export and deployment via Docker. It hosts the complete iGEM Registry of Standard Biological Parts via a public instance at synbiohub.org. BSD-2-Clause license. Stack: JavaScript (Node.js) + Java (Maven) + OpenLink Virtuoso (RDF triplestore).

**Recent open issues:**

| Issue | Summary | Theme |
|---|---|---|
| [#1756](https://github.com/SynBioHub/synbiohub/issues/1756) | SubCollections does not report members in public graph | Bug — data integrity in shared collections |
| [#1755](https://github.com/SynBioHub/synbiohub/issues/1755) | Recursive download does not follow linked collections | Bug — user workflow gap |
| [#1754](https://github.com/SynBioHub/synbiohub/issues/1754) | Legacy data in Virtuoso should be deleted | Maintenance — technical debt from DB migrations |
| [#1753](https://github.com/SynBioHub/synbiohub/issues/1753) | OMEX download missing SBML file (only downloads SBOL) | Bug — export completeness (2 comments) |
| [#1752](https://github.com/SynBioHub/synbiohub/issues/1752) | Changing private collection to public shifts prefix from `localhost:3333` to `synbiohub.org` | Bug — deployment/shareability friction |
| [#1746](https://github.com/SynBioHub/synbiohub/issues/1746) | Incremental updates not work with SBOLExplorer | Bug — tool integration (Milestone: SBH 1.6.2) |
| [#1744](https://github.com/SynBioHub/synbiohub/issues/1744) | Backend should have a mechanism to parse OR request | Bug — query capability gap |

**Takeaway:** The community is focused on **data integrity** (collections, exports), **technical-debt cleanup** (legacy DB data), and **deployment friction** (prefix/URL issues when sharing local designs publicly). These are classic growing-pains for a platform bridging academic research and real-world deployment. The SBH 1.6.2 milestone suggests active release planning.

---

#### 20n/act — Predictive bioengineering (92 ⭐)

20n/act is a platform for **computational synthetic biology** that predicts DNA insertions into cells (e.g., *E. coli*, *S. cerevisiae*) that modify the cell to produce a target molecule via fermentation. It famously predicted the first bio-route to Acetaminophen. Stack: Java/Scala + Python (deep learning for LCMS) + R (visualization).

**Key modules:** Installer, Reaction Operator inference, Biointerpretation, Reachables computation, Cascades computation, DNA designer, NLP for enzymatic biochemistry, patent search, Bioreachables wiki.

**Recent open issues:** No open issues found — the project appears stable but is primarily maintained internally by 20n Inc.

**Takeaway:** The sheer scope of the platform (10+ modules from NLP to patent search to cost modeling) makes it one of the most ambitious open-source bioengineering projects, but it also means the community is small and enterprise-oriented rather than broadly contributor-friendly.

---

#### Synbiota/GENtle2 — Web DNA editor (106 ⭐)

GENtle2 is a re-thought-for-the-web version of the classic GENtle desktop DNA editor. Core features are being extracted into modules using the Refactor milestone pattern.

**Recent open issues:**

| Issue | Summary | Theme |
|---|---|---|
| #164 | Display feature details when hovering | UI / Refactor |
| #163 | Tracking mouse events in `Artist` | Feature / Refactor |
| #162 | Selection disappears when copied via context menu | Bug |
| #161 | Selection disappears with hotkeys without shift | Bug |
| #159 | Tracking shapes in `Artist` | Feature / Refactor (6 comments) |
| #158 | Creating a feature clears plasmid map but doesn't redraw | Bug / Refactor |
| #156 | Caret moves by one base unexpectedly | Bug / Refactor |
| #154 | Plasmid map title overflows for long sequence names | Refactor / Optimization |

**Takeaway:** GENtle2's issues are organized under a "Refactor — Canvas events & RES/annotation cards information" milestone, suggesting the maintainer is actively working on a modernized architecture. However, the original bugs from 2014-era GENtle persist in the backlog. The refactor milestone is a signal that the project is attempting a clean-slate approach rather than patching the old codebase — a story worth telling in an episode about technical debt in scientific software.

---

#### MyersResearchGroup/iBioSim — CAD for genetic circuits (67 ⭐)

iBioSim is a CAD tool for modeling, analysis, and design of genetic circuits, with SBML/SBOL support. Active developers: Lukas Buecherl, Pedro Fontanarrosa, Chris Myers.

**Recent open issues:**

| Issue | Summary | Theme |
|---|---|---|
| [#640](https://github.com/MyersResearchGroup/iBioSim/issues/640) | A Java exception has occurred | Stability / runtime |
| [#639](https://github.com/MyersResearchGroup/iBioSim/issues/639) | Can't upload SynBioHub design | Integration with design-sharing platforms |
| [#638](https://github.com/MyersResearchGroup/iBioSim/issues/638) | Unable to run iBioSim 3.2.0 on Mac | Cross-platform compatibility |
| [#637](https://github.com/MyersResearchGroup/iBioSim/issues/637) | Unable to generate models automatically (NoClassDefFoundError: Apache Jena/Xerces) | Bug — Java dependency conflict (6 comments) |
| [#635](https://github.com/MyersResearchGroup/iBioSim/issues/635) | Cannot open iBioSim on Windows 11 | Cross-platform compatibility |
| [#632](https://github.com/MyersResearchGroup/iBioSim/issues/632) | Can't connect to LCP Synbiohub | Integration failure |

**Key error from #637 (most discussed):**
```
java.lang.NoClassDefFoundError: Could not initialize class org.apache.jena.query.ARQ
Caused by: java.lang.NoClassDefFoundError: org/apache/xerces/util/XMLChar
```
This is a transitive dependency conflict — Apache Jena can't initialize because Xerces is missing or conflicting. Users hitting this when trying to generate models from SBOL designs via SynBioHub integration.

**Takeaway:** iBioSim's 305+ open issues center on cross-platform compatibility (Mac, Windows 11), Java dependency management, and interoperability with SynBioHub. This reinforces a key theme: desktop-based synbio CAD tools struggle with modern OS environments and networked ecosystems. There's a clear opportunity for containerized or web-based alternatives.

---

### 🌐 Broader GitHub Issues Landscape

A wider search across GitHub for synbio/biotech open issues reveals additional community activity patterns:

| Theme | Examples | What it tells us |
|---|---|---|
| **Daily paper / literature tracking** | Multiple repos auto-posting daily ArXiv paper digests (protein structure AI, multimodal, bioRxiv) | The community is saturated with ML-for-biology preprints; tools to filter and prioritize are in demand |
| **Gene regulatory network inference** | DeCovarT — "in silico inference of gene regulatory networks" (enhancement label, active) | Computational biology methods for GRN inference are still actively developing |
| **Protein structure & conformational landscapes** | SKM — "synthetic sequence alignments as programmable probes of learned conformational landscapes" | Deep learning protein structure prediction is being probed with synthetic sequences — a synthetic biology + ML crossover |
| **Sequence design & editing** | pydurma — "relocation (transposition) mode: detect and represent moved blocks" | Genomic sequence manipulation tooling is expanding beyond simple editing |
| **Job market & career resources** | phjobs — daily biotech/pharma job digests with 88 comments | The biotech talent market is a hot topic; community sustains active discussion |

---

### 📊 Community Themes (from issue surveys across all projects)

Across these projects, the synbio/biotech open-source community is currently focused on:

1. **Interoperability & integration friction** — iBioSim can't upload to SynBioHub; OMEX exports miss SBML files; collection prefixes shift when changing visibility. The dream of a connected synbio toolchain is still hampered by format/URL/API mismatches.
2. **Data integrity in shared collections** — SubCollections not reporting members, recursive downloads not following links, legacy DB data piling up — these are growing-pains for platforms that host community-wide design registries.
3. **Long-standing UI bugs in academic tools** — GENtle2's 2015-era interaction bugs remain unfixed; SynBioCAD/biocad's 2019-era UI issues persist. A common pattern in academic tools that lose active maintainers.
4. **Cross-platform compatibility** — iBioSim's Mac and Windows 11 issues, TDC's Windows pip install failures — Java "write once, run anywhere" remains aspirational, not guaranteed.
5. **Optimization depth vs. usability** — DnaChisel users want to explore sub-optimal solutions (fitness landscapes), not just get the single best answer. This is a fundamental UX challenge in computational biology.
6. **Stable enterprise-oriented platforms vs. community-friendly ones** — 20n/act has zero open issues but requires enterprise licensing; Chai Bio's open-source software doesn't extend to hardware schematics. This tension between open-source ideals and practical deployment runs throughout the ecosystem.
7. **Deployment & DevOps gaps** — Virtuoso database migrations (SynBioHub), Docker image complexity, and Windows build failures (TDC) — these barriers push away potential contributors and users who just want to run the tool.
8. **Stalled academic projects** — BiArkit, BIOFAB Studio, and SynBioCAD/biocad all show signs of dormancy with zero open issues but no active maintenance. The "publish and abandon" pattern is prevalent in university synbio software.
9. **Modern language adoption** — The success of **poly** (Go, 737⭐) and **DnaChisel** (Python, 281⭐) vs. aging Java tools (iBioSim, GENtle2) suggests the community is gravitating toward modern, fast, easy-to-deploy languages for scientific tooling.
10. **ML + sequence design convergence** — ART's ML for strain engineering, iBioSim's circuit design, TDC's therapeutic benchmarks, DnaChisel's optimization, and the broader ecosystem point to an accelerating intersection of machine learning and biological design automation.
11. **Open hardware vs. open software divide** — Chai Bio released qPCR software as open source but keeps hardware schematics closed, revealing a gap in the open-science philosophy when commercial interests are involved.
12. **Information overload & literature tracking** — The explosion of daily ArXiv/bioRxiv preprints in ML-for-biology has created demand for automated paper digests, filtering tools, and prioritized reading lists.

---

### 🏛️ Key Organizations & Communities

- **SynBioHub (SynBioHub org)** — Maintains the primary design-sharing platform and the SBOL Java library (libSBOLj)
- **SynBioDex** — Publishes the SBOL specification and related tools; community-driven standards effort
- **Edinburgh Genome Foundry** — Produces DnaChisel and the broader EGF Codons suite; major Python contribution to the ecosystem
- **Myers Research Group** — Academic lab behind iBioSim; representative of university synbio CAD efforts
- **JBEI (Joint BioEnergy Institute)** — DOE-funded lab; produces ART for strain engineering
- **20n** — Startup that produced act; bridges academic research and commercial bioengineering
- **Autodesk Bio/Nano/Protospace** — Surprise entry! Autodesk's wet-lab-accelerator tool shows big-design-interest in synbio protocol automation
- **klavinslab** — University of Washington lab; contributes Coral framework for synbio design processes
- **MIMS/Harvard (Marinka Zitnik's lab)** — Produces TDC; the largest community in therapeutics ML
- **synthetichealth** — Produces Synthea; the largest synbio-adjacent project by stars, focused on synthetic patient data
- **Chai Bio** — Produces chaipcr; open-hardware science instrumentation (with limitations)
- **bebop / Timothy Stiles** — Creator of poly; modern Go-based approach to computational synthetic biology
- **websemantics** — Curates the awesome-synthetic-biology list; community front door for the field
- **BIOFAB** — Early contributor to web-based synbio CAD tools; experimental but historically significant
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
| [bebop/poly](https://github.com/bebop/poly) | 737 | Go package for engineering organisms — modern synbio tooling |
| [Edinburgh-Genome-Foundry/DnaChisel](https://github.com/Edinburgh-Genome-Foundry/DnaChisel) | 281 | Python DNA sequence optimizer for codon, GC, and constraint design |
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
- [DnaChisel Docs](https://edinburgh-genome-foundry.github.io/DnaChisel/) — DNA sequence optimizer documentation
- [poly tutorials](https://github.com/bebop/poly/tree/main/tutorials) — Go synbio tooling tutorials
- [TISIGNER](http://tignamer.com/) — Interactive synbio design
- [GENtle2](https://synbiota.com) — Web DNA editor
- [Autodesk Wet Lab Accelerator](https://wla.bionano.autodesk.com) — Visual wet-lab protocol designer

---

*Last research update: September 2026*