# Code review mode

Use this mode for source code, scripts, configuration, and code generated for an existing project.

## Choose the task

- **Review:** report findings and their impact; do not edit unless asked.
- **Patch or edit:** inspect the surrounding code and make the smallest change that meets the request.
- **Create:** follow the repository's existing architecture, dependencies, supported versions, and style where available.

## Follow the project

- Read surrounding code, documentation, and conventions before editing.
- Preserve public behavior, interfaces, dependencies, architecture, and naming conventions unless the requested change requires otherwise.
- Prefer a small, coherent diff over a stylistic rewrite.

## Review for substance

- Correctness: does the code meet the requested behavior and handle expected inputs?
- Integration: does it fit the project's existing APIs, patterns, and supported versions?
- Clarity: are names, structure, comments, and abstractions useful to maintainers?
- Complexity: remove dead code, repeated logic, unnecessary wrappers, and boilerplate only when behavior remains clear and correct.
- Safety: check input handling, permissions, secrets, error paths, and relevant security concerns.
- Consistency: avoid mixing incompatible styles or introducing a second pattern without a reason.

Do not rename variables, add irregular style, or delete useful comments merely to disguise AI authorship. Do not infer quality from code style alone.

## Review and report

Run repository checks when the user requests them or the agreed project workflow requires them. State the exact commands and results. If checks were not run, say so plainly. A code review is not a test run, and a successful check does not prove unrelated behavior.
