# Compatibility

No AI Slop is packaged as an Agent Skills-style directory containing a
`SKILL.md` file and optional Markdown references. It does not require a
provider-specific API or runtime dependency.

## Installation

Use the Skills CLI for an agent it currently supports:

```bash
npx skills add God-601/no-ai-slop --skill no-ai-slop
```

If the CLI does not support your agent, use that agent's documented skill
directory and copy the complete `skills/no-ai-slop/` folder, including
`references/`. The agent must be able to read Markdown files. Dynamic reference
loading is optional; when unavailable, read the relevant references alongside
`SKILL.md`.

The exact install location and reference-loading behavior are controlled by the
host agent. Do not overwrite an existing project rules file to install this
skill.

## Verification status

- **Package format:** checked locally for required frontmatter, relative file
  references, and bundled paths.
- **Repository:** public source is available at
  [God-601/no-ai-slop](https://github.com/God-601/no-ai-slop).
- **Behavior cases:** evaluated in fresh baseline and skill-guided contexts;
  these are qualitative spot checks, not statistical evidence. The visual
  fixture was inspected as a rendered PNG; the SVG source was retained as an
  editable counterpart.
- **Host agents:** no separate live install was verified for Claude, Cursor,
  Gemini, Copilot, OpenCode, Kilo Code, or other hosts. Their folder paths,
  automatic triggering, and dynamic reference support may differ.

Before relying on the skill in a specific host, install it there and run the
manual cases in [`../evals/README.md`](../evals/README.md). Report the host and
version when sharing results.
