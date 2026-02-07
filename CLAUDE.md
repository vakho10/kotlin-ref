# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a Jekyll static site generator project (Ruby-based blog). Despite the directory name "kotlin-ref", this is not a Kotlin project.

## Build Commands

```bash
cd docs
bundle install              # Install Ruby dependencies
bundle exec jekyll serve    # Run local development server (http://localhost:4000/kotlin-ref/)
bundle exec jekyll build    # Build static site to _site/
```

Note: Changes to `_config.yml` require restarting the server.

## Project Structure

- `docs/` - Jekyll source files (deployed via GitHub Pages from /docs)
  - `_posts/` - Blog posts (markdown with YAML frontmatter)
  - `_config.yml` - Jekyll site configuration
  - `Gemfile` - Ruby dependencies (github-pages gem, Minima theme)
  - `index.markdown`, `about.markdown` - Static pages
  - `_site/` - Generated output (gitignored)

## Content Format

Posts use YAML frontmatter:
```yaml
---
layout: post
title: "Post Title"
date: YYYY-MM-DD HH:MM:SS +/-TTTT
categories: category1 category2
---
```

## Theme

Uses the Minima theme (~> 2.5). Theme files are external; override by creating matching files in `docs/`.
