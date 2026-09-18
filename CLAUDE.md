# CLAUDE.md — repo maintenance instructions

This repo is a public "learning in public" log for a Rails engineering
roadmap. The human's job is to study and write real notes/code. Your
job is the repo mechanics around that: directories, README bookkeeping,
GitHub Issues, commits. Don't write the actual learning content for
them beyond light scaffolding — the notes themselves should be theirs.

## Repo structure (keep this exact shape)

```
Ruby-on-Rails/
├── README.md
├── logs/
│   └── YYYY-Wnn.md
├── notes/
│   ├── phase-0-ruby/
│   ├── phase-1-rails-internals/
│   ├── phase-2-sql/
│   ├── phase-3-testing/
│   ├── phase-4-design-architecture/
│   ├── phase-5-infra-devops/
│   ├── phase-6-system-design/
│   ├── phase-7-modern-rails/
│   ├── phase-8-ai-native/
│   ├── phase-9-platform-breadth/
│   ├── phase-10-ml-leadership-business/
│   └── career-track/
└── exercises/
    ├── exercism/ruby/
    └── snippets/
```

One markdown file per topic in `notes/`, named as a slug of the topic
(e.g. `object-model.md`). Small code goes in `exercises/`. Anything
that grows into a real standalone project does NOT belong in this
repo — flag it to the human and suggest a new repo instead.

## The standard workflow

When the human says something like "I'm starting on <topic>" or "I
just finished <topic>", do the following, in order:

1. **Check for the GitHub Issue.**
   - If `gh` (GitHub CLI) is installed and authenticated (`gh auth status`),
     use it to create the Issue: `gh issue create --title "<topic>" --body "<short description>"`.
   - If `gh` isn't available, tell the human to create the Issue manually
     on github.com and give you the Issue number before you proceed —
     don't guess a number.

2. **Create or update the note file** at
   `notes/<phase-folder>/<topic-slug>.md`, with a simple structure:
   ```markdown
   # <Topic title>

   Issue: #<N>

   ## Notes

   (leave this section for the human to fill in, or lightly scaffold
   with headers based on the roadmap's stated subtopics — don't invent
   the actual content)

   ## Code / examples

   ```
   Do not write the substantive learning notes yourself unless the
   human explicitly pastes content and asks you to clean it up or
   reformat it.

3. **Update the matching checkbox in README.md** for that topic:
   ```
   - [ ] <topic text> [(#N)](https://github.com/imlakshay08/Ruby-on-Rails/issues/N)
   ```
   Use the explicit `[text](url)` link form, not a bare `#N` — bare
   autolinks have been unreliable in this repo before.
   When the human says the topic is *done*, change `- [ ]` to `- [x]`.

4. **Commit with a conventional message**:
   - Starting a topic: `docs: start notes on <topic> (#N)`
   - Finishing a topic: `docs: complete notes on <topic>, closes #N`
     (the `closes #N` auto-closes the Issue on push)
   - Always run `git status` and show the human a summary of what
     changed before committing.

5. **Do not `git push` without explicit confirmation.** Stage and
   commit locally, then ask "ready to push?" and wait for a yes.

## Weekly logs

If the human says "let's do this week's log" (or similar), create
`logs/YYYY-Wnn.md` (ISO week number) with:
```markdown
## Week of <date range>

- What I learned:
- What I built:
- One thing an AI agent got wrong that I caught:
```
Prompt the human for the actual bullet content — don't fabricate it
from commit history alone, though you can use commit history and
closed Issues from that week as a memory aid to ask better questions.

## Things you should never do unprompted

- Never rewrite or delete existing notes content — only add/append
  unless explicitly told to edit.
- Never close an Issue without a corresponding finished note file.
- Never invent progress (checking boxes, closing issues) that the
  human hasn't actually confirmed is done.
- Never push to the remote without explicit confirmation each time.

## Quick reference for the human's prompts

These are the phrasings this file is built to respond well to:
- "Starting Phase 0, topic 1 — object model. Set it up."
- "Finished the object model notes, here's what I learned: <paste>.
  Wire it up and commit, don't push yet."
- "Let's do this week's log."
- "Push everything."
- "Show me what's still open in Phase 0."
