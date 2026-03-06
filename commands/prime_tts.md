---
allowed-tools: Bash, Read
description: Load context for a new agent session by analyzing codebase structure and README
---

# Prime

Load essential context for a new agent session.

## Steps

1. **Structure** — Run `git ls-files` (or `ls -R` if not a git repo) to understand the codebase
2. **README** — Read `README.md` (or `readme.md`) if it exists
3. **Project instructions** — Read `CLAUDE.md` if it exists
4. **Documentation** — Check for and read any docs that exist:
   - `ai_docs/` directory — read all `.md` files if the directory exists
   - `docs/` directory — read top-level `.md` files (not subdirectories) if it exists
5. **Report** — Provide a concise summary of the project

When you finish, run the TTS summary agent and let the user know you're ready to build.
