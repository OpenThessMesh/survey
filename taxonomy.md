# Survey taxonomy

> Version: 2 (work in progress — will be finalised after the 2026 paper discovery sweep)
> Last updated: 2026-05-06

---

## Philosophical position

This survey does not take sides in the feed-forward vs. per-scene optimisation debate. The existing academic surveys treat feed-forward as the new paradigm replacing classical methods. We treat it as one tool among several, each with different trade-offs.

**Our position:** pragmatic hybridisation over paradigm purity. The goal is what works best in practice for real workloads — not what is architecturally purest or most fashionable in the literature.

Real workloads include: drone surveys with thousands of images, robot navigation over extended trajectories, cultural heritage digitisation at scale, and industrial inspection. Neither feed-forward nor per-scene optimisation alone handles these well. This survey documents both paradigms and the methods that bridge them.

---

## Categories

### 1. Feed-forward reconstruction

Methods that estimate camera poses and dense geometry in a single forward pass, generalising across scenes without per-scene optimisation.

**Why it matters for ThessMesh:** These are the inference engines that replace the classical SfM front-end — the first stage of the ThessMesh pipeline.

**Key open question:** How do these methods scale to thousands of images? This remains an open, unanswered question that no existing survey addresses.

---

### 2. Per-scene neural rendering & 3DGS variants

Methods that optimise a scene representation from a fixed set of images. Still state-of-the-art for reconstruction quality and novel view synthesis.

**Why it matters for ThessMesh:** These are the optimisation back-ends — the scene-specific stage that produces the final reconstruction.

---

### 3. Hybrid pipelines

Methods that combine feed-forward initialisation with per-scene optimisation, or that selectively apply each paradigm to different parts of the pipeline. The most under-explored category in existing surveys and the design space ThessMesh directly occupies.

**Why it matters for ThessMesh:** The most under-explored category in existing surveys and the design space ThessMesh directly occupies.

---

### 4. Scalability & large-scale methods

Methods that address reconstruction of large scenes that exceed GPU memory for a single model.

**Why it matters for ThessMesh:** Scalability is a first-class design requirement. This category informs the large-scale pipeline architecture.

---

### 5. Industrial & commercial landscape

Existing tools and products — open-source and commercial. Defines what ThessMesh does not need to rebuild and where the gaps are.

See [tools/README.md](tools/README.md) for the full comparison table.

---

### 6. Datasets & benchmarks

Existing benchmarks and the gap between them and real-world applications.

**ThessMesh survey angle:** explicitly address the disconnect between benchmark conditions and practical deployment.

See [benchmarks/README.md](benchmarks/README.md) for the cross-reference table.

---

### 7. Classical SfM/MVS

The methods ThessMesh partially replaces and partially builds on. Included for baseline comparison and as context for practitioners coming from the classical pipeline.

