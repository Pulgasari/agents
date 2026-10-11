# agents

central rules for working with coding agents (claude code & co.), shared across all projects so the basics do not drift apart.

## files

| file          | content                                           |
| ------------- | ------------------------------------------------- |
| `AGENTS.md`   | entrypoint, imports all modules below             |
| `chat.md`     | communication & tone                              |
| `code.md`     | language, structure, formatting, naming, comments |
| `workflow.md` | how to approach work (architecture, tests)        |
| `templates/`  | starter files for projects                        |

## usage in a project

each project gets a thin root `CLAUDE.md` (see `templates/CLAUDE.md`):

```md
@../agents/AGENTS.md

# project
- project-specific rules only
```

- the `@` import is resolved relative to the importing file, so this repo has to be checked out **next to** the project (e.g. `~/code/agents` + `~/code/aufbau`). in cloud sessions, add `pulgasari/agents` as an additional repository.
- project rules in `CLAUDE.md` override the central ones.
- claude code only picks up `CLAUDE.md` in the repo root or `.claude/CLAUDE.md`, not in arbitrary subfolders.

### globally (local cli)

to apply the rules to every project on a machine, import them once in `~/.claude/CLAUDE.md`:

```md
@~/code/agents/AGENTS.md
```

### other agents

tools that read `AGENTS.md` but do not resolve `@` imports (codex, jules, ...) do not see the module contents. point them at this repo explicitly in their prompt or config.
