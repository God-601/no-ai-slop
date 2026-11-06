---
name: no-ai-slop
description: Improve AI-assisted or AI-sounding text, image prompts and visuals, websites, interfaces, and code. Preserve the user's original idea and voice, remove generic or careless execution, make the correction directly, and explain what changed. Use whenever the user asks to humanize, polish, de-slop, refine, or make generated content feel more specific and intentional.
---

# No AI Slop

Improve the work, not the user's idea. Make it specific to the brief, useful to its audience, and complete enough for its purpose. Avoid formulaic output without flattening the work into one generic "human" style.

## Workflow

1. **Read the brief and artifact.** Identify the user's goal, intended audience, format, constraints, references, and existing conventions. Use relevant context already provided; do not ask for it again.
2. **Protect the intent.** Preserve the core idea, meaning, facts, voice, and requirements. Do not invent personal experiences, evidence, sources, product features, visual details, or project conventions.
3. **Choose the right review mode.** Read only the applicable file in `references/`: `text.md`, `visuals.md`, `websites-and-interfaces.md`, `code.md`, or `other-formats.md`. Mixed artifacts may need more than one.
4. **Find concrete issues.** Describe specific problems in the artifact, not vague claims that it "looks AI." Treat style cues as weak evidence about authorship; a single phrase, visual artifact, or code pattern proves nothing.
5. **Correct directly.** Make the smallest set of meaningful changes that improves the work while preserving its direction. Ask a focused question only if a missing detail could materially change the correction. Otherwise state a brief assumption and proceed.
6. **Review the result.** Compare it with the original request and the relevant reference checklist. Use available tools when the user asked for an edit or when direct inspection is needed. Do not claim an inspection, factual check, build, or test that did not happen.
7. **Deliver the revised artifact first.** Then explain the main changes and why they improve the result. Mention only material remaining limits or uncertainties.

## Quality priorities

When goals conflict, prioritize: **user intent → correctness and coherence → usefulness → specificity → style and polish**. Clarity and accessibility are requirements where relevant, not optional decoration.

Do not add friction for its own sake. Do not replace a plain, effective design with novelty, add quirks to imitate a person, or make a good artifact worse to reduce statistical predictability.

## Detector and authorship limits

Improve naturalness through substantive, context-aware editing. This can reduce formulaic traits often associated with generated content, but it cannot guarantee a result from an AI detector. Do not tune against a named detector, claim that a result is human-authored, or treat detector output as proof. If asked for a detector outcome, explain the limit briefly and continue improving the artifact on its merits.

## Output

- For editable artifacts: return or save the corrected version, then provide a short change log.
- For prompts or code that cannot be edited in place: provide the corrected prompt or patch directly, then explain the key changes.
- For an artifact you cannot access or inspect: say what is missing and give a concrete next step. Never imply that an edit was completed.

## Reference routing

- Text or prose: read `references/text.md`.
- Images, illustrations, image prompts, or visual assets: read `references/visuals.md`.
- Websites or interfaces: read `references/websites-and-interfaces.md`.
- Source code: read `references/code.md`.
- Any other media: read `references/other-formats.md`.

These files are original guidance informed by research and related public skills. They are not authorship detectors and should not be applied as rigid pattern bans.
