# No AI Slop

An agent skill for improving AI-assisted content without replacing the creator's idea. It edits directly, uses review rules suited to the format, and explains the changes.

## What it covers

- Text and prose
- Images, image prompts, and visual assets
- Websites and user interfaces
- Code
- Other media through a purpose-first review workflow

## How it works

The core `SKILL.md` protects the user's intent, selects the relevant format reference, makes a focused correction, and returns a short explanation. Format guidance lives in `skills/no-ai-slop/references/` so agents can load only what they need. Agents without dynamic reference loading can read the short fallback workflow in `SKILL.md`.

This skill improves quality and reduces formulaic patterns where appropriate. It cannot guarantee that an AI detector will classify content a certain way, and style alone does not prove authorship.

## Install

Install from GitHub with the [Skills CLI](https://github.com/vercel-labs/skills):

```bash
npx skills add God-601/no-ai-slop --skill no-ai-slop
```

For agents not supported by the CLI, follow that agent's skill-folder convention and copy `skills/no-ai-slop/` with its `SKILL.md` and `references/` directory.

## Related work

This project uses original wording and adapts general ideas from public work on intent-preserving editing, domain-grounded visual design, progressive disclosure for skills, and cross-agent skill packaging. See [`skills/no-ai-slop/REFERENCES.md`](skills/no-ai-slop/REFERENCES.md) for links and attribution.

See [`examples/README.md`](examples/README.md) for brief examples across the supported formats.

## Evaluations

The repository includes manual evaluation cases for intent preservation, factual restraint, false positives, and format-specific quality. See [`evals/README.md`](evals/README.md) and [`evals/evals.json`](evals/evals.json). These cases assess behavior; they are not AI detectors or proof of authorship.

See [`ROADMAP.md`](ROADMAP.md) for the planned version sequence.

## License

MIT. See [`LICENSE`](LICENSE).
