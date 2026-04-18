# My Blog

Just my public and online notes and thoughts.

This blog is built using [Quartz](https://quartz.jzhao.xyz/), a static site generator for Obsidian vaults.

## Setup

- Content is in the `content/` directory (formerly `vault/`).
- Built with Quartz 4.
- Hosted on GitHub Pages.

## Local Development

1. Install dependencies: `npm install`
2. Build and serve: `npx quartz build --serve`
3. Open http://localhost:8080

## Deployment

Pushes to `main` branch trigger GitHub Actions to build and deploy to GitHub Pages.

Make sure to:
- Set `baseUrl` in `quartz.config.ts` to your GitHub Pages URL (e.g., `username.github.io/blog`).
- Enable GitHub Pages in repo settings with source: GitHub Actions.

## Sponsors

<p align="center">
  <a href="https://github.com/sponsors/jackyzha0">
    <img src="https://cdn.jsdelivr.net/gh/jackyzha0/jackyzha0/sponsorkit/sponsors.svg" />
  </a>
</p>
