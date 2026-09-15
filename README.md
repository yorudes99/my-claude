# my-claude

My global [Claude Code](https://claude.com/claude-code) configuration — the rules,
settings, and machine notes that follow me into every project.

Claude Code loads `~/.claude/CLAUDE.md` in every session regardless of which
directory you launch from. Per-repo `./CLAUDE.md` files stack on top of it rather
than replacing it, so this repo holds only what is true of *me* and *this machine*.

## Contents

| File | Purpose |
| --- | --- |
| `CLAUDE.md` | Global instructions: how I want Claude to work, plus environment gotchas |
| `.gitignore` | Allowlist — everything in `~/.claude` is ignored except the files above |

Everything else in `~/.claude` is machine state Claude Code manages itself
(`sessions/`, `projects/`, `plugins/`, `history.jsonl`, …) and is deliberately
not tracked.

## Install

```bash
git clone git@github.com:yorudes99/my-claude.git ~/.claude-repo
cp ~/.claude-repo/{CLAUDE.md,.gitignore} ~/.claude/
```

Or, to version `~/.claude` in place:

```bash
cd ~/.claude
git init
git remote add origin git@github.com:yorudes99/my-claude.git
git fetch origin && git reset --soft origin/main
```

## Conventions

`CLAUDE.md` is a log of mistakes that already happened, not a wishlist. A rule
earns its place only after something went wrong without it. Kept under 200 lines —
longer files measurably reduce adherence.
