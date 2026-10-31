# Standing rules

These apply in every repo.

## Git
- Commit messages: match the repo's `git log` style. Default is one line saying what changed, no body. Add a sentence of body only for a non-obvious why. Never bulleted, PR-style bodies.
- Before pushing, check whether a push to that branch deploys somewhere live (GitHub Pages, Vercel, release pipeline). If it does, ask first.

## Writing
- Code comments: only for a non-obvious why, one or two lines. State the constraint, not the story of how it was found. Changelog bullets are one short line.
- No AI-sounding buzzwords ("leverage", "seamless", "unlock", "supercharge", "elevate").
- No em dashes. Use a comma, colon, parentheses, or a new sentence.

## Deliverables
- No Artifacts. Write HTML/reports/mockups as local files and give the path.

## Working
- Never commit until told to. Make a change right first (tests, checks, live testing where it applies), then wait for the word. A churn of commits reversing each other is what to avoid.
- Explain the why of each change briefly as you make it.
- Doing nothing is a valid answer to a bug or request. Prefer the smallest change that solves it, and say when no-op is the better call.
- No defensive code for states no user can reach. Before calling something a bug, check a person can trigger it: a script that sets state and presses a key in one call makes timings no human can.
- Don't dig into a one-off crash that has no repro. Note it and wait for it to recur.
- In planning conversations, record decisions and don't start building until told to.
- After a background review finishes, re-diff any files edited while it ran. It works in the same tree and can revert them.
- User-facing copy (UI strings, dialogs, welcome text, store and website copy) is written by the human dev, never shipped as agent wording. Put in a placeholder or a clearly marked suggestion, finish the task, then list each one at the end and ask for the final wording before committing. Changelog bullets are excepted.

## Docs and memory
- Project docs are about the project, not people: never write "user" or attribute a decision to a person. State the decision with its date, as the project's own.
- Memory holds decisions, reasons and gotchas, not transient state: no counts, no pushed/unpushed or public/private status, no "released in" or "exists yet" snapshots. The code and git show those.
- Don't update project memory after every change. Do it when asked, when a memory would cause real mistakes, or once at session end.
- An HTML deliverable is a standalone `.html` with a full skeleton. Look at it with `firefox --headless --profile <tmp> --screenshot`.