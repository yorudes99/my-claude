# Working with me

## Scope
- Do only what was asked. Nothing adjacent.
- Never add items to a list I didn't ask for.
- If I ask "what should we do", answer with my options, not yours.
- Approval for one action does not extend to the next.

## Honesty
- Verify before claiming: read the file, run the command, paste the output.
- If unverified, write "I have not verified this" on its own line.
- Never write "should work". Run it, or say you didn't run it.
- When corrected: state the fix in one line, then continue. No re-explaining.

## Output
- If one sentence works, do not write three.
- No table unless comparing two or more things.
- Never recap what you just did unless I ask.

## Research
- Look up any library, CLI, or version question before touching it.
- Do not trial-and-error through fixes.
- Cite what you checked.

# This Mac

## Language servers
- `typescript-language-server` + `typescript@5` installed via **npm** global.
  Never pnpm — its isolated store breaks tsserver resolution.
- Never `typescript@7` — native Go port, ships no `lib/tsserver.js`.
- `pyright` via pnpm global. Both symlinked into `~/.local/bin`.

## Shell
- `cat` is a function: `bat` at a TTY, real `cat` when piped. Heredocs are safe.
- Claude Code's shell snapshot drops single-underscore zsh functions. A
  `command_not_found_handler` in `.zshrc` absorbs the omz-nvm helpers.
- `~/Library/pnpm/global/5` is pinned to pnpm's v10 store. Leave it alone —
  `pm2` and `buddy-reroll` live there.

## Toolchain
- node v24.18.0 via nvm, lazy-loaded. Sourcing nvm.sh costs ~0.8s.
- `python3` is Apple's 3.9.6. Brew `python@3.13` and `uv` are installed.
