# CLAUDE.md — Brook Lab Website

## Overview

This is the [Brook Lab](https://brooklab.org) website — a Jekyll static site deployed via Netlify. Content is written in Markdown. Netlify auto-deploys on every push to `main`.

## Local Development

```bash
bundle install          # install dependencies (first time or after Gemfile changes)
bundle exec jekyll serve  # build and serve at http://localhost:4000
```

Ruby version is pinned in `.ruby-version`. Use `bundle exec` for all Jekyll commands.

## Repository Structure

```
_posts/        # news posts (Markdown)
_layouts/      # page templates: default, page, post, home, noheader
_includes/     # shared partials: header, footer, head, pagination
assets/img/    # images for news posts
assets/team/   # photos for the Team page
*.md           # top-level site pages (research, team, publications, etc.)
_config.yml    # site title, URL, plugins
```

## Adding a News Post

Create a file in `_posts/` named `YYYY-MM-DD-short-title.markdown` with this front matter:

```yaml
---
layout: post
title: Your Post Title Here
date: 2025-01-01 01:00:00 -0700
description: (optional)
img: your-image.jpg        # filename only — file goes in assets/img/
alt: Brief image alt text.
tags: [tag1, tag2]
permalink: /news/short-url-slug
---
```

Write the post body below the `---` in Markdown. HTML is allowed inline (used for image sizing/alignment).

**Image placement example:**
```html
<img src="/assets/img/your-image.jpg" alt="description" class="img-thumbnail col-md-6" />
```

Common Bootstrap width classes: `col-md-3`, `col-md-5`, `col-md-6`, `col-md-10`, `col-md-12`.
Use `class="float-start ..."` to wrap text around an image; add `<div style="clear:both;">&nbsp;</div>` after to clear the float.

Posts appear on `/news` sorted by date (newest first). The `img` field is required — it shows as the thumbnail on the news index.

## Top-Level Pages

These are Markdown files in the root directory. Each uses `layout: page` unless noted.

| File | URL | Notes |
|---|---|---|
| `index.md` | `/` | `layout: home` |
| `research.md` | `/research` | |
| `publications.md` | `/publications` | |
| `cara-brook.md` | `/cara-brook` | |
| `team.md` | `/team` | Team member photos live in `assets/team/` |
| `values-and-policies.md` | `/values-and-policies` | |
| `join.md` | `/join` | |
| `news.md` | `/news` | Lists all posts automatically |
| `programs.md` | `/programs` | |

## Navigation

Nav links are hardcoded in `_includes/header.html`. To add/remove a nav item, edit that file directly.

## Site Configuration

`_config.yml` holds the site title, URL (`https://brooklab.org`), timezone, and plugins. The only active plugin is `jekyll-sitemap`.

## Deployment

- **Production:** Netlify deploys automatically from `main`. No manual step needed after pushing.
- **CI:** GitHub Actions (`.github/workflows/jekyll.yml`) runs `jekyll build` and `htmlproofer` on every push/PR to verify the build.
