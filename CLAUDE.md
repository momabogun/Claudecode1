# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Layout

The git root contains a single app, `momo-project/` (Vue 3 + Vite, plain JavaScript, no TypeScript). Run all npm commands from inside `momo-project/`. Requires Node `^22.18.0` or `>=24.12.0`.

## Commands

```bash
cd momo-project
npm install
npm run dev       # Vite dev server (vite-plugin-vue-devtools enabled)
npm run build     # production build
npm run preview   # serve the production build
npm run format    # prettier --write --experimental-cli src/
```

There is no test runner or linter configured.

## Notes

- `vue` and all `@vue/*` packages are pinned to the `rc` tag via `overrides` in `package.json`; keep them in sync when upgrading.
- Path alias `@` → `momo-project/src` (set in both `vite.config.js` and `jsconfig.json`).
- Prettier style: no semicolons, single quotes, 100-column width.
- The app is still the default Vue starter scaffold: `src/main.js` mounts `App.vue`, which renders `HelloWorld` and `TheWelcome` (with `WelcomeItem` and `components/icons/*`). Global styles are in `src/assets/base.css` and `main.css`.
