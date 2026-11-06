# No AI Slop — Design document

**Status:** Implemented as version 1.0.0
**Date:** 2026-11-06
**Project name:** No AI Slop
**Repository:** `God-601/no-ai-slop`
**License:** MIT
**Initial version:** 0.1.0
**Current version:** 1.0.0

## Intent

Create one reusable agent skill that improves AI-assisted content across text, images, websites/interfaces, code, and other formats. Its purpose is to remove generic, careless, formulaic, incoherent, or visibly unfinished output while preserving the user's original idea.

The user wants the skill to make corrections directly and then explain the changes. It should also reduce stereotypical cues commonly associated with AI output. It must not promise that a particular detector will classify an artifact as human-made: detection systems and their errors vary, and style cues are not proof of authorship.

## Goals

- Preserve the user's core idea, intent, constraints, and voice while improving execution.
- Edit the artifact directly when enough context is available; then summarize what changed and why.
- Detect and fix low-specificity, padding, repetitive structures, incoherent details, generic visual choices, weak implementation choices, and other format-specific quality issues.
- Use separate review criteria for each content type rather than applying one generic checklist everywhere.
- Ask concise, targeted questions only when a missing answer could materially change the result; otherwise proceed with explicit, reasonable assumptions.
- Match the surrounding project, references, audience, language, conventions, and technical constraints.
- Identify uncertainty, unverifiable claims, or issues that could not be fixed with available tools.

## Non-goals

- Guaranteeing a score or outcome from AI detectors, plagiarism checkers, or platform moderation systems.
- Making content appear human-authored through false claims about who created it.
- Replacing the user's concept with the agent's preferred concept.
- Adding invented personal experiences, evidence, sources, features, or visual details.
- Treating any single phrase, image artifact, code style, or design choice as proof of AI authorship.

## Anti-goals: what would make this fail

- Rewriting every artifact into the same polished, neutral, generic voice.
- Removing useful structure or clarity just to make output less predictable.
- Changing meaning, requirements, or project conventions without saying so.
- Making gratuitous edits that add length, complexity, decoration, or features without improving the result.
- Claiming detector evasion, human authorship, factual verification, visual inspection, or successful code execution that did not happen.

## Approaches considered

1. **One universal checklist:** compact and easy to maintain, but likely to apply text-centric rules to images, code, and interfaces.
2. **One skill with a shared core and format-specific modes (chosen):** routes each task through common intent-preservation steps, then applies focused criteria for the artifact. It balances one familiar entry point with specialist review.
3. **Separate skills per format:** permits deep specialization but fragments the user experience and duplicates shared rules; not suitable for this goal.

## Proposed design

### Shared workflow

1. Identify the requested outcome, audience, constraints, references, and the artifact's current state.
2. Preserve the core intent and voice. If a critical requirement is missing, ask a targeted question; otherwise state assumptions briefly and continue.
3. Diagnose concrete quality problems using the relevant format mode.
4. Edit directly, making the smallest changes that materially improve the artifact.
5. Review the result against the user's goal and format-specific criteria. Do not report checks that were not actually performed.
6. Deliver the corrected artifact first, followed by a concise change log: what changed, why, and anything still uncertain or limited.

### Format modes

- **Text:** remove filler, repeated points, canned transitions, unsupported generalities, unnatural register, and monotonous structure; improve specificity, flow, and voice while preserving meaning and factual boundaries.
- **Images and visual assets:** inspect composition, subject integrity, anatomy/object structure where applicable, physical and spatial coherence, typography, style consistency, and distracting generation artifacts. Use available image tools for edits; if they are unavailable, provide actionable correction instructions instead of claiming an edit was made.
- **Websites and interfaces:** check whether layout, hierarchy, content, interactions, responsive behavior, and accessibility serve the actual use case. Avoid defaulting to decorative gradients, interchangeable cards, empty marketing copy, or deceptive interaction patterns without a reason.
- **Code:** follow the repository's existing conventions; remove needless boilerplate, dead code, inconsistent patterns, and unjustified complexity; prioritize correctness, maintainability, security, and integration with existing architecture over cosmetic authorship cues.
- **Other formats:** infer the artifact's purpose, use the shared principles, and ask for format-specific context only when it materially affects the edit.

### Detector-related handling

The skill may reduce formulaic patterns as part of substantive editing, but it will not claim guaranteed detector avoidance or optimize against a named detector as a measure of quality. It should explain this limitation plainly when detector outcomes are requested.

