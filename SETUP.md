# Publishing this profile README

GitHub shows a profile README from a repository named exactly after the username: `TituJesh/TituJesh`.
The banner, cards and stack are SVG files that live in that repo, so push the whole folder, not just `README.md`.

## 1. Create the repository

Create a **public** repo called `TituJesh` at https://github.com/new and leave it empty (no README, no licence),
or with the GitHub CLI:

```bash
gh repo create TituJesh/TituJesh --public --description "Profile README"
```

## 2. Push these files

From inside this folder:

```bash
git init
git add README.md assets
git commit -m "Add profile README"
git branch -M main
git remote add origin https://github.com/TituJesh/TituJesh.git
git push -u origin main
```

The profile page updates within a minute of the push.

## What's in here

| Path | Purpose |
| --- | --- |
| `README.md` | The profile page |
| `assets/hero-light.svg`, `assets/hero-dark.svg` | Banner. GitHub picks one based on the viewer's theme. The avatar is embedded inside it |
| `assets/card-*.svg` | The three project cards (each is a link in the README) |
| `assets/stack-*.svg` | The four-column stack strip |
| `assets/label-*.svg` | The small section labels with the self-drawing rule |

## Editing later

- Text in the banner, cards and stack lives inside the SVGs. Open the file and change the text between the `<text>` tags; keep lines roughly the same length so nothing overflows.
- The intro paragraph and the contact links are plain HTML in `README.md`.
- To add a project, copy one of the `<a><picture>…</picture></a>` blocks in `README.md` and duplicate a card SVG with the new text. The cards are 32% wide each, so three per row.
- The avatar inside the banner is a baked-in copy. If the GitHub profile picture changes, re-embed it or remove the `<image>` element from both hero SVGs.
