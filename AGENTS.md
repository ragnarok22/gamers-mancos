# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Commands

- `pnpm dev` — dev server at localhost:4321
- `pnpm build` — production build to ./dist/
- `pnpm preview` — preview production build
- `pnpm format` — format with Prettier (Astro + Tailwind plugins)
- `pnpm format:check` — check formatting without writing
- `pnpm lint` — lint with ESLint (Astro plugin)
- `pnpm lint:fix` — lint and auto-fix
- `pnpm typecheck` — typecheck with `astro check`

No test runner is configured. No Makefile. CI runs format:check, lint, and typecheck on push/PR to main.

## Architecture

Astro 5 static site showcasing gamer profiles. Spanish language. Cyber/neon dark theme.

**Stack:** Astro 5, Tailwind CSS 4 (via `@tailwindcss/vite` plugin), GSAP for animations.

**Single page app** — `src/pages/index.astro` renders `Layout` → `GamersArena`.

- `src/components/GamersArena.astro` — main component. Contains the gamer data array, the fullscreen layout (background, logo, spotlight area, bottom thumbnail bar), and all GSAP animation logic in a `<script>` tag. To add a gamer, add an entry to the `gamers` array and place their photo in `public/gamers/`.
- `src/layouts/Layout.astro` — HTML shell. Loads Google Fonts (Orbitron, Inter), global CSS, sets `lang="es"`.
- `src/styles/global.css` — Tailwind import + `@theme` block defining the color palette and font tokens.

## Style Conventions

- Path alias: `@/*` maps to `./src/*` (configured in tsconfig.json)
- Tailwind v4 with Vite plugin — no `tailwind.config` file; theme tokens live in `global.css` under `@theme`
- Use CSS custom properties (`var(--color-neon-pink)`) in `<style>` blocks, not `theme()` function (Tailwind v4 scoped style limitation)
- Prettier auto-sorts Tailwind classes via `prettier-plugin-tailwindcss`
- All content is in Spanish