## Research basis and limits

- A PNAS study comparing multiple LLMs with human writing found measurable grammatical, lexical, and stylistic differences, and found that genre/register matters. This supports contextual editing rather than a universal list of banned words: [Do LLMs write like humans?](https://pmc.ncbi.nlm.nih.gov/articles/PMC11874169/).
- An ACL 2026 study evaluating 11 models across eight genres reported that genre had a stronger effect on stylistic features than source alone, and that model mattered more than decoding settings in many cases: [Interpretable Stylistic Variation](https://aclanthology.org/2026.findings-emnlp.1375/).
- An image-perception research preprint identified artifact categories including anatomical, stylistic, functional, physical, and sociocultural implausibilities, while stressing that cues are not always present: [Characterizing Photorealism and Artifacts](https://arxiv.org/abs/2502.11989).
- Microsoft Research's code-smell study reports that prompting and generation choices affect structural quality, supporting project-aware code review rather than superficial renaming: [A Causal Perspective on Code Smells](https://www.microsoft.com/en-us/research/publication/a-causal-perspective-on-measuring-explaining-and-mitigating-smells-in-llm-generated-code/?lang=zh-cn).
- A 2025 accessibility study of six AI-generated websites found many accessibility and cognitive-clarity errors. This supports explicit accessibility and structure checks, not assumptions that visual polish means quality: [Can Generative AI Create Accessible Websites?](https://doi.org/10.1145/3663547.3759755).
- These studies evaluate limited models, genres, tasks, or samples. Their findings inform review criteria; they do not define reliable authorship tests or universal signatures of AI content.

## Related skills reviewed and adaptations

The user asked to combine useful ideas from existing skills. This project will adapt principles, not copy full instructions or package other projects' text:

- **blader/humanizer:** adapt intent preservation, edits proportional to concrete evidence, and distinguishing stronger patterns from weak cues. Its text-specific checklist will not be treated as a universal detector or applied to images/code: [repository](https://github.com/blader/humanizer).
- **Anthropic frontend-design:** adapt grounding visual decisions in the actual product, audience, and subject matter rather than default templates: [skill](https://github.com/anthropics/skills/tree/main/skills/frontend-design).
- **Anthropic skill-creator:** adapt progressive disclosure, concise trigger descriptions, and format-specific reference files so the core stays small: [skill](https://github.com/anthropics/skills/tree/main/skills/skill-creator).
- **Vercel agent-skills:** use the familiar `SKILL.md` plus optional `references/` structure and document Skills CLI installation where applicable: [repository](https://github.com/vercel-labs/agent-skills).
- **Superpowers brainstorming/writing-plans:** keep intent, anti-goals, and implementation choices explicit, then execute in a reviewable sequence: [repository](https://github.com/obra/superpowers).

These references are inspiration and compatibility examples. Their full content, branding, or restricted assets will not be copied into this project. The new skill will have original wording and its own license.

## Constraints

- Ship as one public GitHub skill repository with a short main entry file and separate references for each format. Load-on-demand behavior depends on each agent platform's skill format; where that is unsupported, the core must include clear routing to the relevant references.
- Keep the package platform-neutral and document installation and platform-specific limitations without claiming unverified host support.
- Use only tools available in the current environment; report when a requested modality cannot be edited or inspected directly.
- Repository name, MIT license, and initial release version are fixed implementation decisions; 1.0.0 is the current stable cross-format package version.

## Success criteria

- The edited result retains the original intent and is materially less generic or careless.
- The skill uses the correct format-specific checks and does not mechanically apply irrelevant rules.
- The response explains concrete changes and discloses unresolved limitations.
- No false detector, authorship, factual-check, visual-review, or test claims are made.
- Initial examples demonstrate the workflow on text, image prompts/assets, a website/interface, and code.
- Manual evaluation cases cover supported formats, at least one false positive, and the detector-evasion boundary; their rubric guides review without claiming statistical reliability.

## Implementation decisions

- Public GitHub repository: `God-601/no-ai-slop`.
- MIT license, original wording, and attribution links for related skills.
- Package layout: `skills/no-ai-slop/SKILL.md` plus format-specific references.
- Initial development version: 0.1.0; 0.2.0 added manual behavior evaluation cases and a qualitative rubric; 1.0.0 includes the planned PT-BR, visual, interface, code, and compatibility milestones.
- Dynamic reference loading is used where supported; the main skill keeps a concise fallback workflow.
