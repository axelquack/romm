# Changelog

## 2026-11-13

- Patched frontend npm advisories in the lockfile: handlebars 4.7.10, Storybook 10.6.2, vue-i18n 11.4.14, Vue and @vue/server-renderer 3.5.42, axios 1.20.0, happy-dom 21.0.4, vite 8.1.6, ws 8.21.3, markdown-it 14.3.3. The rolldown override is 1.1.5 so Vite 8.1.6 can load, and engine.io-client 6.6.7 unlocks ws 8.21. Upstream master already has these fixes, mixed into 2,504 later commits, so the fork takes the minimum patched releases instead of a full sync.
