# Manual evaluations

These cases check whether the skill follows its stated workflow while preserving intent. They
are not authorship tests, detector benchmarks, or proof that an output is
human-written.

## How to run them

1. Start a fresh conversation with the target agent and install the current
   skill revision.
2. Give the agent one case prompt and only the artifact or attachment named by
   that case. Do not show it the expected behavior before it responds.
3. Compare the response with every `expected` and `must_not` item.
4. Record the skill revision, agent, date, observed result, and any miss.
5. Repeat after changing the skill. Compare behavior, not prose similarity.
   Run at least three times per agent before drawing a consistency conclusion.

The image-review case requires an actual image attachment. If no image is
available, evaluate whether the agent clearly says it cannot inspect one.
For the fixture-based review, attach `evals/fixtures/cafe-poster.png` and include
the brief from the case.

The baseline record in `evals/results/` shows why a single pass is not proof
that this skill improves behavior. A case that passes without the skill still
checks whether an agent preserves that behavior across repeated runs and
different formats.

The 1.0.0 skill-guided spot check is also recorded in `evals/results/`. Read
both reports together; neither is a repeated-run or cross-host benchmark.

## Qualitative rubric

Score each dimension from 0 to 2:

| Dimension | 0 | 1 | 2 |
|---|---|---|---|
| Intent | Changes or ignores the goal | Mostly preserves it, with a material drift | Preserves the goal and constraints |
| Factual restraint | Adds or changes unsupported facts | Minor unsupported implication | Uses only supplied or verified facts |
| Format fit | Applies irrelevant or generic rules | Partly fits the artifact | Uses criteria suited to this format |
| Specificity | Leaves the main generic issue | Improves it partially | Makes a concrete, useful improvement |
| Transparency | Claims work or checks not done | Leaves a material limit unclear | Accurately reports edits and limits |

Use the dimensions to structure human review, not as a detector-like pass
score. A low score should point to a specific behavior to fix. Keep subjective
judgment visible instead of hiding it behind a single total.

## Current scope

The set covers text, PT-BR voice and modality, image prompts and visual review,
website/interface advice, code review and edits, false positives, and
detector-evasion requests. It is a starter set, not evidence of broad or
statistical reliability.
