# Code review mode

Use this mode for source code, scripts, configuration, and code generated for an existing project.

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

Use the repository's existing checks when the user asks for verification or when the requested workflow authorizes them. Otherwise, describe what was inspected and do not claim tests passed. Clearly separate code changes from checks actually performed.
