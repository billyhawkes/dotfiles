---
description: Create a git commit with a conventional message
subtask: true
model: opencode/minimax-m2.5
---

Run `git add .` then create a commit.

Here is the current git status and staged diff:
!`git status`
!`git diff --staged`

Create a git commit using the staged changes above.

Analyze the changes and generate a proper commit message.

Use these prefix types:
- task: general tasks (ex. documentation, localizations, etc)
- fix: bug fixes
- improve: improvements of existing features or code
- feat: new features or additions

Never invent new prefixes; use task as fallback.

Issues to close (optional): $ARGUMENTS

