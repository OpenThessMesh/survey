# Contributing to the ThessMesh Survey

Thank you for your interest in contributing. This survey is a community effort and all contributions are welcome — paper summaries, reproduction notes, corrections, new papers, and benchmark data.

---

## What you can contribute

- **Paper summaries** — add a new paper to an existing category
- **Reproduction notes** — run a paper's code and document the experience
- **Corrections** — fix errors in existing summaries
- **New categories** — propose a new taxonomy category via an issue first
- **Benchmark data** — add results to the benchmark comparison tables
- **Industrial landscape** — add or update entries in the tools table

---

## Folder structure

```
papers/
  01-feed-forward/
    dust3r/
      README.md       ← paper summary
      repro.md        ← reproduction notes (optional but encouraged)
  02-per-scene-3dgs/
  03-hybrid/
  04-scalability/
  05-classical-sfm/
benchmarks/
  README.md           ← benchmark cross-reference table
tools/
  README.md           ← industrial landscape table
taxonomy.md           ← the taxonomy document
```

---

## Paper summary template

Create a folder named after the paper (lowercase, hyphens) inside the relevant category folder. Add a `README.md` using this template:

```markdown
# [Paper title]

**Authors:** [Author list]
**Venue:** [CVPR 2024 / arXiv 2312.xxxxx / etc.]
**Links:** [Paper](https://arxiv.org/abs/...) · [Code](https://github.com/...) · [Project page](https://...)

---

## Summary

[3–4 sentences. What problem does this paper solve? What is the key idea?]

## Key contribution

[1–2 sentences. The single most important thing this paper contributes.]

## Limitations

[2–3 bullet points. Be honest — what does this method not do well?]

## Relevance to ThessMesh

[1–2 sentences. Why does this paper matter for the ThessMesh library specifically?]

## Notes

[Any additional observations, connections to other papers, or open questions.]
```

---

## Reproduction notes template

If you have run the paper's code, add a `repro.md` in the same folder:

```markdown
# Reproduction notes — [Paper title]

**Tested on:** [GPU model, VRAM, OS, date]
**Code repo:** [URL]
**Commit/version:** [hash or version tag]

---

## Environment setup

[Step-by-step instructions that actually work. Be specific about versions.]

## What works out of the box

[What runs without modification.]

## Known issues

[What breaks, what requires workarounds, undocumented dependencies.]

## GPU requirements

[Minimum VRAM, recommended VRAM, whether multi-GPU is needed.]

## Runtime

[Approximate inference time on your hardware for a representative input.]

## Notes

[Anything else a practitioner should know before trying to run this.]
```

---

## Submitting a contribution

1. Fork the repo
2. Create a branch: `git checkout -b add/dust3r-summary`
3. Add your files following the templates above
4. Open a pull request with a short description of what you added

For larger contributions (new categories, structural changes), please open an issue first to discuss.

---

## Code of conduct

Be respectful. This is a technical community project — disagreements about paper quality or taxonomy belong in issues, not in PR comments directed at people.
