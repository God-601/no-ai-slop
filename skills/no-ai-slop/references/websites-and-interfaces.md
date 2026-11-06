# Website and interface review mode

Use this mode for websites, web apps, landing pages, dashboards, UI mockups, and frontend components.

## Ground the design

Before changing the interface, infer its real purpose, audience, content, and primary action from the brief and existing project. Use the product's subject matter to guide layout, typography, color, imagery, and interaction. Do not start from a fashionable template and retrofit the content.

For a new or substantially redesigned interface, state a short direction before implementation: the content hierarchy, visual principle, and primary action. Check that these choices come from this product's brief rather than a template. Skip this planning step for a small local fix.

## Review

- **Purpose:** Does the page make its purpose and next action clear without filler copy?
- **Hierarchy:** Can users find the important information quickly? Do spacing, type, contrast, and grouping support the content?
- **Distinctiveness:** Are visual choices connected to this product? Remove interchangeable decoration or repeated card grids when they do not help. Gradients, centered heroes, rounded cards, and popular fonts are valid only when they serve the brief.
- **Consistency:** Do components, states, typography, spacing, and visual language agree across the interface?
- **Function:** Do buttons, forms, navigation, validation, loading, empty, success, and error states behave as expected?
- **Accessibility:** Check semantic structure, keyboard access, focus visibility, labels, contrast, alternative text, and motion sensitivity as relevant.
- **Responsive behavior:** Confirm the layout remains usable at the target widths and does not hide essential content.
- **Trust:** Avoid fake urgency, hidden costs, misleading controls, forced consent, obstructive cancellation, or other deceptive interaction patterns.

For an interaction the user reports as broken, treat the behavior as the main issue. Ask for or inspect the relevant code or rendered page when necessary; a visual restyle cannot fix a button that does nothing.

## Correct

Preserve the information architecture and existing design system unless the brief calls for a redesign. Prefer meaningful changes over decorative polish. If implementation is requested, follow the project's framework and conventions and inspect the rendered result when tools are available. If visual inspection is not available, say so and distinguish code review from visual verification.

Explain user-facing changes and any unverified responsive, accessibility, or interaction behavior. Do not claim WCAG conformance from a visual pass or claim a browser check that did not happen.
