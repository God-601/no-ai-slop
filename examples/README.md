# Examples

These short examples illustrate the skill's workflow. Revised versions use only details supplied in each brief; they are not detector tests.

## Text

**Context:** The build now takes 3 minutes instead of 11, and one command replaced four manual steps.  
**Draft:** “In today's fast-paced world, efficiency is more important than ever. Our solution empowers teams to unlock their productivity.”

**Edited:** “One command now runs the build in 3 minutes instead of 11.”

**Why:** Removed broad promotional filler and used the concrete result from the supplied context.

## Image prompt

**Brief:** A small wooden desk lamp in a cozy reading corner, with warm indirect light; no people.

**Edited prompt:** “A small wooden desk lamp in a cozy reading corner, casting warm indirect light. Close three-quarter view, clear lamp silhouette, natural wood texture, subdued palette. No people, no text.”

**Why:** Kept the requested subject and mood, then clarified framing and material cues without adding a new subject.

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
