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

## Development Session Lessons Learned

### What Worked Well (Tasks Completed Successfully)

1. **Initial Setup and Configuration**
   - ✅ Successfully updated `_config.yml` with personal information
   - ✅ Git repository connection and push workflow established
   - ✅ Basic site structure understanding and navigation

2. **Data Structure Updates**
   - ✅ Employment and education data properly transferred from CV
   - ✅ Profile picture replacement workflow
   - ✅ CLAUDE.md documentation creation with development commands

3. **UI/UX Improvements**
   - ✅ Commenting out long descriptions in highlights.yml for cleaner design
   - ✅ Publications sorted in reverse chronological order (latest first)

### Critical Issues That Required Multiple Attempts

1. **Publication Data Accuracy** ⚠️
   - **Problem**: Author lists were frequently incorrect or incomplete
   - **Root Cause**: Insufficient cross-referencing between multiple authoritative sources
   - **Example**: AI-mediated 3D Video Conferencing had completely wrong authors initially
   - **Solution Applied**: Systematic verification against NVIDIA research page, CV, and project sites

2. **Publication Information Verification** ⚠️
   - **Problem**: Titles, venues, and author orders were often inaccurate
   - **Examples**: 
     - "Matching Prescription & Visual Acuity" missing full title and Best in Show Award
     - "Varifocal Virtuality" incorrect title format
     - "Neural Holography" venue confusion (SIGGRAPH vs Emerging Tech)
   - **Solution**: Multiple rounds of corrections using primary sources

3. **Missing Publications** ⚠️
   - **Problem**: Significant publications were missing from initial import
   - **Root Cause**: Insufficient comprehensive review of NVIDIA research page
   - **Solution**: Systematic addition of 9+ missing publications with proper author attribution

### Best Practices for Future Development

1. **Publication Data Management**
   - ALWAYS cross-reference multiple sources: CV, Google Scholar, NVIDIA research page, Stanford publications
   - Verify exact titles, author order, and venue information before committing
   - Use WebFetch to pull accurate data from authoritative sources
   - Double-check recent publications (2023-2024) as they're most likely to have errors

2. **Author Information**
   - Maintain consistent author ID format in authors.yml
   - Verify author spelling and affiliations
   - Include proper website links when available
   - Mark the main author (is_me: true) correctly

3. **Data Verification Workflow**
   ```
   1. Extract data from primary source (CV/official websites)
   2. Cross-reference with secondary sources
   3. Verify author lists and order
   4. Confirm exact titles and venues
   5. Test links and project pages
   6. Commit changes
   ```

4. **Quality Assurance**
   - Read data back after updates to catch obvious errors
   - Test website functionality after major changes
   - Maintain chronological organization
   - Keep descriptions consistent in length and style

### Technical Implementation Notes

- GitHub Pages deployment works reliably with push workflow
- Jekyll builds handle YAML data structure changes well
- Project page links from computationalimaging.org are reliable
- NVIDIA research page is the most authoritative source for recent work
- CV PDF contains the most comprehensive publication list

### Common Pitfalls to Avoid

1. Don't assume author lists - always verify from primary sources
2. Don't copy-paste without cross-checking accuracy
3. Don't commit large data changes without reviewing output
4. Don't ignore venue vs conference vs journal distinctions
5. Don't skip verification of publication years and chronological order