# AGENTS.md — instructions for Codex / coding agents

## What this is
A personal academic homepage for Qingsong Pan (economist, empirical IO /
structural econometrics). It is a **plain static site**: hand-written HTML and
CSS, **no build system, no framework, no npm/Ruby/Jekyll**. It is hosted as a
GitHub Pages *user site* (`<username>.github.io`).

## Files
- `index.html` — the entire site (single page; sections: About, Research, Teaching).
- `styles.css` — all styling. Design tokens live in `:root` at the top.
- `assets/` — images (e.g. `photo.jpg`).
- `.nojekyll` — empty file; tells GitHub Pages to skip Jekyll processing.

## Run / preview locally
```bash
python3 -m http.server 8000      # then open http://localhost:8000
```
There is **no build step**. Editing a file and refreshing the browser is the
whole loop.

## Deploy
Pushing to the default branch publishes automatically (GitHub Pages user site).
Do **not** add a build pipeline or static-site generator unless explicitly asked.

## Hard rules
1. **Never change factual academic content** — paper titles, coauthor names and
   links, journal names, R&R / publication status, years, or PDF URLs — unless
   I explicitly ask. These are real records; a hallucinated edit here is the
   worst possible failure. If unsure, leave it and ask.
2. **Preserve every existing hyperlink** exactly (CV, papers, coauthor pages).
3. Stay dependency-free: vanilla HTML/CSS; add vanilla JS only if genuinely
   necessary and say why.
4. Keep the quality floor: responsive down to ~360px, visible `:focus-visible`
   outlines, `prefers-reduced-motion` respected, semantic HTML, AA contrast.
5. Make **small, targeted diffs**. Don't refactor or reflow unrelated code.

## Before reporting a change as done
- Start the preview server and confirm the page actually renders.
- Check it at a narrow (mobile) width as well as desktop.
- Summarize exactly what changed and confirm rule 1 was not touched.
