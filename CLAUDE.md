# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a Jekyll-based academic personal website template that showcases research publications, career highlights, and professional information. The site is designed for academics and researchers to present their work with interactive features and clean styling.

## Architecture

### Core Structure
- **Jekyll Static Site**: Uses Jekyll 4.3 with the Minima theme
- **Data-Driven Content**: All content is managed through YAML files in `_data/` directory
- **Dual Layout System**: Two main page types - landing page (`index.html`) and CV page (`cv.html`)
- **Interactive Media**: Supports video hover effects for publication previews

### Key Directories
- `_data/`: Contains all site content as YAML files (publications, employment, education, authors, highlights, news)
- `css/`: SCSS stylesheets with Bulma CSS framework integration
- `images/`: Publication images, videos, and portrait photos
- `js/`: JavaScript for interactive features (mainly video hover effects)

### Content Management
All site content is managed through YAML files:
- `publications.yml`: Research papers with metadata, links, and media
- `employment.yml`: Work history and positions
- `education.yml`: Academic background
- `authors.yml`: Collaborator information with links
- `highlights.yml`: Featured work for the landing page
- `news.yml`: Recent updates and announcements

## Development Commands

### Local Development
```bash
# Install dependencies
bundle install

# Serve locally with live reload
bundle exec jekyll serve

# Build for production
bundle exec jekyll build
```

### Git Workflow
This repository is connected to GitHub Pages at https://jkim89.github.io

```bash
# Check current status
git status

# Stage all changes
git add .

# Commit with descriptive message
git commit -m "Description of changes"

# Push to GitHub (automatically deploys to GitHub Pages)
git push origin main
```

### Content Updates
When updating content, modify the appropriate YAML files in `_data/`. The Jekyll templating system will automatically render changes. After making changes, use the Git workflow above to deploy to GitHub Pages.

## Key Features

### Publication System
- Supports project pages, arXiv links, GitHub repositories
- Interactive hover effects show videos when available
- Author highlighting for the site owner
- Venue and award display

### Responsive Design
Uses Bulma CSS framework with custom SCSS for:
- Mobile-responsive layouts
- Publication grid systems
- Interactive media elements
- Academic styling conventions

### Media Integration
- Automatic video/image switching on hover
- Support for MP4 videos and standard image formats
- Optimized media loading and display

## Site Configuration

Primary configuration in `_config.yml`:
- Personal information (name, email, social links)
- Google Analytics integration
- Jekyll build settings
- SCSS compilation options

The site uses Google Fonts (Google Sans, Noto Sans) and integrates Font Awesome and Academicons for iconography.

## Reference URLs

### Project Page Sources
- **Computational Imaging Publications**: https://www.computationalimaging.org/publications/
  - Contains project pages for Stanford holography research
  - Neural Holography, Holographic Glasses, Time-multiplexed Neural Holography, etc.

- **NVIDIA Research Profile**: https://research.nvidia.com/person/jonghyun-kim
  - Contains NVIDIA-era publications and projects
  - Foveated AR, Prescription AR, and other AR/VR display research

- **Google Scholar Profile**: https://scholar.google.com/citations?user=QKsqzVEAAAAJ
  - Complete publication list with citation counts
  - Useful for finding arXiv links and publication metadata

### Publication Venues
- **SIGGRAPH/SIGGRAPH Asia**: ACM Digital Library
- **Nature**: https://www.nature.com/
- **Optics Letters/Optica**: Optica Publishing Group
- **Science Advances**: https://www.science.org/journal/sciadv