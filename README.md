# 🧬 Episode Scripts Archive

> A structured archive for storing episode scripts, source materials, research notes, and reference links — covering topics in **synthetic biology**, **biotech software tools**, and adjacent open-source communities.

---

## 📁 Repository Purpose

This archive serves as a centralized home for:

- **Episode scripts** — full write-ups and outlines for episodes covering science, technology, and open-source topics
- **Source materials** — research notes, citations, GitHub issue threads, and community discussions consulted during episode prep
- **Reference links** — curated pointers to key projects, papers, and communities
- **Background research** — snapshots of the open-source landscape at the time of each episode's production

---

## 🔬 Synthetic Biology & Biotech Software Tools Landscape

The following open-source projects represent the active frontier of computational synthetic biology and bioinformatics tooling on GitHub. These were surveyed as part of episode research, with a close read of each project's live issue tracker to surface what the community is currently concerned about or actively working on.

---

### 🏆 Top Synthetic Biology Tools

#### 1. [Cello — CIDARLAB/cello](https://github.com/CIDARLAB/cello) ⭐ 873
**Language:** Java | **License:** BSD-2-Clause

Cello is a **genetic circuit design automation** tool. It takes high-level logic specifications written in **Verilog** (a hardware description language) and compiles them into biological implementations. The workflow includes:
- Logic synthesis from truth tables → AND-Inverter Graphs → NOR-Inverter Graphs
- Gate assignment using breadth-first search, hill climbing, or simulated annealing
- Physical plasmid/DNA layout generation via the Eugene language

> **Active Issues:** The community is reporting login/authentication issues with the hosted web platform at cellocad.org, as well as compilation errors in local deployments — suggesting friction between the hosted service and the open-source codebase. Some long-standing issues around Linux/NetSynth compatibility and Docker build failures (matplotlib errors) remain open, indicating the tooling is aging and needs maintenance attention.

#### 2. [SynBioHub — SynBioHub/synbiohub](https://github.com/SynBioHub/synbiohub) ⭐ 84
**Language:** JavaScript (Node.js + Java backend) | **License:** BSD-2-Clause

SynBioHub is a **web-based repository for browsing, uploading, and sharing synthetic biology designs**. It powers public instances like synbiohub.org (enriched _B. subtilis_, _E. coli_ features, and the iGEM Registry of Standard Biological Parts). It stores data in OpenLink Virtuoso and serves designs via the SBOL standard.

