<a href="https://falsify.dev"><img src="https://raw.githubusercontent.com/studio-11-co/falsify/main/brand/hero.png" alt="falsify: fix the pass bar before the test runs. Anyone can check it later." width="100%"></a>

[![PyPI](https://img.shields.io/pypi/v/falsify?label=pypi%20falsify&color=2ea44f&style=flat-square)](https://pypi.org/project/falsify/)
[![npm](https://img.shields.io/npm/v/falsify-js?label=npm%20falsify-js&color=2ea44f&style=flat-square)](https://www.npmjs.com/package/falsify-js)
[![CI](https://img.shields.io/github/actions/workflow/status/studio-11-co/falsify/falsify.yml?branch=main&label=CI&style=flat-square)](https://github.com/studio-11-co/falsify/actions/workflows/falsify.yml)
[![Multi-lang Conformance](https://img.shields.io/github/actions/workflow/status/studio-11-co/falsify/multi-lang-conformance.yml?branch=main&label=conformance%20%C2%B7%204%20languages&style=flat-square)](https://github.com/studio-11-co/falsify/actions/workflows/multi-lang-conformance.yml)
[![OpenSSF Best Practices](https://img.shields.io/cii/level/13539?label=OpenSSF%20best%20practices&style=flat-square)](https://www.bestpractices.dev/projects/13539)
[![IANA](https://img.shields.io/badge/IANA-application%2Fvnd.prml%2Byaml-555?style=flat-square)](https://www.iana.org/assignments/media-types/application/vnd.prml+yaml)
[![DOI](https://img.shields.io/badge/DOI-10.5281%2Fzenodo.20177839-blue?style=flat-square)](https://doi.org/10.5281/zenodo.20177839)
[![live example](https://img.shields.io/badge/live%20example-SynthID--Text%20receipt-39D98A?style=flat-square)](https://falsify.dev/receipts/synthid-text-2026-10/)

**PRML** is an open format for writing down, before a test runs, what the test has to achieve: metric, comparator, threshold, dataset hash, seed. A verifier recomputes the SHA-256 digest from the manifest's canonical bytes and returns **PASS**, **FAIL** or **TAMPERED**. The public registry adds Ed25519-signed receipts, independent RFC 3161 timestamps and a Rekor transparency-log entry. A receipt shows that the bar existed no later than the timestamp and whether a later copy is byte-identical to it. It never shows that a result is true.

**Live example:** [a pre-registered robustness evaluation of the open-source SynthID-Text watermark](https://falsify.dev/receipts/synthid-text-2026-10/), with six pass bars timestamped before the main run and the results reported against them: 8 of 12 outcomes met.

- **Spec:** [spec.falsify.dev/v0.1](https://spec.falsify.dev/v0.1) · [Community Specification License 1.0](https://github.com/studio-11-co/falsify/blob/main/spec/LICENSE.md) · [Zenodo DOI](https://doi.org/10.5281/zenodo.20177839)
- **Site:** [falsify.dev](https://falsify.dev) · **Registry:** [registry.falsify.dev](https://registry.falsify.dev)
- **Registered and listed:** IANA media type [`application/vnd.prml+yaml`](https://www.iana.org/assignments/media-types/application/vnd.prml+yaml) · `prml` namespace in the [OWASP CycloneDX property taxonomy](https://github.com/CycloneDX/cyclonedx-property-taxonomy/pull/193) · JSON Schema in [SchemaStore](https://github.com/SchemaStore/schemastore/pull/5673) · [UK AI Security Institute's Inspect extensions page](https://github.com/UKGovernmentBEIS/inspect_ai/pull/4440) · [OECD.AI catalogue of tools](https://oecd.ai/en/catalogue/tools/prml-%E2%80%94-pre-registered-ml-manifest-specification). Listings and registry entries, not endorsements.
- **Crosswalks:** EU AI Act technical documentation (Art. 11 / Annex IV, retention Art. 18) · NIST AI RMF · ISO/IEC 42001

### Proof, not promises
**4 reference implementations** (Python, JavaScript, Go, Rust), byte-equivalent across **21 conformance vectors**, all rejecting the same **20 negative vectors**, plus a **92-vector edge suite** derived from the formal grammar. MIT code, Community Specification License 1.0 for the spec, 646 tests in CI, OpenSSF Best Practices passing.

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

Running a benchmark or leaderboard? **[Require a receipt](https://falsify.dev/require/)**: no locked claim, no entry.

Falsify OÜ, Tallinn · [hello@falsify.dev](mailto:hello@falsify.dev)
