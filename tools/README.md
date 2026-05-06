# Industrial & commercial landscape

> A comparison of existing tools — open-source and commercial — that ThessMesh relates to, competes with, or builds on.

---

## Open-source tools

> This table is continuously updated. See [CONTRIBUTING.md](../CONTRIBUTING.md) to add an entry.

| Tool | Language | License | Input | Output | Active | Notes |
|---|---|---|---|---|---|---|
| COLMAP | C++ | BSD-3 | Images | Sparse point cloud, camera poses | Yes | The classical baseline. SfM + MVS. |
| GLOMAP | C++ | — | Images | Sparse point cloud, camera poses | Yes | Fast global SfM. COLMAP successor to watch. |
| OpenMVS | C++ | AGPL-3 | Poses + sparse cloud | Dense mesh, texture | Yes | Open-source MVS pipeline. |
| OpenSplat | C++ | MIT | Poses + sparse cloud | 3DGS splat | Yes | Most architecturally similar to ThessMesh on the Gaussian training side. Study closely. |
| gsplat | Python/CUDA | Apache 2.0 | Poses + sparse cloud | 3DGS splat | Yes | UC Berkeley + Luma AI. JMLR 2025. Python-first. |
| Nerfstudio | Python | Apache 2.0 | Images | NeRF / 3DGS | Yes | Key reference for API design. Python-first. |
| Instant NGP | C++/CUDA | Custom | Images + poses | NeRF | Maintenance | Fast hash-encoding NeRF. |

---

## Commercial tools

> This table is continuously updated. See [CONTRIBUTING.md](../CONTRIBUTING.md) to add an entry.

| Tool | Input | Output | Pricing model | Notes |
|---|---|---|---|---|
| Luma AI | Images / video | NeRF / 3DGS | Freemium + API | Consumer-grade, API available. |
| Polycam | Images / LiDAR | Mesh, point cloud | Subscription | Mobile-first. |
| RealityCapture | Images | Mesh, point cloud | Free (Epic) | Professional photogrammetry. |
| Agisoft Metashape | Images | Mesh, point cloud, orthomosaic | One-time license | Industry standard photogrammetry. |

---

## How ThessMesh differs

> This table is continuously updated. See [CONTRIBUTING.md](../CONTRIBUTING.md) to add an entry.

| Capability | COLMAP | OpenSplat | Nerfstudio | ThessMesh (planned) |
|---|---|---|---|---|
| Feed-forward inference | ✗ | ✗ | Partial | ✓ |
| 3DGS training | ✗ | ✓ | ✓ | ✓ |
| End-to-end pipeline | ✗ | ✗ | Partial | ✓ |
| C++ core | ✓ | ✓ | ✗ | ✓ |
| Minimal dependencies | ✓ | ✓ | ✗ | ✓ |
| Large-scale support | Partial | ✗ | ✗ | ✓ (planned) |
| Mesh output | Via OpenMVS | ✗ | Partial | ✓ (planned) |

---

## License notes

Pre-trained model weights (DUSt3R, VGGT, MASt3R) are typically CC BY-NC — restricting commercial use of the weights even if the wrapper code is Apache 2.0. Track weight licenses carefully. Prioritise permissively licensed weights for any commercial deployment path.