> **Active Issues (as of Sept 2026):** This is a **healthily active** project with a swarm of recent, labeled issues targeted at the upcoming **SBH 1.6.2** release. Current community focus:
> - Correctly handling recursive downloads that follow linked collections (#1755)
> - Deleting outdated legacy data stored in Virtuoso (#1754)
> - OMEX downloads not pulling attached SBML files (#1753)
> - Public-collection visibility toggles accidentally changing URL prefixes (#1752)
> - SubCollection membership reporting in the public graph (#1756)
> - Incremental update support for SBOLExplorer (#1746)
> - SBOLCanvas layout handling for root-collection filters (#1745)
> - Backend OR-parsing for SPARQL queries (#1744)

#### 3. [20n/act](https://github.com/20n/act) ⭐ 92
**Language:** Java (Scala stack) | **License:** GPL-3.0

20n/act is a **computational / predictive bioengineering** platform: given a target molecule, it predicts the DNA insertions into a host (e.g. _E. coli_, _S. cerevisiae_) that enable the cell to produce that molecule by fermentation. It predicted/invented the first biosynthetic route to acetaminophen (Tylenol). Issue tracker is **closed/private** (no open issues — the team keeps development closed and offers an enterprise-licensed DB), but the public codebase covers reaction-operator inference, biointerpretation, reachables/cascades computation, and DNA design.

---

### 🧬 Related & Emerging Biotech Infrastructure

| Project | ⭐ Stars | Language | Role |
|---|---|---|---|
| [bebop/poly](https://github.com/bebop/poly) | 729 | Go | Modern Go package for engineering organisms — codon optimization, primer design, circular hashing, GenBank/FASTA I/O |
| [khokao/synergetica](https://github.com/khokao/synergetica) | 118 | TypeScript | Desktop genetic-circuit designer with a node-based UI |
| [Edinburgh-Genome-Foundry/DnaChisel](https://github.com/Edinburgh-Genome-Foundry/DnaChisel) | 274 | Python | DNA sequence optimizer; demand rising around mRNA therapeutics |
| [Edinburgh-Genome-Foundry/DnaFeaturesViewer](https://github.com/Edinburgh-Genome-Foundry/DnaFeaturesViewer) | 690 | Python | Plot DNA sequence features from GenBank/GFF |
| [Adibvafa/CodonTransformer](https://github.com/Adibvafa/CodonTransformer) | 212 | Python | Transformer-based ML codon optimizer (2M+ downloads) |
| [MyersResearchGroup/iBioSim](https://github.com/MyersResearchGroup/iBioSim) | 67 | Java | CAD tool for genetic circuits; SBML/SBOL support |

**Genomics / CRISPR tooling (for sourcing & editing context):**

| Project | ⭐ Stars | Language | Role |
|---|---|---|---|
| [google/deepvariant](https://github.com/google/deepvariant) | 3,726 | Python | Deep-learning genetic variant calling |
| [Merck/deepbgc](https://github.com/Merck/deepbgc) | 158 | Jupyter | Deep learning for biosynthetic gene cluster detection |
| [richysix/Crispr](https://github.com/richysix/Crispr) | 24 | Perl | CRISPR/Cas9 guide RNA design and analysis |
| [sunjiamin0824/CRISPR-Local](https://github.com/sunjiamin0824/CRISPR-Local) | 17 | Perl | Local sgRNA design for non-reference plant genomes |

---

### 📋 What the Community Is Currently Concerned About (Cross-Project Themes)

Synthesizing the live issue-trackers surveyed above, several recurring themes emerge:

1. **Platform/service vs. open-source divergence** — Hosted web platforms (cellocad.org / SynBioHub instances) drift from the open-source repos; users hit login, build, and deployment mismatches (Cello #63, #61, #50; SynBioHub #1752, #1753).
2. **Data lifecycle & correctness** — Managing legacy data, recursive collection traversal, and attached-file completeness in multi-part downloads remain live concerns (SynBioHub #1754, #1755, #1753).
3. **Standards compliance & interoperability** — SBOL/SBML/OMEX handling and correct parsing (SPARQL OR semantics, SBOLCanvas layouts) dominate current SynBioHub development (#1744, #1745, #1746).
4. **Maintenance debt** — Aging codebases (Cello's NetSynth/Linux/Docker issues from 2018–2023) show that long-lived CAD tools often lack ongoing upkeep, leaving broken builds for new users.
5. **Modernization via ML** — Enzymatic pathway prediction (20n/act), codon optimization (CodonTransformer), and variant calling (DeepVariant) reflect a broader shift towards data-driven / ML-augmented bioengineering.

---

### 🌐 Communities & Hubs

- **iGEM / Registry of Standard Biological Parts** — foundational shared-parts ecosystem (mirrors in SynBioHub).
- **SynBioBench / SynBioDex** — standards testing (SBOLTestSuite) backing tools like SynBioHub.
- **Broad / Edinburgh Genome Foundry** — open CAD tooling (DnaChisel, DnaFeaturesViewer).
- **20n** — predictive/mechanistic bioengineering research (commercial-licensed core).

---

## 📚 Contents (planned structure)

- `episodes/` — individual episode scripts and show notes
- `source-materials/` — research notes, transcripts, citations
- `synthetic-biology/` — synbio/biotech-specific episode research (this `README.md`, tooling notes, issue-tracker snapshots)
- `reference-links/` — curated links to projects, papers, and communities

---

## 🤝 Contributing

Contributions, corrections, and episode submissions are welcome. Please fork the repository, propose changes via a pull request, and ensure scripts/links are organized under the appropriate topic folder.

---

## 📜 License

This archive is shared for research and reference purposes. See individual project licenses (linked above) for third-party tooling.
