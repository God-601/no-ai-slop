# No AI Slop Skill Implementation Plan

> **For agentic workers:** This plan is executed natively in this session. Keep the user's intent, preserve the artifact's original idea, and report only checks actually performed.

**Goal:** Create an original, cross-format agent skill that removes generic or careless output while preserving user intent and explaining edits.

**Architecture:** Package one skill under `skills/no-ai-slop/`, with a concise `SKILL.md` router and separate format references for text, visual assets, websites/interfaces, and code. The repository root contains installation, scope, attribution, and license documentation.

**Tech Stack:** Markdown skill package following common Agent Skills conventions; no runtime dependencies.

**Spec:** [2026-11-06-no-ai-slop-design.md](../specs/2026-11-06-no-ai-slop-design.md) (current Library design is the source of truth).

## Global Constraints

- Preserve original user intent, meaning, constraints, and voice wherever feasible.
- Correct directly when sufficient context exists, then explain concrete changes.
- Never invent personal experience, evidence, sources, or artifact details.
- Do not promise or optimize for a specific AI detector result.
- Treat cues as quality signals, not proof of authorship.
- Use original wording; cite inspiration and do not copy bundled skill text.
- Keep the core concise and use relevant modality references only.
- The user created the public repository `God-601/no-ai-slop`; the GitHub connector can write files once the repository exists.

## Review Focus

- Vague or mixed-format input should preserve intent while asking only when a missing detail could change the result.
- Existing writing should not be flattened into one neutral voice or padded for perceived human-ness.
- Generated images should be corrected against the brief without relying on any single alleged AI artifact.
- Website reviews must include function, accessibility, and dark-pattern checks, not just visual styling.
- Code edits must follow the existing project and avoid cosmetic rewrites disguised as quality improvements.

---

## Task 1: Create skill package and shared workflow

**Files:**
- Create: `skills/no-ai-slop/SKILL.md`

**Interfaces:**
- Consumes: user-provided artifact, intent, audience, references, project context, and constraints.
- Produces: directly improved artifact plus a short explanation of changes and unresolved limits.

- [x] **Step 1: Write the skill metadata and purpose**
  Use the `no-ai-slop` identifier and a trigger description covering text, image, interface, and code refinement.
- [x] **Step 2: Write the shared workflow**
  Add intake, intent preservation, relevant-mode selection, direct correction, review, and output behavior.
- [x] **Step 3: Add reference routing and fallback**
  Load only the relevant format file where supported; provide a compact fallback when an agent cannot load references dynamically.
- [x] **Step 4: Define detector boundaries and reporting**
  State that naturalness and quality are targets; detector outcomes are not guaranteed and authorship cannot be inferred from style alone.

## Task 2: Add format-specific review references

**Files:**
- Create: `skills/no-ai-slop/references/text.md`
- Create: `skills/no-ai-slop/references/visuals.md`
- Create: `skills/no-ai-slop/references/websites-and-interfaces.md`
- Create: `skills/no-ai-slop/references/code.md`
- Create: `skills/no-ai-slop/references/other-formats.md`

**Interfaces:**
- Consumes: the selected mode, brief, and artifact from Task 1.
- Produces: domain-specific checks and correction priorities, without making authorship claims.

- [x] **Step 1: Write text guidance**
  Cover specificity, register, repetitive structure, filler, unsupported claims, and voice-preserving edits.
- [x] **Step 2: Write visual guidance**
  Cover subject integrity, composition, anatomy/object geometry, physics, visual coherence, typography, and artifact severity; use human curation only to improve the brief, not to fake provenance.
- [x] **Step 3: Write website/interface guidance**
  Cover domain-grounded art direction, hierarchy, behavior, accessibility, responsiveness, and deceptive patterns.
- [x] **Step 4: Write code guidance**
  Cover project conventions, correctness, security, maintainability, unnecessary boilerplate, and minimal diffs.
- [x] **Step 5: Write other-format guidance**
  Apply purpose-first review and explain tool limits; ask targeted questions only for material gaps.

## Task 3: Document project and compatibility

**Files:**
- Create: `README.md`
- Create: `LICENSE`
- Create: `CHANGELOG.md`
- Create: `skills/no-ai-slop/REFERENCES.md`

**Interfaces:**
- Consumes: package structure and the related-skill research.
- Produces: installation and usage instructions, project scope, attribution, license, and version notes.

- [x] **Step 1: Write README**
  Explain what it does, supported formats, workflow, limitations, and installation paths.
- [x] **Step 2: Add MIT license**
  Use original content and attribute conceptual inspiration to the referenced projects without copying their skill files.
- [x] **Step 3: Add initial changelog**
  Record the initial `0.1.0` development version and core functionality.
- [x] **Step 4: Add reference/attribution index**
  Link Humanizer, Anthropic Frontend Design and Skill Creator, Vercel Agent Skills, and Superpowers; summarize what principles informed this skill.

## Task 4: Assemble repository locally and review completeness

**Files:**
- Review all files created in Tasks 1–3.

- [x] **Step 1: Inspect tree and metadata**
  Confirm expected files exist and the skill metadata is valid YAML with a clear name and description.
- [x] **Step 2: Inspect cross-links**
  Confirm every reference path in `SKILL.md` resolves and each format module stands on its own.
- [x] **Step 3: Review against the design**
  Confirm each goal, non-goal, anti-goal, supported mode, and output behavior is represented.
- [ ] **Step 4: Verify GitHub publication**
  Confirm the public repository contains the complete package and that the linked README and install path are accurate.
