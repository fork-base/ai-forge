# Git Conventions

- [GC1] Commit message format is as follows:

```
<type>(<scope>): <description>

<body>

<footer>
```

 - type -- The standard types are `feat`, `fix`, `refactor`, `docs`, `style`, `test`, `chore`, and `build`.
 - scope -- Reach of the changes in the projects (e.g. backtester).
 - description -- What was done in this commit (<=50 characters long).
 - body -- Why was this change done. Never describe how. Written in imperative.
 - footer -- Lore footer. Contains Agent ID, issue id/link, and agent-model.

```
Co-authored-by: claude-code[bot] <claude@anthropic.com>
Agent-Model: claude-sonnet-4-5
Triggered-by: issue #42
```

- [GC2] Commit message types map directly onto SemVer. `feat!` or `BREANKING CHANGE:` bumps major. A `feat` bumps minor. And all other tpyes bump patch.
- [GC3] Agents open a new branch when they work on a new user story or issue. This branch is prefixed with `bot/` (e.g. `bot/<us-id>-<slug>`). When done with the story, create a PR for the human to review.
- [GC4] Before creating a PR do the following:
 - Review the code to see if it works and fulfills all requirements of the user story.
 - Review the code for quality standards of the project.
 - Squash branch commit history and rewrite the commit history into a coherent story before creating a PR (using `git rebase -i`).
 - Before passing PR to a human, review the PR.
- [GC5] Pre-commit hooks need to pass before commit can be made.
- [GC6] Never merge or push to `main`.
