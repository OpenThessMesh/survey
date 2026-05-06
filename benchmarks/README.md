# Datasets & benchmarks

> This table maps key benchmarks to the methods that use them and notes the gap between benchmark conditions and real-world deployment.

---

## Benchmark cross-reference

> This table is continuously updated. See [CONTRIBUTING.md](../CONTRIBUTING.md) to add an entry.

| Dataset | Scale | Domain | GT type | Used by |
|---|---|---|---|---|
| Tanks & Temples | Object / scene | Outdoor, mixed | LiDAR mesh | 3DGS, COLMAP, DUSt3R, MASt3R, VGGT |
| ETH3D | Scene | Indoor / outdoor | LiDAR point cloud | COLMAP, MVS methods, DUSt3R |
| MipNeRF-360 | Scene | Unbounded 360° | — | 3DGS, Mip-Splatting, Scaffold-GS |
| DL3DV-10K | Large | Diverse | — | 3DGS variants, feed-forward methods |
| ScanNet / ScanNet++ | Scene | Indoor, RGB-D | Depth + semantics | SLAM methods, indoor reconstruction |
| CO3D | Object | Multi-view | — | Object-centric feed-forward methods |
| Waymo Open | Large | Autonomous driving | LiDAR | Driving-specific methods |
| nuScenes | Large | Autonomous driving | LiDAR + radar | Driving-specific methods |

---

## The benchmark gap

A recurring theme in this survey: existing benchmarks do not represent the scale or capture conditions of real-world deployments.

**What benchmarks don't cover:**

- **Thousands of images per scene** — drone surveys, photogrammetry missions. No standard benchmark at this scale.
- **Long sequential captures** — robot navigation over extended trajectories. ScanNet is the closest but is small-scale.
- **Domain-specific conditions** — cultural heritage (complex geometry, variable lighting), industrial inspection (repetitive textures, reflective surfaces), medical (limited viewpoints).
- **Practical compute constraints** — most benchmarks assume unlimited GPU time. Real deployments have latency and cost requirements.

This gap is one of the primary motivations for ThessMesh: a library designed for real-world workloads, not benchmark performance.

---

## Adding benchmark data

If you have run a method on one of these benchmarks, please contribute results. See [CONTRIBUTING.md](../CONTRIBUTING.md) for instructions.
