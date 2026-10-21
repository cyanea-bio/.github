<p align="center">
  <a href="https://cyanea.bio">
    <img src="https://raw.githubusercontent.com/cyanea-bio/.github/main/profile/banner.png" alt="Cyanea: the system of record for computational biology. Versioned, reproducible, provenance-tracked notebooks. Open source." width="100%">
  </a>
</p>

<p align="center">
  <a href="https://cyanea.bio">Website</a> &middot;
  <a href="https://docs.cyanea.bio">Docs</a> &middot;
  <a href="https://cyanea.bio/learn">Learn</a> &middot;
  <a href="https://cyanea.bio/blog">Blog</a> &middot;
  <a href="https://cyanea.bio/status">What's live</a> &middot;
  <a href="https://app.cyanea.bio">Open the app</a>
</p>

---

### The system of record for computational biology

Cyanea keeps notebooks, datasets and protocols versioned, provenance-tracked and re-runnable. Open an analysis, press run, get the same answer; follow any number back through cells, code versions and datasets to the raw files it came from.

- **Re-run.** Notebooks execute in the browser or on server compute with pinned inputs, so last year's result still reproduces.
- **Trace.** Every output has a lineage you can follow.
- **Review.** Cell-level diffs between versions, so a changed parameter is visible before it reaches a paper.
- **Federate.** Self-host an instance next to sensitive data and share the method, not the files.

Cyanea is open source and in public alpha. [See what's live today.](https://cyanea.bio/status)

### Open-source repositories

| Repository | What it is |
|---|---|
| [`cyanea`](https://github.com/cyanea-bio/cyanea) | The platform: a Phoenix LiveView app with versioned notebooks, datasets and protocols, a REST API, real-time collaboration and Rust NIFs for heavy compute. Self-hostable, SQLite or PostgreSQL. |
| [`labs`](https://github.com/cyanea-bio/labs) | Cyanea Labs: 18 Rust crates for sequences, alignment, omics, statistics, machine learning, chemistry, structures, phylogenetics, metagenomics, epigenomics, proteomics and networks. Native, WebAssembly (`@cyanea/bio`) and Python (`cyanea`). Apache 2.0. |

### How it fits together

```
Browser ── WebAssembly (cyanea-wasm) ──┐
                                       ▼
            Cyanea platform (Elixir / Phoenix)
         LiveView · REST API · Oban · PubSub · CLI
                         │
                         ▼
               Rustler NIFs (cyanea_native)
                         │
                         ▼
                  Cyanea Labs (Rust)
   seq · align · io · omics · stats · ml · chem · struct
   phylo · meta · epi · proteomics · network · gpu
```

The same Rust libraries run on the server through NIFs (parsing, alignment, hashing) and in the browser through WebAssembly (notebook cells, sequence viewers, local file previews), so a result computed in either place matches the other.

### Learn biology by running it

[cyanea.bio/learn](https://cyanea.bio/learn) has lessons from the cell to the genome, each with code you can run and a simulation you can break: transcription, sequence alignment, k-mer spectra, phylogenetic trees, p-values and more. No install needed.

### Get involved

- Found a bug? Open an issue on [`cyanea`](https://github.com/cyanea-bio/cyanea/issues) or [`labs`](https://github.com/cyanea-bio/labs/issues).
- Writing about Cyanea? The [press kit](https://cyanea.bio/press) has the marks, colours and type.
- Anything else: [cyanea.bio/contact](https://cyanea.bio/contact).

---

<p align="center">
  <img src="https://raw.githubusercontent.com/cyanea-bio/.github/main/brand/mark-colour.svg" alt="" width="40"><br>
  <sub>Named for <i>Cyanea capillata</i>, the lion's mane jellyfish: long reach, lots of threads.</sub>
</p>
