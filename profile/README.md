## PRML / falsify

**Pre-Registered ML Manifests** — an open, content-addressed format for committing a machine-learning evaluation claim to a SHA-256 hash *before* the experiment runs. Lock the threshold before the data, or it didn't happen.

A verifier with the manifest, the dataset, and the model independently recomputes the digest and emits a deterministic verdict: **PASS / FAIL / TAMPERED**. Tampering produces a detectable hash mismatch.

- **Spec:** [spec.falsify.dev/v0.1](https://spec.falsify.dev/v0.1) — CC BY 4.0, v0.2 frozen
- **Site:** [falsify.dev](https://falsify.dev) · **Registry:** [registry.falsify.dev](https://registry.falsify.dev)
- **Citable:** Zenodo DOI [10.5281/zenodo.20177839](https://doi.org/10.5281/zenodo.20177839)
- Maps to **EU AI Act** Articles 12/15/18/50, NIST AI RMF, ISO/IEC 42001

### Proof, not promises
- **4 reference implementations** (Python, JavaScript, Go, Rust) — byte-equivalent across **21 conformance vectors** (13 v0.1 stable + 8 v0.2)
- MIT-licensed code · CC BY 4.0 spec · JSON Schema in SchemaStore

### Repositories
- **[falsify](https://github.com/studio-11-co/falsify)** — spec + Python reference + conformance suite (Go/JS/Rust under `impl/`)
- **[falsify-js](https://github.com/studio-11-co/falsify-js)** — JavaScript reference (npm: `falsify-js`)
- **[mlflow-falsify](https://github.com/studio-11-co/mlflow-falsify)** — MLflow plugin: auto-tag every run with its PRML manifest hash
- **[prml-verify-action](https://github.com/studio-11-co/prml-verify-action)** — GitHub Action: gate CI on tampered/regressed eval claims
- **[falsify-inspect](https://github.com/studio-11-co/falsify-inspect)** — adapter for Inspect AI eval logs
- **[falsify-cookbook](https://github.com/studio-11-co/falsify-cookbook)** — patterns, anti-patterns, worked examples (CC0)
- **[falsify-integrity-index](https://github.com/studio-11-co/falsify-integrity-index)** — public scorecard of how published ML eval claims meet falsifiability criteria

Maintained by Cüneyt Öztürk · [hello@falsify.dev](mailto:hello@falsify.dev)
