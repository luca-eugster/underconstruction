# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this is

A single-page static website for Luca Eugster (psychotherapist and supervisor in Zurich), deployed via GitHub Pages at `www.luca-eugster.ch` (configured in `CNAME`).

No build tools, no frameworks, no package manager — just HTML and CSS.

## Structure

- `index.html` — the entire site: all markup and all CSS (inline `<style>` block)
- `index_underconstruction.html` — a "coming soon" placeholder page (not currently served; swap with `index.html` if needed)
- `images/` — local portrait photos (`luca-eugster-profil-*.jpg`)
- `favicon.ico` — site icon

## Development

Open `index.html` directly in a browser — no server needed. To preview with a local server:

```
python3 -m http.server 8000
```

Deployment is automatic: push to `main` and GitHub Pages publishes it.

## Design system

All design tokens are CSS custom properties at the top of the `<style>` block:

| Variable | Role |
|---|---|
| `--bg` | Page background |
| `--surface` | Card/panel background |
| `--text` | Body text |
| `--muted` | Secondary/lead text |
| `--accent` | Brand green |
| `--accent-dark` | Darker brand green (headings, quotes) |
| `--accent-soft` | Pale green tint |
| `--line` | Divider colour |

Font stack: Georgia serif for body; no external fonts loaded.

## Layout conventions

- `.page` — centred content wrapper, `max-width: 1120px`
- `.section` — top-bordered content block with `padding: 64px 0`
- `.section-grid` — two-column grid (`0.95fr / 1.05fr`), collapses to one column at 960 px
- `.split` — equal two-column grid, also collapses at 960 px
- Breakpoints: 960 px (tablet), 640 px (mobile)

## Language

All content is in Swiss German (`lang="de-CH"`). Keep copy in Swiss German when editing.
