<p align="center">
  <img src="https://raw.githubusercontent.com/cyanea-bio/assets/main/mascot.png" alt="Cyanea" width="160" />
</p>

<h3 align="center">GitHub for Life Sciences</h3>

<p align="center">
  Store datasets, protocols, experiments, and analyses.<br/>
  Version control everything. Collaborate openly. Own your data.
</p>

<p align="center">
  <a href="https://cyanea.bio">Website</a> &middot;
  <a href="https://docs.cyanea.bio">Docs</a> &middot;
  <a href="https://github.com/cyanea-bio/cyanea">Platform</a> &middot;
  <a href="https://github.com/cyanea-bio/labs">Labs</a>
</p>

---

### What is Cyanea?

Cyanea is an open-source, federated platform for life science R&D — what GitHub and Hugging Face did for code and ML, applied to **bioinformatics, protocols, and experimental artifacts**.

- **Cyanea Platform** — An Elixir/Phoenix app for storing, versioning, and sharing scientific artifacts (datasets, protocols, notebooks, pipelines). Self-hostable, federation-ready.
- **Cyanea Labs** — A Rust bioinformatics ecosystem: 13 crates covering sequence I/O, alignment, omics data structures, phylogenetics, GPU compute, WASM, and Python bindings.

### Repositories

| Repo | Description |
|------|-------------|
| [`cyanea`](https://github.com/cyanea-bio/cyanea) | Elixir/Phoenix platform — the core application |
| [`labs`](https://github.com/cyanea-bio/labs) | Rust bioinformatics libraries (Cargo workspace, 13 crates) |
| [`docs`](https://github.com/cyanea-bio/docs) | Documentation site (Zola) |
| [`www`](https://github.com/cyanea-bio/www) | Marketing website (Zola) |
| [`design`](https://github.com/cyanea-bio/design) | Design token system — single source of truth for colors, typography, spacing |
| [`assets`](https://github.com/cyanea-bio/assets) | Brand assets and media files |

### Architecture

```
Browser ── WASM (cyanea-wasm) ──┐
                                ▼
          Cyanea Platform (Elixir/Phoenix)
          LiveView · Channels · REST API · Oban
                       │
                       ▼
              Rustler NIFs (cyanea_native)
                       │
                       ▼
              Cyanea Labs (Rust)
   cyanea-seq · cyanea-align · cyanea-omics · ...
```

Rust libraries are consumed **server-side** via NIFs for heavy compute (parsing, alignment, hashing) and **client-side** via WASM for interactive browser tools (sequence viewers, local file preview).

### Built with

Elixir &middot; Phoenix LiveView &middot; Rust &middot; PostgreSQL &middot; Tailwind CSS &middot; WASM

---

<p align="center">
  <sub>Named after <em>Cyanea</em>, the genus of lion's mane jellyfish — a distributed nervous system, like networked research data.</sub>
</p>
