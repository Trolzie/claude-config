---
allowed-tools: Bash, Read
description: Load context for a new agent session by analyzing codebase structure, documentation and README
---

# Prime

Load essential context for a new agent session.

## Steps

1. **Structure** — Run `git ls-files` (or `ls -R` if not a git repo) to understand the codebase
2. **README** — Read `README.md` (or `readme.md`) if it exists
3. **Project instructions** — Read `CLAUDE.md` if it exists (note: also auto-loaded, but reading it explicitly helps you reference specific sections in your report)
4. **Documentation** — Check for and read any docs that exist:
   - `ai_docs/` directory — read all `.md` files if the directory exists
   - `docs/` directory — read top-level `.md` files (not subdirectories) if it exists
5. **Report** — Provide a concise summary:
   - What the project does
   - Tech stack and key dependencies
   - Project structure highlights
   - Key patterns or conventions from CLAUDE.md (if present)
   - Notable documentation found
