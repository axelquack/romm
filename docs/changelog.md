# Changelog

## 2026-11-16

- Merged upstream `rommapp/romm` `master` (07b193c, 15 Nov 2026) into this fork. The fork was 2,518 commits behind and 13 commits ahead. Those 13 were documentation, the `.devcontainer/dev.env` gitignore, and earlier dependency bumps.
- Conflicts were resolved by taking upstream `uv.lock`, `pyproject.toml`, `frontend/package.json`, and `frontend/package-lock.json`, and by keeping the fork notes in `AGENTS.md`, `SECURITY.md`, `docs/changelog.md`, the `.devcontainer/dev.env` gitignore, and the security and dev-container notes in `README.md` and `DEVELOPER_SETUP.md`.
- `CLAUDE.md` is now a symlink to `AGENTS.md`. Upstream moved the repository guide into `AGENTS.md` and deleted `CLAUDE.md`.
- After the sync, the upstream lockfiles already include patched releases for certifi, anyio, aiohttp, urllib3, cryptography, js-yaml, nanoid, source-map-js, browserslist, and the fast-uri highs.
- Added npm overrides for `follow-redirects` 1.16.2 (upstream still had 1.16.1) and `fast-uri` 3.1.9. `npm audit` in `frontend/` then reports 0 high and 0 critical findings. A further override pins `glob` to 14.0.2 (GHSA-3g3m-2fjr-6pw4). Trunk CI also required a single top-level heading in `AGENTS.md` and Prettier formatting of the resolved markdown files.

## 2026-11-14

- Bump Pillow from 12.3.0 to 13.0.0 (#1).
- Bump joserfc from 1.6.8 to 1.7.6 (#2).
- Bump tornado from 6.5.7 to 6.6 (#3).
- Bump Authlib from 1.6.12 to 1.9.1 (#4).
- Bump opentelemetry-api from 1.36.0 to 1.45.2 (#6).
- Bump dnspython from 2.7.0 to 2.9.2 (#7).

## 2026-11-13

- Patched frontend npm advisories in the lockfile: handlebars 4.7.10, Storybook 10.6.2, vue-i18n 11.4.14, Vue and @vue/server-renderer 3.5.42, axios 1.20.0, happy-dom 21.0.4, vite 8.1.6, ws 8.21.3, markdown-it 14.3.3. The rolldown override is 1.1.5 so Vite 8.1.6 can load, and engine.io-client 6.6.7 unlocks ws 8.21. Upstream master already has these fixes, mixed into 2,504 later commits, so the fork takes the minimum patched releases instead of a full sync.
- Stopped tracking `.devcontainer/dev.env`. The dev container copies `.devcontainer/dev.env.example` to the gitignored `.devcontainer/dev.env` when that file is missing. Credential placeholders in the example are `changeme`.
- Noted that Dependabot alerts and automatic security updates are enabled on this fork as of 2026-11-13.
