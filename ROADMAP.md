# Roadmap

The roadmap is staged so each release has a clear focus. Planned items are not
promises or completed features; scope can change based on real use and review.

## 0.2.0 — Behavioral evaluation

**Status: implemented**

- Add a compact set of manual cases for each current format, a human-written
  false positive, PT-BR register, and detector-evasion boundaries.
- Add a qualitative rubric for intent, factual restraint, format fit,
  specificity, and honest reporting.
- Keep the cases outside the runtime skill so they do not add context cost.

## 0.3.0 — PT-BR text and voice

**Planned**

- Add context-aware Brazilian Portuguese guidance for common registers without
  treating a list of phrases as a detector.
- Support optional voice samples or a user-provided style guide.
- Preserve facts, modality, commitments, and uncertainty during edits.
- Add culturally grounded examples and corresponding evaluation cases.

## 0.4.0 — Visual review

**Planned**

- Distinguish editing an image prompt from reviewing or editing an image asset.
- Prioritize visual issues by impact on the brief and intended use.
- Make the workflow explicit about available image tools and actual inspection.
- Add cases for typography, subject integrity, and uncertain visual cues.

## 0.5.0 — Websites and interfaces

**Planned**

- Ground visual direction in product, audience, and task.
- Include functional, responsive, accessibility, and deceptive-pattern review.
- Separate design recommendations from checks actually performed in a browser.

## 0.6.0 — Code and repository workflows

**Planned**

- Strengthen project-aware minimal-diff guidance and behavior preservation.
- Separate code review, patch generation, and direct editing behaviors.
- Report commands, tests, and build checks only when run, with their actual
  results.

## 1.0.0 — Stable cross-agent package

**Planned**

- Document supported installation paths and known agent-specific limits.
- Review trigger wording, reference routing, examples, and evaluation cases.
- Publish a stable release only after the package has been tried across
  representative agents and formats.
