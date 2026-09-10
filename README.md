# 🎬 Episode Scripts Archive

A curated archive for storing episode scripts and associated source materials (research notes, references, tooling context, and community discussions). This repository is organized for version-controlled collaboration on audiovisual and written episode content.

## 📁 Repository Purpose

- **Centralize** episode scripts, show notes, source materials, and production assets in a single, version-controlled location
- **Preserve** content history through Git's branching and commit tracking
- **Collaborate** by providing a clear workflow for writers, editors, producers, and guests
- **Enable reuse** — modular script components can be repurposed across episodes
- **Document provenance** — every edit and contributor is tracked
- **Anchor research** — each episode's notes tie back to real, live open-source projects and the concerns bubbling up in their issue trackers

## 🔬 Synthetic Biology & Biotech Software Tools (Research Survey)

This archive keeps a running snapshot of the GitHub-based **synthetic biology (synbio)** and **biotech software** ecosystem, with a live eye on each project's open issues. The projects below were surveyed as part of episode research, with several investigated in depth.

### 🏆 Synthesized Landscape (high-activity / high-relevance tools)

| Project | Stars | Language | What it does |
|---|---|---|---|
| [deeptools/deepTools](https://github.com/deeptools/deepTools) | 765 | Python | Process & analyze deep-sequencing data (normalization, coverage, visualization) |
| [google/deepvariant](https://github.com/google/deepvariant) | 3,726 | Python | Deep-learning variant calling from NGS data |
| [biopython/biopython](https://github.com/biopython/biopython) | 5,070 | Python | Foundational Python toolkit for computational molecular biology |
| [nextflow-io/nextflow](https://github.com/nextflow-io/nextflow) | 3,412 | Groovy | DSL for reproducible, scalable bioinformatics pipelines |
| [Edinburgh-Genome-Foundry/DnaFeaturesViewer](https://github.com/Edinburgh-Genome-Foundry/DnaFeaturesViewer) | 690 | Python | Plot DNA sequence features from GenBank/GFF files |
| [bebop/poly](https://github.com/bebop/poly) | 729 | Go | Go package for engineering organisms (codon optimization, primer design, synthesis fragments) |
| [Edinburgh-Genome-Foundry/DnaChisel](https://github.com/Edinburgh-Genome-Foundry/DnaChisel) | 274 | Python | DNA sequence optimizer (expression, synthesis, mRNA constraints) |
| [Adibvafa/CodonTransformer](https://github.com/Adibvafa/CodonTransformer) | 212 | Python | Transformer-based ML codon optimizer (2M+ downloads) |
| [broadinstitute/viral-ngs](https://github.com/broadinstitute/viral-ngs) | 197 | Python | Command-line viral NGS toolkit (assembly, classification, phylogenetics) |
| [deeptools/HiCExplorer](https://github.com/deeptools/HiCExplorer) | 276 | Python | Process, normalize & visualize Hi-C data |
| [RafsanjaniHub/PyFeat](https://github.com/RafsanjaniHub/PyFeat) | 97 | Python | Feature generation from DNA, RNA & protein sequences |
| [CIDARLAB/Cello-v2](https://github.com/CIDARLAB/Cello-v2) | 74 | Java | Genetic circuit design automation (successor to the original Cello) |
| [MyersResearchGroup/iBioSim](https://github.com/MyersResearchGroup/iBioSim) | 67 | Java | CAD for genetic circuits; SBML/SBOL support |
| [khokao/synergetica](https://github.com/khokao/synergetica) | 118 | TypeScript | Node-based desktop app for genetic circuit design |
| [lexO-dat/CELLM](https://github.com/lexO-dat/CELLM) | 2 | Python | AI-powered bridge between synthetic biology and natural-language processing |
| [SynBioHub/synbiohub](https://github.com/SynBioHub/synbiohub) | 84 | JavaScript | Web platform for sharing synthetic biology designs |
| [20n/act](https://github.com/20n/act) | 92 | Java | Predictive bioengineering (biosynthesizable chemical discovery) |
| [Merck/deepbgc](https://github.com/Merck/deepbgc) | 158 | Jupyter Notebook | Deep learning for Biosynthetic Gene Cluster detection |

### 🧬 In-Depth Investigation (open issues reviewed)

#### CIDARLAB/Cello-v2 (genetic circuit design automation)
The community is currently raising: a **licensing question** around Cello-v2 and its Docker-based DNACompiler image (#50); persistent **login/account creation failures** on the hosted `cellocad.org` platform (#48, #49); requests for **sequential logic** support (#47); and a long-standing feature request for **GFF / APE / FASTA output** (#26). Taken together, these point to friction between the **open-source CLI** and the **hosted web service** — a common theme across academic synbio tooling.

#### deeptools/deepTools (deep-sequencing analysis)
Recent open issues expose **correctness regressions introduced in the 4.0.0 Rust re-implementation**: a new SVD-based `plotPCA` that writes **bin scores instead of per-sample loadings** by default (#1459); a `bamCompare` catch-all arm that causes `--operation first/second/add/mean` to silently emit the **log2 ratio**, plus an inverted `reciprocal_ratio` (#1457); and a long-standing `plotCorrelation` **xRange/yRange** customization gap (#1107). These are high-priority correctness items for users upgrading to 4.0.0.

#### broadinstitute/viral-ngs (viral NGS toolkit)
Active work centers on **packaging & delivery**: a request to add the new **minibwa** short-read aligner to the core Docker image and expose it in `align_and_fix` / `align_and_plot_coverage` (#1101); a **duplicate read ID** handling gap in `FastqToUBAM` (#1051); and an effort to **improve the RTD documentation** (#1035). The project's multi-flavor Docker image strategy (core / assemble / classify / phylo) is a notable pattern for bundling complex bioinformatics stacks.

#### RafsanjaniHub/PyFeat (sequence feature generation)
A focused feature-generation tool for DNA/RNA/protein sequences using permutation-based and information-theoretic features, paired with optional ML classification — illustrative of the lightweight, scriptable ML-adjacent tooling growing in the bioinformatics space.

### 🗺️ Community Resources & Curated Lists

| Resource | Stars | Description |
|---|---|---|
| [Awesome-Bioinformatics](https://github.com/danielecook/Awesome-Bioinformatics) | 4,098 | Curated list of bioinformatics libraries and software |
| [awesome-single-cell](https://github.com/seandavi/awesome-single-cell) | 3,748 | Software and data resources for single-cell omics |

## 🌐 Key Themes in the Community (from open issue surveys)

Across these projects, the synbio/biotech open-source community is currently focused on:

1. **Correctness of re-implemented backends** — The deepTools 4.0.0 Rust rewrite introduced silent numerical/logic bugs (wrong PCA output, broken bamCompare operations), underscoring how risky ground-up rewrites are for scientific computation.
2. **Packaging & dependency delivery** — Tooling increasingly ships via **Bioconda + multi-stage Docker images** (viral-ngs) to manage complex C/C++/Rust dependencies; requests center on adding new aligners without breaking existing images.
3. **Parser fragility & dependency churn** — The GFF3 parser in DnaFeaturesViewer broke when BCBio ended active development; GenBank parsers in Poly are flagged for rewrite — a recurring cost of relying on unmaintained upstream libraries.
4. **mRNA & therapeutic sequence design** — DnaChisel (uridine depletion, CAI), CodonTransformer, and CELLM reflect heavy demand from the mRNA therapeutics/vaccine space.
5. **Bridging the hosted-service gap** — Cello-v2's `cellocad.org` login issues and SynBioHub edge cases reveal that open-source academic tools often lack the DevOps backing for reliable hosted experiences.
6. **Reproducibility & provenance** — Nextflow lineage-tracking bugs and the general move toward pipeline frameworks highlight how critical cache/lineage tracking has become for scientific reuse.
7. **ML + sequence design convergence** — CodonTransformer, DeepBGC, and CELLM point to an accelerating intersection of deep learning and biological sequence engineering.

## 📂 Archive Structure (proposed)

```
episode-scripts-archive/
├── episodes/
│   └── EPXXX-title/
│       ├── script.md
│       ├── sources.md
│       └── assets/
├── research/
│   ├── synbio-tools-survey-2026-09.md
│   └── community-issues-snapshot.md
├── templates/
│   ├── episode-script-template.md
│   └── sources-template.md
└── README.md
```

## 🔗 Quick Reference Links

- [Cello CAD](http://www.cellocad.org/) — Hosted genetic circuit design tool
- [Biopython Docs](https://biopython.org/docs/latest/) — Full tutorial and API reference
- [Opentrons Protocol Library](https://protocols.opentrons.com/) — Community-shared lab-automation protocols
- [nf-core](https://nf-co.re/) — Curated Nextflow pipelines for bioinformatics
- [CELLM (synbio + NLP)](https://github.com/lexO-dat/CELLM) — AI bridge for synthetic biology
- [Edinburgh Genome Foundry](https://edinburgh-genome-foundry.github.io/) — Suite of Python tools for DNA design

---

*Last research update: September 2026*
