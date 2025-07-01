# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a company website for Adaptive Flow Ltd built with Hugo static site generator using the Docsy theme. The site is configured for English content with automatic deployment.

## Essential Commands

### Development
```bash
# Start development server with drafts
hugo server -D

# Start development server (production-like)
hugo server

# View at http://localhost:1313
```

### Building
```bash
# Build for production
hugo --minify

# Build without minification
hugo

# Output goes to ./public/
```

### Content Management
```bash
# Create new blog post
hugo new blog/post-title.md

# Create new service page  
hugo new services/service-name.md

# Create new content page
hugo new section/page-name.md
```

### Dependencies
```bash
# Update Hugo modules
hugo mod get -u
hugo mod tidy

# Install npm dependencies (for build tools)
npm install

# Update submodules (theme)
git submodule update --init --recursive
```

## Architecture

### Hugo Configuration
- Primary config: `config.toml` (TOML format)
- Secondary config: `hugo.yaml` (YAML format) 
- Base URL configured for https://adaptiveflow.ca
- Content directory: `content/en/` (English only)
- Theme: Docsy (via Hugo modules and git submodule)

### Key Directories
- `content/en/`: All site content (Markdown files)
- `static/`: Static assets (images, favicons)
- `assets/`: Processed assets (SCSS, custom CSS)
- `themes/docsy/`: Docsy theme as git submodule
- `public/`: Generated site output (ignored in git)
- `resources/`: Hugo's generated resources cache

### Theme Integration
- Uses Google's Docsy theme v0.12.0
- Bootstrap 5.3.6 and FontAwesome 6.7.2 included
- Custom styling in `assets/scss/` files
- Theme customizations should go in project assets, not theme files

### Content Structure
- Single-language site (English)  
- Navigation configured in `hugo.yaml` menu section
- Taxonomies disabled in config
- Content lives in `content/en/` with `_index.md` as homepage

### Build Pipeline
- Hugo extended version required (v0.147.8)
- PostCSS processing for CSS (autoprefixer, postcss-cli)
- Minification available via `--minify` flag
- Git info enabled for last modified dates
- Robot.txt generation enabled

## Development Notes

### Theme Development
- Don't modify files in `themes/docsy/` directly
- Override theme files by creating same structure in project root
- Custom SCSS variables go in `assets/scss/_variables_project.scss`
- Custom styles go in `assets/scss/custom.scss`

### Content Guidelines
- All content files should be in `content/en/`
- Use proper Hugo front matter
- Follow existing content structure patterns
- Images should be optimized before adding to `static/images/`

### Deployment
- Automatic deployment configured via GitHub Actions
- Manual deployment requires `hugo --minify` then deploy `public/` directory
- Configured for various platforms (Netlify, AWS S3, etc.)