# Learning Record Format

Learning records live in `./learning-records/` and use sequential numbering: `0001-slug.md`, `0002-slug.md`, etc. Create the directory lazily — only when the first record is written.

They are the teaching equivalent of ADRs: they capture non-obvious things the child has learned, what delighted them, misconceptions corrected, prior knowledge established, and developmental-stage shifts. They are used to calculate the **two-axis** zone of proximal development (knowledge floor × available cognitive tools).

## Template

```md
# {Short title of what was learned, delighted, or shifted}

{1-3 sentences: what happened, and why it changes what to teach next.}
```

That is the whole format. A record can be a single paragraph. The value is in recording _that_ this is now true and _why_ it changes the next lesson — not in filling sections.

## Optional sections

Only when they add genuine value:

- **Status** frontmatter (`active | superseded by LR-NNNN`) — when an earlier understanding turns out wrong.
- **Evidence** — *how* the child showed it (retold the story, used the word correctly, completed the task, taught a sibling). Useful when the claim might be revisited.
- **Implications** — what this unlocks or rules out next, when non-obvious.

## When to write a learning record

Write one when any of these is true:

1. **The child demonstrated genuine understanding of something non-trivial** — evidence they can *use* the idea, not just that they were exposed to it. Sets a new floor.
2. **A cognitive hook landed especially well** — a metaphor, a binary opposite, a hero, a song. These are reusable gold; record what worked so future lessons reuse the register.
3. **The child disclosed or revealed prior knowledge** — record it (and its depth) so you don't re-teach it.
4. **A misconception was corrected** — high value; misconceptions predict future stumbling blocks.
5. **The child's developmental stage shifted** — new appetite for argument, extremes, or making. Cross-link to [[LEARNER.md]] and update it.
6. **The mission shifted** — the child discovered they cared about something different. Cross-link to [[MISSION.md]] and update it.

### What does _not_ qualify

- Material merely covered. Coverage is not learning — wait for evidence.
- Terms already captured tersely in [[GLOSSARY.md]]. Don't duplicate.
- A session-by-session activity log. These are decision-grade insights, not a journal.

## Supersession

When a later record contradicts an earlier one (understanding deepened or corrected), mark the old one `Status: superseded by LR-NNNN` rather than deleting it. The history of how a child's understanding evolved is itself useful signal.
