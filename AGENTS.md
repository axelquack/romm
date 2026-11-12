# Repository Instructions

Read and follow [CLAUDE.md](CLAUDE.md) for all repository instructions.


## Role

- **Project:** Axel's public fork of RomM (rommapp/romm), a self-hosted ROM manager and player. `origin` is `axelquack/romm`; `upstream` is `rommapp/romm`. Recent fork work is Demozoo, Pouet, and CSDb scene metadata.
- **This agent owns:** Changes in this fork that follow `CLAUDE.md` (v2 is the active frontend; v1 is frozen). Push only to `origin`, never to `upstream`, unless Axel explicitly asks.
- **Out of scope / handoff:** Unclear whether this agent also maintains sibling repos `roms-tui`, `romm-demoscene-stack`, or `igir` (the herdr `~romm` space lists them; this tree does not). Do not commit `.env`, API keys, or ROM/BIOS dumps. Do not refactor v1 except for a critical bug.

Herdr agent: Oskar (Library) · RomM fork & catalog (pane w2:p1)

## Documentation, commit & push

Standing rule from Axel (2026-11-12), for every Grok bot and herdr agent working in this repo:

- Document every change in this project: README, `docs/`, and the changelog (`CHANGELOG.md` or `docs/changelog.md`), with date and what/why.
- Commit with a clear message, then push to the repo's existing remote, public or private, after the secret check.
- Before each commit, run a secret check: `git diff --cached --name-only` and `git diff --cached`. Never commit `.env*`, keys, tokens, `auth.json`, credentials, session exports, or `*.bak*` files. If one is staged, unstage it and add it to `.gitignore`.
- Public repos (`gh repo view --json visibility`): be extra strict. Before pushing, review the full diff being pushed (`git diff @{u}..HEAD`) for secrets, tokens, private IPs and hostnames the repo does not already contain, personal data, and session exports. If anything looks sensitive, do not push; report it to Axel.
- If the repo has no remote, commit locally and report that.
- Commit only your own change; do not sweep in someone else's uncommitted work.
