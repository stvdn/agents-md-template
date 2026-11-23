# AGENTS.md template

A reusable [`AGENTS.md`](./AGENTS.md) for AI coding agents (Claude Code, Codex, Cursor, Copilot, and others).

It covers only what an agent **can't infer from your code**: branch naming, commit format, PR structure, when to run checks, and what to ask before doing.
There's no stack, folder map or style guide here, because agents can read those from the repo.

## What's inside

| Section | What it sets |
| --- | --- |
| Branches | `<type>/<description>` naming, one branch per task, never on `main` |
| Commits | Conventional Commits, small focused commits, no secrets |
| Pull requests | What / Why / How to test / Notes, draft until ready, squash merge |
| Checks | Run tests at the end of a task, not after every edit; `wip` pauses them |
| Ask first | Push, PR, merge, dependencies, schema, destructive commands |
| Never | Force-push, skip hooks, commit to `main` |

## Usage

1. Copy [`AGENTS.md`](./AGENTS.md) into the root of your project.
2. Edit anything that doesn't match how you work.
3. **Claude Code users:** Claude Code reads `CLAUDE.md`, not `AGENTS.md`. Copy [`CLAUDE.md`](./CLAUDE.md) too; its single line `@AGENTS.md` imports the same rules, so every agent shares one file.

Quick copy from the command line:

```bash
curl -O https://raw.githubusercontent.com/stvdn/agents-md-template/main/AGENTS.md
```

## Tips

- Keep it short. Every line is loaded into the agent's context on every task.
- When an agent makes the same mistake twice, add a one-line rule for it.
- Remove rules your linter, formatter or CI already enforce.

## Contributing

Suggestions are welcome. Open an issue or a PR with the rule you'd add and why.

## License

[MIT](./LICENSE)
