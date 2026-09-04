# Episode Scripts Archive

Welcome to the **Episode Scripts Archive** — a project dedicated to storing, organizing, and preserving episode scripts, source materials, transcripts, and related content. This repository serves as a central hub for audiovisual content production, enabling creators, researchers, and collaborators to manage, version, and reuse script assets.

## Purpose & Scope

- **Centralize** episode scripts, show notes, source materials, and production assets in a single, version-controlled location
- **Preserve** content history through Git's branching and commit tracking
- **Collaborate** by providing a clear workflow for writers, editors, producers, and guests
- **Enable reuse** — modular script components can be repurposed across episodes
- **Document provenance** — every edit and contributor is tracked

---

## Research: Synthetic Biology & Biotech Software Tools

This archive tracks the ecosystem of **synthetic biology (synbio)** and **genetic engineering software**, profiled alongside live GitHub issue-tracker findings.

### 🧬 Genetic Circuit Design & CAD Tools

| Project | Stars | Language | Description |
|---|---|---|---|
| [CIDARLAB/cello](https://github.com/CIDARLAB/cello) | 877 | Java | Genetic circuit design automation using Verilog-like specifications |
| [MyersResearchGroup/iBioSim](https://github.com/MyersResearchGroup/iBioSim) | 67 | Java | CAD tool for genetic circuits; supports SBML and SBOL standards |
| [bebop/poly](https://github.com/bebop/poly) | 729 | Go | Go package for engineering organisms: codon optimization, primer design, synthesis fragment design |
| [khokao/synergetica](https://github.com/khokao/synergetica) | 118 | TypeScript | Desktop app for genetic circuit design with node-based interfaces |
| [Edinburgh-Genome-Foundry/DnaChisel](https://github.com/Edinburgh-Genome-Foundry/DnaChisel) | 274 | Python | DNA sequence optimizer; surging 2026 demand around mRNA therapeutics |
| [Edinburgh-Genome-Foundry/DnaFeaturesViewer](https://github.com/Edinburgh-Genome-Foundry/DnaFeaturesViewer) | 690 | Python | Plot DNA sequence features from GenBank/GFF files |
| [Adibvafa/CodonTransformer](https://github.com/Adibvafa/CodonTransformer) | 212 | Python | Transformer-based ML codon optimizer, 2M+ downloads |
| [SynBioHub/synbiohub](https://github.com/SynBioHub/synbiohub) | 84 | JavaScript | Web platform for sharing synthetic biology designs |
| [20n/act](https://github.com/20n/act) | 92 | Java | Predictive bioengineering: finding all biosynthesizable chemicals |

### 🔬 CRISPR & Guide RNA Design

| Project | Stars | Language | Description |
|---|---|---|---|
| [richysix/Crispr](https://github.com/richysix/Crispr) | 24 | Perl | CRISPR/Cas9 guide RNA design and analysis |
| [sunjiamin0824/CRISPR-Local](https://github.com/sunjiamin0824/CRISPR-Local) | 17 | Perl | Local sgRNA design for non-reference plant genomes |

### 🧬 Deep Learning & Genomics

| Project | Stars | Language | Description |
|---|---|---|---|
| [google/deepvariant](https://github.com/google/deepvariant) | 3,726 | Python | Google's deep learning pipeline for genetic variant calling |
| [Merck/deepbgc](https://github.com/Merck/deepbgc) | 158 | Jupyter Notebook | Deep learning for Biosynthetic Gene Cluster detection |

### 🧬 Bioinformatics Infrastructure

| Project | Stars | Language | Description |
|---|---|---|---|
| [biopython/biopython](https://github.com/biopython/biopython) | 5,070 | Python | Foundational Python toolkit for computational molecular biology |
| [nextflow-io/nextflow](https://github.com/nextflow-io/nextflow) | 3,412 | Groovy | DSL for reproducible bioinformatics pipelines |
| [MultiQC/MultiQC](https://github.com/MultiQC/MultiQC) | 1,491 | JavaScript | Bioinformatics QC report aggregator |

### 🔍 Live Issue-Tracker Snapshot (June 2026)

#### SynBioHub/synbiohub (84 ⭐)

| # | Issue | Label |
|---|---|---|
| 1756 | SubCollections not reporting members in public graph | bug |
| 1755 | Recursive download not following linked collections | bug |
| 1753 | OMEX download dropping attached SBML files | bug |
| 1752 | Visibility changes alter URL prefix (private→public) | — |
| 1746 | Incremental updates not working with SBOLExplorer | bug |

*Themes: data integrity, URL/visibility consistency, frontend-backend interoperability around the SBOL standard.*

#### MyersResearchGroup/iBioSim (67 ⭐)

| # | Issue | Age |
|---|---|---|
| 640 | Java exception on launch | 1 yr |
| 639 | Can't upload SynBioHub designs | 1 yr |
| 638 | Unable to run iBioSim 3.2.0 on Mac | 1 yr |
| 635 | Can't open iBioSim on Windows 11 | 2 yr |
| 634 | Bug importing files on startup | 2 yr |

*Themes: cross-platform compatibility rot (Mac/Win/Linux, 1-2 yr backlog), SynBioHub integration failures, maintenance bandwidth shortage.*

#### 20n/act (92 ⭐) & JBEI/ART (66 ⭐)
**Zero open issues.** Both reflect sustained, focused engineering — 20n/act predicted and invented the first bio-route to Acetaminophen; ART (multi-target MCMC strain recommender) keeps its source in a private repo under commercial-friendly licensing, limiting external contributions.

#### MultiQC/MultiQC (1,491 ⭐)

| # | Issue | Labels |
|---|---|---|
| 3535 | Exploration: use ECharts instead of Plotly | refactoring |
| 3616 | Add columns in Software Versions section | front end |
| 3603 | New module: cramino | module: new |

*Themes: healthy architectural modernization debate, continuous module onboarding — signs of growth at scale.*

### 🎯 Community Concerns Summary

1. **mRNA Therapeutics demand** — DnaChisel, CodonTransformer (2M+ downloads) reflect explosive mRNA/vaccines market pull.
2. **Parser fragility** — Bioinformatics parsers (GenBank, GFF3) break as upstream libraries lose maintenance.
3. **Cross-platform reliability** — Cello, iBioSim, CRISPR-Local need better Docker support and CI.
4. **Cloud dependency fragility** — Academic tools' web services and integrations go down with no DevOps.
5. **Maintenance debt** — Stale 1-2 year old issues at iBioSignal show academic tools lack sustainenance.
6. **Genome awareness gap** — Most tools assume a single reference; CRISPR-Local's non-reference approach is underserved.
7. **ML + sequence design** — CodonTransformer, DeepBGC, CELLM point to accelerating AI/biology convergence.
8. **ML-driven biology** — CodonTransformer, DeepBGC, CELLM represent growing ML/biology intersection.
9. **Accessibility vs. commercialization** — ART's closed-source and 20n/act's commercial-tied models show sustainability tensions.

---

## Structure

```
episode-scripts-archive/
├── README.md                  # This file
├── episodes/
│   ├── ep-001/
│   │   ├── script.md
│   │   ├── source-materials/
│   │   └── metadata.json
│   └── ep-002/
├── research/
│   ├── synbio-tools-survey-2026-06.md
│   └── community-issues-snapshot.md
├── templates/
├── assets/
└── docs/
```

## Contributing

1. Create a branch per episode or major update
2. Include `metadata.json` with episode details
3. Link or attach source materials, transcripts, show notes
4. Submit PRs for review before merging

## License

MIT License — see [LICENSE](LICENSE).

---

## Acknowledgments

Conceived alongside research into the open-source synthetic biology ecosystem: Cello's circuit engineering, CRISPR-Local's non-reference genome editing, iBioSim's SBML/SBOL modeling, SynBioHub's design-sharing platform, Opentrons' lab automation, DnaChisel's mRNA therapeutics optimizations, 20n/act's bioproduction route prediction, and JBEI's ML-driven strain recommendation. Their shared challenges — reliability, genome diversity, reproducibility, usability, maintenance — mirror every collaborative project's tensions.