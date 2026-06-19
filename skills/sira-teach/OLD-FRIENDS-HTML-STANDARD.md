# Old Friends HTML Standard

Use this when an HTML lesson includes due old friends, creates new old friends, or asks the child to review memory cards.

## Default

Do not make old friends static in an HTML lesson. Default to an interactive Anki-style review surface unless the parent explicitly asks for a printable or static artifact.

The page should let the parent:

- show the prompt;
- reveal the answer or performance cue;
- mark `Again`, `Hard`, `Good`, or `Easy`;
- see the suggested next due date;
- add a short note if needed;
- save, download, or copy a Markdown review log.

## Source Of Truth

The durable source of truth is still the subject `memory/` folder, not the browser.

If creating the HTML inside a family workspace:

- create or update source cards in `memory/cards.md` or separate card files;
- embed stable card IDs in the HTML;
- include only the due cards and the new cards needed for that lesson.

The HTML may use `localStorage` to preserve in-page progress on that device. It must not pretend that browser state has updated the workspace.

## Save / Import Flow

Avoid making copy-paste the main path. Prefer this order:

1. **Save to workspace**: when the browser supports a file-save picker, offer `Save review file` and suggest `memory/inbox/old-friends-review-{YYYY-MM-DD}.md`.
2. **Download file**: always offer `Download review file`; tell the parent to move it into the subject's `memory/inbox/` folder.
3. **Copy log**: keep `Copy log` as the fallback for chat-only use.

The final screen should say plainly: "To update Sira, save or move this review file into `memory/inbox/`, then tell Sira you reviewed old friends."

When Sira next receives feedback, it should look for `memory/inbox/*.md` review files before asking the parent to paste anything.

## Review Log

Export review results as Markdown shaped like this:

```md
# Old Friends Review - {YYYY-MM-DD}

- **Subject**: {subject}
- **Lesson**: {lesson or artifact name}
- **Learner**: {learner name or shared}

## Results

| Card ID | Result | Previous due | Previous interval | Suggested next due | Suggested interval | Note |
|---|---|---|---|---|---|---|
| {id} | {Again|Hard|Good|Easy} | {date} | {interval} | {date} | {interval} | {note} |
```

When a review log appears in `memory/inbox/` or is pasted by the parent, update the card schedule, save or move the log under `memory/reviews/YYYY-MM-DD.md`, and remove or mark the inbox copy as imported. Do not update durable learner or arc state from one review result unless there is accrued signal.

## Scheduling Heuristic

Use a simple, legible heuristic unless the workspace already has a different one:

- `Again`: later today or tomorrow; interval stays tiny.
- `Hard`: 2-3 days.
- `Good`: roughly double the previous interval.
- `Easy`: roughly triple the previous interval, or retire if it is now trivial.

If prior interval is missing, use:

- `Again`: 1 day.
- `Hard`: 2 days.
- `Good`: 4 days.
- `Easy`: 7 days.

These suggestions are editable. Do not make the parent feel trapped by the algorithm.

## Interaction Shape

Keep the old-friends module short and calm:

1. show one card at a time;
2. include a clear progress count;
3. separate child-facing prompt from parent-facing cue;
4. make the four result buttons large enough for a phone;
5. show a final "review log ready" panel.
6. make the save/import instruction impossible to miss.

The review surface should work offline, on a phone, and from a double-clicked local file. Inline all CSS and JavaScript.
