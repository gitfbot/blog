---
title: Launching This Blog
date: 2026-04-18
tags:
  - blog
  - github-pages
  - quartz
  - obsidian
---

I finally got this blog live, and I wanted my first post to be about that process while it is still fresh in my head.

The goal was pretty simple: I wanted this GitHub repo to become a blog hosted on GitHub Pages, with Quartz turning an Obsidian-style folder of notes into an actual site. I had a starter setup already, but it still felt more like "Quartz, the project" than "my blog, on purpose."

## What We Started With

The repo was close, but not fully pointed at the right destination yet.

There was starter content, some placeholder config, and a bunch of GitHub files that made sense for the Quartz maintainers but not really for me as someone trying to publish a personal blog. The biggest configuration issue was the `baseUrl`, because GitHub Pages project sites are picky about that. If the repo is `gitfbot/blog`, the published site lives at `https://gitfbot.github.io/blog`, not just the root domain.

That was one of the first lessons: static site generators can be mostly correct and still fail in ways that feel mysterious if one important URL setting is wrong.

## What We Changed

We cleaned the repo up and made it actually match the project I wanted:

- updated the site config to point at my real GitHub Pages URL
- simplified the package scripts so local development was clearer
- cleaned out extra upstream GitHub templates and workflows I did not need
- updated the README so future me can remember how this is supposed to work
- replaced the starter pages with content that actually belongs to this blog

That part felt good because it turned the repo from a borrowed scaffold into something that felt like mine.

## The Deploy Error

The most confusing part was that the site built fine locally, but the GitHub Pages deployment still failed.

The failure happened in the `actions/deploy-pages` step with a `404 Not Found`, which is not the kind of error message that immediately makes me think, "oh, Pages itself is not enabled yet." But that was the problem. The workflow had an artifact ready to deploy, but GitHub Pages was not fully turned on for the repo, so the deployment step had nowhere to go.

Once GitHub Pages was enabled with `GitHub Actions` as the source, the deploy could finally succeed.

That was another useful lesson: a successful build is not the same thing as a successful publish.

## Re-Running the Actions

Another little adventure was figuring out how to re-run the failed workflow.

I did not immediately see the right UI button, so I asked whether this could be done from the command line. It turns out the GitHub CLI is really nice for this once you are logged in. After authenticating, I could inspect the Pages settings, check workflow runs, and confirm that newer deploys had already succeeded.

That felt much better than clicking around and guessing.

## Lessons Learned

- `baseUrl` matters a lot on GitHub Pages project sites
- local success does not guarantee deployment success
- starter repos often come with extra baggage that is worth trimming
- GitHub CLI is excellent when the web UI is not obvious
- the first publish is the hardest part, because you are really learning the whole chain

## What Happens Now

Now the workflow is the part I wanted all along: write Markdown in `content/`, push to `main`, and let GitHub Actions publish the site.

That means I can spend less time thinking about infrastructure and more time actually writing.

Which is a pretty good way to start a blog.
