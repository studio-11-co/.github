<img src="https://raw.githubusercontent.com/studio-11-co/falsify/main/brand/lockup.svg" alt="falsify" width="280">

**PRML — Pre-Registered ML Manifests.** An open, content-addressed format for committing a machine-learning evaluation claim to a SHA-256 hash *before* the experiment runs. Lock the threshold before the data, or it didn't happen.

A verifier recomputes the digest from the manifest's canonical bytes and emits a deterministic verdict: **PASS / FAIL / TAMPERED**. Moving the bar after the results exist produces a detectable hash mismatch. It proves the bar was locked, never the result.

- **Spec:** [spec.falsify.dev/v0.1](https://spec.falsify.dev/v0.1) · CC BY 4.0 · [Zenodo DOI](https://doi.org/10.5281/zenodo.20177839)
- **Site:** [falsify.dev](https://falsify.dev) · **Registry:** [registry.falsify.dev](https://registry.falsify.dev) — Ed25519-signed receipts, independent RFC 3161 timestamps, mirrored to the Rekor transparency log
- **Listed on the [UK AI Safety Institute's Inspect extensions page](https://github.com/UKGovernmentBEIS/inspect_ai/pull/4440)** · JSON Schema in [SchemaStore](https://github.com/SchemaStore/schemastore/pull/5673) · JOSS paper under review
- Crosswalks: **EU AI Act** technical documentation (Art. 11 / Annex IV, retention Art. 18) · NIST AI RMF · ISO/IEC 42001

### Proof, not promises
**4 reference implementations** (Python, JavaScript, Go, Rust), byte-equivalent across **21 conformance vectors** and rejecting a shared **14-vector negative suite**. MIT code, CC BY 4.0 spec, ~600 tests, OpenSSF Best Practices passing.

### Repositories
| | |
|---|---|
| **[falsify](https://github.com/studio-11-co/falsify)** | Spec + Python reference + conformance suite (Go/JS/Rust under `impl/`) |
| **[falsify-js](https://github.com/studio-11-co/falsify-js)** | JavaScript reference (npm: `falsify-js`) |
| **[prml-verify-action](https://github.com/studio-11-co/prml-verify-action)** | GitHub Action: gate CI on tampered or regressed eval claims |
| **[mlflow-falsify](https://github.com/studio-11-co/mlflow-falsify)** | MLflow plugin: bind runs to their locked bar, verify on run end |
| **[falsify-inspect](https://github.com/studio-11-co/falsify-inspect)** | Inspect AI adapter (on the UK AISI extensions page) |
| **[falsify-giskard](https://github.com/studio-11-co/falsify-giskard)** | Giskard scenario adapter |
| **[falsify-cookbook](https://github.com/studio-11-co/falsify-cookbook)** | Patterns, anti-patterns, worked examples (CC0) |
| **[falsify-integrity-index](https://github.com/studio-11-co/falsify-integrity-index)** | Scorecard: 27 well-known eval claims vs 9 falsifiability criteria |

Running a benchmark or leaderboard? **[Require a receipt](https://falsify.dev/require/)** — no locked claim, no entry.

Maintained by Cüneyt Öztürk · [hello@falsify.dev](mailto:hello@falsify.dev)
