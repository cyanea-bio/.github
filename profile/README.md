<p align="center">
  <img src="https://cyanea.bio/mascot.png" alt="Cyanea" width="160" />
</p>

<h3 align="center">The Open Community for Life Science Research</h3>

<p align="center">
  Share datasets, protocols, and experiments. Version everything.<br/>
  Collaborate openly. Built by scientists, for scientists.
</p>

<p align="center">
  <a href="https://cyanea.bio">Website</a> &middot;
  <a href="https://app.cyanea.bio">App</a> &middot;
  <a href="https://docs.cyanea.bio">Docs</a> &middot;
  <a href="https://cyanea.bio/blog">Blog</a> &middot;
  <a href="https://app.cyanea.bio/status">Status</a>
</p>

---

### What is Cyanea?

Cyanea is an open-source, federated platform for life science R&D. Store, version, and share datasets, protocols, notebooks, and pipelines. Self-hostable, federation-ready, with a Rust-powered compute layer that runs natively and in the browser via WASM.

- **[Cyanea Platform](https://github.com/cyanea-bio/cyanea)** — Elixir/Phoenix web application with interactive notebooks (dual WASM + server execution), REST API, CLI tool, real-time collaboration, and a full billing system. SQLite or PostgreSQL.
- **[Cyanea Labs](https://github.com/cyanea-bio/labs)** — 15 Rust crates covering sequences, alignment, omics, statistics, ML, chemistry, structural biology, phylogenetics, metagenomics, epigenomics, GPU compute, file I/O, WASM bindings, and Python bindings. 3,700+ tests.

### Open Source Repositories

| Repo | Description |
|------|-------------|
| [`cyanea`](https://github.com/cyanea-bio/cyanea) | Elixir/Phoenix platform with LiveView, Rust NIFs, and WASM compute |
| [`labs`](https://github.com/cyanea-bio/labs) | Rust bioinformatics ecosystem (Cargo workspace, 15 crates, 3,700+ tests) |

### Architecture

```
Browser ── WASM (cyanea-wasm) ──┐
                                ▼
          Cyanea Platform (Elixir/Phoenix)
          LiveView · REST API · Oban · PubSub
                       │
                       ▼
              Rustler NIFs (cyanea_native)
                       │
                       ▼
              Cyanea Labs (Rust)
   seq · align · omics · stats · ml · chem
   struct · phylo · meta · epi · io · gpu
```

Rust libraries are consumed **server-side** via NIFs for heavy compute (parsing, alignment, hashing) and **client-side** via WASM for interactive browser tools (sequence viewers, notebook execution, local file preview).

### Labs Crates

| Crate | Domain |
|-------|--------|
| `cyanea-core` | Shared primitives, hashing, compression |
| `cyanea-seq` | Sequence I/O, manipulation, k-mers, indexing |
| `cyanea-align` | Pairwise and multiple sequence alignment, GPU dispatch |
| `cyanea-omics` | Expression matrices, variants, genomic intervals, single-cell |
| `cyanea-stats` | Descriptive stats, hypothesis testing, PCA, distributions |
| `cyanea-ml` | Clustering, dimensionality reduction, KNN, embeddings |
| `cyanea-chem` | SMILES/SDF parsing, fingerprints, molecular properties |
| `cyanea-struct` | PDB/mmCIF parsing, secondary structure, superposition |
| `cyanea-phylo` | Newick/NEXUS I/O, tree building, ancestral reconstruction |
| `cyanea-meta` | Metagenomics: taxonomy, diversity, functional annotation |
| `cyanea-epi` | Epigenomics: peak calling, motifs, chromatin states |
| `cyanea-io` | Unified file format parsers (CSV, VCF, BED, GFF, SAM) |
| `cyanea-gpu` | GPU compute abstraction (CUDA/Metal) |
| `cyanea-wasm` | Browser runtime and JavaScript bindings |
| `cyanea-py` | Python bindings via PyO3 |

### Built with

Elixir &middot; Phoenix LiveView &middot; Rust &middot; SQLite &middot; Tailwind CSS &middot; WASM &middot; S3

---

<p align="center">
  <sub>Named after <em>Cyanea</em>, a genus of jellyfish. Among jellyfish are the only known organisms capable of biological immortality. The quest for eternal life is as old as humanity itself, and the life sciences are its most promising modern pursuit.</sub>
</p>
