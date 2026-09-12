# 🔬 Synthetic Biology & Biotech Software Tools — Research Findings

> **Surveyd September 2026** — A snapshot of open issues and community concerns across key synbio/biotech open-source projects on GitHub. This document was compiled as research for the *episode-scripts-archive* project.

---

## 🏆 Synthesized Landscape — High-Activity / High-Relevance Tools

| Project | Stars | Language | What it does |
|---|---|---|---|
| [biopython/biopython](https://github.com/biopython/biopython) | 5,070 | Python | Foundational Python toolkit for computational molecular biology |
| [google/deepvariant](https://github.com/google/deepvariant) | 3,726 | Python | Deep-learning variant calling from NGS data |
| [nextflow-io/nextflow](https://github.com/nextflow-io/nextflow) | 3,412 | Groovy | DSL for reproducible, scalable bioinformatics pipelines |
| [Edinburgh-Genome-Foundry/DnaFeaturesViewer](https://github.com/Edinburgh-Genome-Foundry/DnaFeaturesViewer) | 690 | Python | Plot DNA sequence features from GenBank/GFF files |
| [bebop/poly](https://github.com/bebop/poly) | 729 | Go | Go package for engineering organisms (codon optimization, primer design, synthesis fragments) |
| [deeptools/deepTools](https://github.com/deeptools/deepTools) | 765 | Python | Process & analyze deep-sequencing data (normalization, coverage, visualization) |
| [deeptools/HiCExplorer](https://github.com/deeptools/HiCExplorer) | 276 | Python | Process, normalize & visualize Hi-C data |
| [Edinburgh-Genome-Foundry/DnaChisel](https://github.com/Edinburgh-Genome-Foundry/DnaChisel) | 274 | Python | DNA sequence optimizer (expression, synthesis, mRNA constraints) |
| [Adibvafa/CodonTransformer](https://github.com/Adibvafa/CodonTransformer) | 212 | Python | Transformer-based ML codon optimizer (2M+ downloads) |
| [Merck/deepbgc](https://github.com/Merck/deepbgc) | 158 | Jupyter Notebook | Deep learning for Biosynthetic Gene Cluster detection |
| [broadinstitute/viral-ngs](https://github.com/broadinstitute/viral-ngs) | 197 | Python | Command-line viral NGS toolkit (assembly, classification, phylogenetics) |
| [SynBioHub/synbiohub](https://github.com/SynBioHub/synbiohub) | 84 | JavaScript | Web platform for sharing synthetic biology designs |
| [CIDARLAB/Cello-v2](https://github.com/CIDARLAB/Cello-v2) | 74 | Java | Genetic circuit design automation (successor to the original Cello) |
| [MyersResearchGroup/iBioSim](https://github.com/MyersResearchGroup/iBioSim) | 67 | Java | CAD for genetic circuits; SBML/SBOL support |
| [khokao/synergetica](https://github.com/khokao/synergetica) | 118 | TypeScript | Node-based desktop app for genetic circuit design |
| [BuildACell/bioCRNpyler](https://github.com/BuildACell/bioCRNpyler) | 54 | Python | Modular compiler for biomolecular chemical reaction networks (SBML output) |
| [SynBioDex/SBOLCanvas](https://github.com/SynBioDex/SBOLCanvas) | 17 | TypeScript | Web app for creation & editing of genetic constructs using the SBOL visual standard |
| [lexO-dat/CELLM](https://github.com/lexO-dat/CELLM) | 2 | Python | AI-powered bridge between synthetic biology and natural-language processing |

---

## 🧬 In-Depth Investigation — Open Issues Reviewed

### CIDARLAB/Cello-v2 (genetic circuit design automation)

**Repo:** 874 ⭐ (original Cello), 74 ⭐ (Cello-v2) · **Language:** Java · **License:** BSD-2-Clause

Cello lets users specify genetic circuits in **Verilog**, synthesizes them into logic gates, assigns experimentally characterized **TetR homologs** as NOR/NOT gates using Hill-function response curves, and then generates physical DNA sequences via the **Eugene language**. Cello-v2 is the actively maintained successor.

| # | Issue | Description |
|---|---|---|
| #50 | Licensing question | User asks about licensing for Cello-v2 and the Docker-based DNACompiler container |
| #49 / #48 | Login failures | Persistent inability to create accounts on hosted `cellocad.org` using Gmail addresses |
| #47 | Sequential logic | Feature request: support for sequential (clocked) logic in Cello-v2 |
| #26 | GFF/APE/FASTA output | Long-standing enhancement: export designs in GFF, APE, and FASTA formats |
| #63 | Account creation (original Cello) | Same login issue on the original Cellocad platform |

**Takeaway:** Friction between the **open-source CLI** and the **hosted web service** — a common theme across academic synbio tooling. Users trust the community cloud but it lacks DevOps backing.

---

### BuildACell/bioCRNpyler (biomolecular CRN compiler)

**Repo:** 54 ⭐ · **Language:** Python · **License:** BSD-3-Clause

BioCRNpyler compiles high-level biological part specifications (promoters, RBSs, CDSs, terminators) into **SBML chemical reaction networks**. It has first-class support for **cell-free transcription–translation (TXTL) extracts** as simulation contexts, and supports automatic CRN compilation and interactive visualization.

| # | Issue | Description |
|---|---|---|
| #328 | TMSE companion module | Feature request: implement toehold-mediated strand displacement circuits as a "companion module" |
| #337 | ODEint convergence failure | Bug: `ODEint` fails with "Repeated convergence failures" when using EnergyTXTL context |
| #338 | Multi-substrate membrane components | Feature request: allow lists of multiple substrates for membrane components (i.e. transport) |
| #333 | Naming conventions | Task: use consistent naming conventions for classes |
| #341 | CI with bioscrape | Task: include bioscrape in CI tests |
| #339 | Examples handling | Task: decide how to handle examples |

**Takeaway:** The project is actively expanding toward **RNA-based devices** (TMSE module bridges into the toehold-switch toolchain from SASTRA-iGEM) and **cell-free expression** (EnergyTXTL), with growing pains around internal consistency and CI maturity.

---

### SynBioDex/SBOLCanvas (SBOL-based genetic construct editor)

**Repo:** 17 ⭐ · **Language:** TypeScript · **License:** Apache-2.0

SBOLCanvas is a web application (Angular frontend + Dockerized Java backend) for creating and editing genetic designs using the **SBOL 2/3 data and visual standard**, with import/export via SynBioHub.

| # | Issue | Description |
|---|---|---|
| #426 / #463 | Modeling elements + SBML linkage | Add additional modeling elements; add SBOL Model object referencing generated SBML files (Milestone 3.0) |
| #458 / #460 | Annotations & parts | Add support for feature annotations; add ability to define parts (Milestone 2.1) |
| #417 | Visual polish | Adjustable stroke width of part glyphs (Milestone 2.1) |
| #446 | Circular DNA import | Circular topology recognized by VisBOL but not SBOLCanvas (Bug, Milestone 2.0) |
| #453 | Interaction edges | Interaction edges missing the options that interaction nodes have (Bug, Milestone 2.0) |
| #457 | External parts import | Can't import designs with unreachable external parts (Bug, Milestone 2.0) |
| #471 | VPR interactions | Add interactions to components and modules using VPR (Milestone 2.0) |
| #470 | Linked collections | Linked collection does not show up when importing parts (Bug, Milestone 2.0) |

**Takeaway:** The project is closing the gap between visual design and simulation (SBML linkage, modeling elements), and the import pipeline has rough edges that need stabilization before the v2.1 release.

---

### deeptools/deepTools (deep-sequencing analysis)

**Repo:** 765 ⭐ · **Language:** Python

| # | Issue | Description |
|---|---|---|
| #1459 | plotPCA regression | New SVD-based plotPCA writes bin scores instead of per-sample loadings (4.0.0 regression) |
| #1457 | bamCompare bug | Catch-all arm causes `--operation first/second/add/mean` to silently emit log2 ratio; `reciprocal_ratio` inverted |
| #1107 | plotCorrelation | xRange/yRange customization gap (long-standing) |

**Takeaway:** Correctness regressions in the 4.0.0 Rust re-implementation are alarming for scientific users — ground-up rewrites of numerical code need rigorous validation.

---

### broadinstitute/viral-ngs (viral NGS toolkit)

**Repo:** 197 ⭐ · **Language:** Python

| # | Issue | Description |
|---|---|---|
| #1101 | minibwa in Docker | Request to add minibwa aligner to the core Docker image |
| #1051 | Duplicate read IDs | Gap in FastqToUBAM for duplicate read ID handling |
| #1035 | Documentation | Effort to improve the RTD documentation |

**Takeaway:** The multi-flavor Docker image strategy (core / assemble / classify / phylo) is a notable pattern for bundling complex bioinformatics stacks.

---

## 🗺️ Community Resources & Curated Lists

| Resource | Stars | Description |
|---|---|---|
| [Awesome-Bioinformatics](https://github.com/danielecook/Awesome-Bioinformatics) | 4,098 | Curated list of bioinformatics libraries and software |
| [awesome-single-cell](https://github.com/seandavi/awesome-single-cell) | 3,748 | Software and data resources for single-cell omics |
| [iGEM Registry](https://parts.igem.org/) | — | Central repository of biological parts for the international iGEM competition |
| [SBOL Stack](https://sbols.org/) | — | Synthetic Biology Open Language — data model, visual notation, and repositories |

### 🌐 The SBTools Community

A cross-cutting thread across these projects is the **SBTools** (Synthetic Biology Tools) community, organized around a [Google Group](https://groups.google.com/g/sbtools/) and an active **Slack workspace** (channels like `#biocrnpyler`). This is the informal hub where synbio tool developers coordinate on standards (SBOL, SBML, Eugene), share best practices, and report cross-project bugs. BioCRNpyler's README explicitly references it, and the Cello authors are also active participants.

---

## 🌐 Key Themes in the Community

| # | Theme | Evidence |
|---|---|---|
| 1 | **Correctness of re-implemented backends** | deepTools 4.0.0 Rust rewrite introduced silent numerical/logic bugs (wrong PCA, broken bamCompare) |
| 2 | **Packaging & dependency delivery** | Bioconda + multi-stage Docker images (viral-ngs) to manage complex C/C++/Rust dependencies |
| 3 | **Parser fragility & dependency churn** | GFF3 parser in DnaFeaturesViewer broke when BCBio stagnated; GenBank parsers in Poly flagged for rewrite |
| 4 | **mRNA & therapeutic sequence design** | DnaChisel (uridine depletion, CAI), CodonTransformer, and CELLM reflect heavy mRNA therapeutics demand |
| 5 | **Bridging the hosted-service gap** | Cello-v2's cellocad.org login issues; SBOLCanvas production-maturity tasks — open-source academic tools lack DevOps for reliable hosted UX |
| 6 | **Reproducibility & provenance** | Nextflow lineage-tracking bugs; general move toward pipeline frameworks for cache/lineage tracking |
| 7 | **ML + sequence design convergence** | CodonTransformer, DeepBGC, CELLM — accelerating intersection of deep learning and biological sequence engineering |
| 8 | **RNA device engineering & cell-free systems** | BioCRNpyler's TMSE module; EnergyTXTL convergence bug; toehold-switch design tools from SASTRA-iGEM — growing interest in programmable RNA devices and cell-free expression as alternatives to in-vivo circuit characterization |
| 9 | **SBOL standard adoption** | SBOLCanvas roadmap (modeling elements, SBML linkage, feature annotations, part definitions) signals push toward richer, simulation-ready digital representations of genetic designs |
