# References and design influences

This skill is original work. These projects informed design choices; their skill files, branding, and distinctive prose are not bundled or reproduced here.

| Project | Ideas adapted |
| --- | --- |
| [blader/humanizer](https://github.com/blader/humanizer) | Preserve meaning and voice; make edits proportional to concrete issues; treat text patterns as context-dependent rather than a universal detector. |
| [Anthropic `frontend-design`](https://github.com/anthropics/skills/tree/main/skills/frontend-design) | Ground visual choices in the actual product, audience, and subject matter. |
| [Anthropic `skill-creator`](https://github.com/anthropics/skills/tree/main/skills/skill-creator) | Keep the core focused and route to supporting references only when relevant. |
| [Vercel `agent-skills`](https://github.com/vercel-labs/agent-skills) | Use a discoverable skill directory with `SKILL.md` and optional references; document Skills CLI installation. |
| [Superpowers](https://github.com/obra/superpowers) | Make intent, tradeoffs, and reviewable work steps explicit. |
| [Agent Skills specification](https://agentskills.io/specification) | Follow the shared folder and `SKILL.md` metadata conventions while keeping host-specific behavior explicit. |
| [fabricioctelles `humanizar`](https://github.com/fabricioctelles/skills/tree/main/skills/humanizar) | Treat Brazilian Portuguese register and idiom as context-sensitive rather than translating English phrase bans literally. |

## Research informing review criteria

- [Do LLMs write like humans?](https://pmc.ncbi.nlm.nih.gov/articles/PMC11874169/) compares linguistic variation across human and LLM text.
- [Interpretable Stylistic Variation in Human and LLM Writing Across Genres](https://aclanthology.org/2026.findings-emnlp.1375/) studies genre, model, and stylistic variation.
- [Characterizing Photorealism and Artifacts in Diffusion Model-Generated Images](https://arxiv.org/abs/2502.11989) studies human perception and image artifact categories; this is a research preprint.
- [A Causal Perspective on Measuring, Explaining and Mitigating Smells in LLM-Generated Code](https://www.microsoft.com/en-us/research/publication/a-causal-perspective-on-measuring-explaining-and-mitigating-smells-in-llm-generated-code/?lang=zh-cn) examines structural code smells and generation conditions.
- [Can Generative AI Create Accessible Websites?](https://doi.org/10.1145/3663547.3759755) evaluates accessibility in AI-generated websites.

These sources cover limited samples, tasks, and models. They support contextual quality review, not universal authorship detection. The PT-BR guidance is original and does not copy a phrase catalog from another skill.
