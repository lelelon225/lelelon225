# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this repo is

This is the special GitHub **profile repo** for user `lelelon225` (repo name matches the username). GitHub renders `README.md` directly on the user's profile page at `github.com/lelelon225`. There is no application code, build system, or test suite — the repo's only "output" is that rendered README.

## Structure

- `README.md` — the profile page content. Uses external badge/widget services (capsule-render, readme-typing-svg, github-readme-stats, nirzak-streak-stats, github-profile-trophy, github-contributor-stats, skillicons.dev, img.shields.io) embedded as images, so changes are visible purely by editing markdown/HTML — there's nothing to build or compile.
- `.github/workflows/snake.yml` — generates the animated "contribution snake" SVGs (via `Platane/snk`) and publishes them to the `output` branch (via `crazy-max/ghaction-github-pages`), which `README.md` then references directly from `raw.githubusercontent.com`. Runs on push to `main`, daily via cron, and on manual dispatch.

## Working in this repo

- There is nothing to lint, build, or test. Verify changes by checking that the markdown/HTML renders correctly (e.g. preview on GitHub) and that embedded widget URLs are well-formed.
- When editing README badges/widgets, match the existing color scheme: dark background (`0D1117`), cyan accent (`00F5FF`), violet accent (`B967FF`), light gray text (`C9D1D9`).
- The `output` branch is generated entirely by `snake.yml` — never hand-edit it.
- Don't rename `README.md`/change the default branch — GitHub only renders the profile page from `README.md` on the repo's default branch.
