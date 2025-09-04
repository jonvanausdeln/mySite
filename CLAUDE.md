# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a Quarto-based personal website for Jon Vanausdeln hosted at https://www.jonvanausdeln.com. The site uses Quarto's static site generation to create a personal website with blog functionality. Most of the content will have a technology focus and Software Quality assurance.

## Architecture

- **Quarto Website**: Built using Quarto with YAML configuration in `_quarto.yml`
- **Content Structure**: 
  - Main pages: `index.qmd`, `about.qmd`, `blog.qmd` 
  - Blog posts: Individual directories under `blog-posts/` containing `index.qmd` files
  - Static assets: `JRV-logo.png`, `styles.css`
- **Theme**: Uses "slate" and "brand" themes with custom CSS
- **Deployment**: Automated via GitHub Actions to GitHub Pages

## Development Commands

Since this is a Quarto project, the primary commands are:

```bash
# Preview the site locally (serves at localhost:4200 by default)
quarto preview

# Render/build the site
quarto render

# Publish to GitHub Pages (handled automatically by CI/CD)
quarto publish gh-pages
```

## Content Management

- **Blog Posts**: Create new directories under `blog-posts/` with an `index.qmd` file
- **Pages**: Add new `.qmd` files in the root directory and update navigation in `_quarto.yml`
- **Styling**: Modify `styles.css` for custom styling
- **Site Configuration**: Update `_quarto.yml` for site-wide settings

## Deployment

The site automatically deploys to GitHub Pages via the workflow in `.github/workflows/publish.yml` when changes are pushed to the main branch. The workflow uses Quarto's official GitHub Actions.

## Key Configuration

- Site metadata and navigation defined in `_quarto.yml`
- Google Analytics tracking enabled
- Open Graph metadata enabled
- Freeze execution mode for reproducible builds