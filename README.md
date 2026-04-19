# My Blog
---
https://gitfbot.github.io/blog
---
This repo is set up to publish an Obsidian-style blog with [Quartz](https://quartz.jzhao.xyz/) and host it on GitHub Pages.

## Where to write

Put public notes and posts in `content/`.

- `content/index.md` is the homepage.
- Any other Markdown file in `content/` becomes a page on the site.
- Obsidian wikilinks like `[[My Note]]` work.
- Private notes can stay outside this repo, or in ignored folders like `.obsidian/`, `private/`, and `templates/`.

## Local development

1. Install dependencies: `npm install`
2. Start the local site: `npm run dev`
3. Open `http://localhost:8080`

## Deploy to GitHub Pages

This repo already includes a GitHub Actions workflow that deploys on pushes to `main`.

In GitHub, open this repository and set:

1. `Settings` -> `Pages`
2. `Source` -> `GitHub Actions`

The configured site URL for this repo is:

- `https://gitfbot.github.io/blog`

## Useful commands

- `npm run dev` - build and serve locally
- `npm run build` - produce the static site in `public/`
- `npm run check` - typecheck and run formatting checks
