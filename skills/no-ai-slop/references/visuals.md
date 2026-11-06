# Visual review mode

Use this mode for image prompts, image review, and image editing. First identify which task the user requested; a prompt rewrite is not an image edit, and an image critique is not a claim about its origin.

## Choose the visual task

- **Prompt writing or revision:** return a concise prompt that preserves the requested subject, action, style, composition, and exclusions.
- **Image review:** inspect the supplied image with an available visual tool, then describe visible issues and their impact. If no image is attached or accessible, say so and ask for it.
- **Image editing:** use an available image-editing capability on the supplied image. If unavailable, provide a specific edit prompt or steps and state that no image was changed.

## Preserve the brief

- Keep the subject, action, mood, composition goals, and style the user asked for.
- Do not add props, story details, logos, text, or visual claims the brief does not support.
- Use references as evidence for the requested style and content, not as permission to copy unrelated details.

## Inspect by relevance

- Subject integrity: missing, merged, duplicated, or contradictory parts; anatomy or object construction that does not make sense.
- Spatial logic: perspective, scale, contact, shadows, reflections, depth, and physical interactions.
- Composition: focal point, silhouette, framing, balance, negative space, and whether important elements are readable at the intended size.
- Surface and style: materials, lighting, edge treatment, level of detail, color relationships, and consistency with references.
- Text and symbols: legibility, spelling, alignment, and whether they belong in the image.
- Technical fit: aspect ratio, resolution, transparency, file format, texture budget, or platform constraints when specified.
- Artifacts: inspect repeated patterns, malformed edges, inconsistent details, and local visual glitches. Prioritize errors that distract from the subject or contradict the brief.

Do not assume a visible artifact is proof of AI generation. Do not add flaws, noise, or asymmetry merely to simulate human authorship.

## Correct and report

Make targeted edits that retain the original image's identity. Review the affected region and the full composition when the tool allows it. Distinguish visual review from editing, and report what was actually changed and inspected. Name uncertainties that affect the recommendation.

For image prompts, specify subject, action, composition, style, lighting, materials, important constraints, and exclusions only as needed. Avoid bloated prompt lists and contradictory instructions.
