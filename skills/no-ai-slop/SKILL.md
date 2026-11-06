---
name: no-ai-slop
description: Use when the user asks to review, create, or improve text, image prompts or assets, websites, interfaces, code, or other content they call generic, formulaic, careless, incoherent, unfinished, AI-sounding, or AI slop; also when they ask to humanize or de-slop content.
license: MIT
metadata:
  version: "1.0.0"
---

# No AI Slop

Improve the work, not the user's idea. Make it specific to the brief, useful to its audience, and complete enough for its purpose. Avoid formulaic output without flattening the work into one generic "human" style.

## Workflow

1. **Identify the task mode.** Follow the user's request to review only, edit an existing artifact, or create something new. A request for critique is not permission to rewrite; a request for an edit is not a reason to stop at advice.
2. **Read the brief and artifact.** Identify goal, audience, format, constraints, references, and surrounding project conventions. Reuse context already supplied; do not ask again.
3. **Protect intent and evidence.** Preserve the idea, facts, voice, constraints, and requirements. Do not invent personal experience, sources, claims, product features, visual details, or project conventions.
4. **Route to the right guidance.** Read only relevant files in `references/`. For Brazilian Portuguese text, also read `text-pt-br.md`. Read `voice-matching.md` only when the user asks for voice matching or supplies a writing sample for that purpose. Mixed work may need multiple modes.
5. **Diagnose concrete issues.** Point to observable problems and their effect on the intended use. A phrase, image artifact, or code pattern alone does not establish AI authorship.
6. **Make a focused correction.** Keep changes proportional to the problem. Ask only when a missing detail could materially change the result; otherwise state a brief assumption and proceed.
7. **Review and report honestly.** Compare the result with the brief and relevant format guidance. Use tools for inspection or editing when available. Report only checks actually performed, and do not claim detector success, visual inspection, fact-checking, or code execution that did not occur.
8. **Deliver in the requested mode.** For edits and creations, present the artifact first and then explain material changes. For review-only requests, provide findings and recommendations without rewriting the artifact.

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
- Brazilian Portuguese: also read `references/text-pt-br.md`.
- Voice matching from a supplied sample or style guide: also read `references/voice-matching.md`.
- Images, illustrations, image prompts, or visual assets: read `references/visuals.md`.
- Websites or interfaces: read `references/websites-and-interfaces.md`.
- Source code: read `references/code.md`.
- Any other media: read `references/other-formats.md`.

These files are original guidance informed by research and related public skills. They are not authorship detectors and should not be applied as rigid pattern bans.
