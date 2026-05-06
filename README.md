# ThessMesh Survey

[![License: CC BY 4.0](https://img.shields.io/badge/License-CC_BY_4.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](CONTRIBUTING.md)

A practitioner's survey of ML 3D reconstruction — feed-forward methods, 3DGS variants, hybrid pipelines, scalability, and the industrial landscape.

This survey is the companion to the [ThessMesh library](https://github.com/OpenThessMesh/thessmesh). Where existing academic surveys are researcher-to-researcher, this one is engineer-to-engineer: focused on what works in practice, how methods connect into real pipelines, and what the gap is between benchmark performance and real-world deployment.

> **Status:** 🚧 Work in progress — actively being built. Contributions welcome.

---

## What this survey covers

- **Feed-forward reconstruction** — methods that estimate geometry and camera poses in a single forward pass (DUSt3R, VGGT, and their derivatives)
- **Per-scene neural rendering & 3DGS** — scene-specific optimisation methods and Gaussian splatting variants
- **Hybrid pipelines** — methods combining feed-forward initialisation with per-scene optimisation; the design space ThessMesh occupies
- **Scalability** — large-scale reconstruction at scales that challenge current feed-forward models
- **Industrial & commercial landscape** — what exists, what it does, and where the open-source gaps are
- **Datasets & benchmarks** — and the gap between benchmark conditions and real-world deployment
- **Classical SfM/MVS** — context and baseline for everything above

## What makes this different

Most surveys in this space take a paradigm-centric view — feed-forward vs. per-scene optimisation. This survey takes a **pragmatic hybridisation** perspective: feed-forward methods win on generalisation and speed; per-scene optimisation still wins on reconstruction quality. For real workloads — drone surveys of construction sites, robot navigation, cultural heritage digitisation at scale — neither paradigm alone is the answer. This survey documents both, and the methods that combine them.

---

## Navigation

| Category | Papers | Status |
|---|---|---|
| [Feed-forward reconstruction](papers/01-feed-forward/) | 6+ | 🚧 In progress |
| [Per-scene neural rendering & 3DGS](papers/02-per-scene-3dgs/) | 8+ | 🚧 In progress |
| [Hybrid pipelines](papers/03-hybrid/) | 4+ | 🚧 In progress |
| [Scalability & large-scale](papers/04-scalability/) | 5+ | 🚧 In progress |
| [Industrial & commercial landscape](tools/) | 10+ | 🚧 In progress |
| [Datasets & benchmarks](benchmarks/) | 7+ | 🚧 In progress |
| [Classical SfM/MVS](papers/05-classical-sfm/) | 4+ | 🚧 In progress |

---

## Paper format

Each paper has its own folder with two files:

- `README.md` — summary, key contribution, limitations, relevance to ThessMesh
- `repro.md` — environment setup, GPU requirements, what works out-of-the-box, known issues

See [CONTRIBUTING.md](CONTRIBUTING.md) for the full template.

---

## About

This survey is part of the [ThessMesh](https://github.com/OpenThessMesh) project, based in Thessaloniki, Greece. The name combines Thessaloniki and Mesh — a 3D reconstruction representation.

**Contributors:** Georgios Floros ([@gfloros](https://github.com/gfloros))

---

## Contributing

Contributions are very welcome — paper summaries, reproduction notes, corrections, and new papers. Please read [CONTRIBUTING.md](CONTRIBUTING.md) before submitting a PR.

---

## Citation

If you find this survey useful in your research or work, please consider citing it:

```bibtex
@misc{thessmesh2026survey,
  title   = {ThessMesh Survey: A Practitioner's Survey of ML 3D Reconstruction},
  author  = {ThessMesh Contributors},
  year    = {2026},
  url     = {https://github.com/OpenThessMesh/survey}
}
```
