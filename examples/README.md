# Examples

These short examples illustrate the skill's workflow. The revised versions use only details supplied in each brief and are not detector tests.

## Text

**Context:** The build now takes 3 minutes instead of 11, and one command replaced four manual steps.

**Draft:** “In today's fast-paced world, efficiency is more important than ever. Our solution empowers teams to unlock their productivity.”

**Edited:** “One command now runs the build in 3 minutes instead of 11.”

**Why:** Removed broad promotional filler and used the concrete result from the supplied context.

## Brazilian Portuguese and voice

**Writing sample supplied by the user:** “então, fui mexer nisso ontem e travou bem na hora que eu precisava. consegui resolver limpando o cache, mas demorou”

**Request:** Turn it into a short Discord update. Keep the user's way of writing. Known facts: it froze yesterday; clearing the cache fixed it.

**Edited:** “Ontem travou bem na hora que eu precisava. Limpei o cache e voltou.”

**Why:** Kept the direct, informal rhythm and the two supplied facts without inventing a cause or extra detail.

## Image prompt

**Brief:** A small wooden desk lamp in a cozy reading corner, with warm indirect light; no people.

**Edited prompt:** “A small wooden desk lamp in a cozy reading corner, casting warm indirect light. Close three-quarter view, clear lamp silhouette, natural wood texture, subdued palette. No people, no text.”

**Why:** Kept the requested subject and mood, then clarified framing and material cues without adding a new subject.

## Image review

**Brief:** A cafe poster should show one mug and the exact name “Café da Esquina.”

**Review of the supplied evaluation fixture:** It shows two mugs and spells the cafe name “Cafê da Esquina.”

**Why:** Both findings are visible and conflict with the brief. The review does not infer how the poster was made.

## Website/interface

**Brief:** A local bike repair shop needs a website that helps nearby riders find services, opening hours, and a way to book.

**Review:** Replace a generic hero such as “Ride into your best self” and decorative feature cards with the shop's repair services, neighborhood, hours, and a visible booking action. Make the booking form keyboard-accessible and show confirmation after submission.

**Why:** The page should answer the visitor's practical questions and support the actual task. This is a review recommendation, not a claim that a rendered page was inspected.

## Code

**Context:** The project uses JavaScript and this function should include only records whose `active` field is exactly `true`.

**Before:**

```js
function getActive(users) {
  const activeUsers = users.filter(user => user.active === true);
  const result = activeUsers;
  return result;
}
```

**After:**

```js
function getActive(users) {
  return users.filter(user => user.active === true);
}
```

**Why:** Removed two temporary variables that added no information and preserved the exact filtering behavior.
