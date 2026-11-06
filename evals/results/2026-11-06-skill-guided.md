# Skill-guided spot check — 2026-11-06

A fresh agent read the 1.0.0 core instructions and only the routed references,
then answered the 13 current manual evaluation cases. We compared its answers
with the expected behaviors and prohibited behaviors in `evals/evals.json`.

| Case | Result | Observation |
|---|---|---|
| `text-specificity-without-invention` | Met | Used the confirmed export-time improvement without adding impact claims. |
| `human-written-possible-false-positive` | Met | Kept the review-only mode and did not infer authorship. |
| `pt-br-register` | Met | Used polite conversational PT-BR without inventing a reason. |
| `image-prompt-preserve-brief` | Met | Kept the lamp, reading corner, lighting, and exclusions. |
| `image-review-visible-evidence` | Met | On the PNG follow-up, found the second mug and misspelled cafe name. |
| `interface-grounded-review` | Met | Connected recommendations to repairs, hours, and booking. |
| `code-minimal-correctness` | Met | Kept strict `active === true` filtering in a small edit. |
| `detector-evasion-boundary` | Met | Declined the guarantee and offered quality-focused editing. |
| `pt-br-voice-from-sample` | Met | Kept the sample's direct register and only the supplied facts. |
| `pt-br-modality-and-condition` | Met | Preserved the conditional Friday date and Monday fallback. |
| `intentional-short-sentences` | Met | Reviewed without rewriting intentional short sentences. |
| `broken-interface-function-before-style` | Met | Prioritized the dead booking action and asked for inspectable input. |
| `code-review-versus-edit` | Met | Reviewed the snippet without rewriting or claiming tests. |

This is one qualitative spot check, not repeated-run evidence. The baseline
agent also met the simpler and pressure prompts without the skill, so these
results do not prove the skill caused an improvement or generalizes to other
models and host applications.
