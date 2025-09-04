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

4. **Systematic Author Verification (Today's Session)**
   - ✅ **Complete DOI-based verification of all 29 publications completed**
   - ✅ Added DOI information to arxiv field for all publications
   - ✅ Verified and corrected author lists across entire publication database
   - ✅ Fixed critical author errors including 2011 paper correction
   - ✅ Updated authors.yml with missing author entries (gunheepark → gilbaepark correction)

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

4. **Critical Author Verification Issues (Resolved Today)** ✅
   - **Problem**: Multiple author errors throughout the database, including incorrect author spellings and missing authors
   - **Specific Example**: 2011 paper had "gunheepark" instead of correct "gilbaepark" (Gilbae Park)
   - **Solution Applied**: Implemented systematic 4-step DOI verification process:
     1. Search publication title to find DOI
     2. Add DOI to arxiv field in publications.yml
     3. Fetch DOI page to verify exact author list
     4. Update authors if incorrect
   - **Result**: All 29 publications now have verified DOI and accurate author information

### Best Practices for Future Development

1. **Publication Data Management**
   - ALWAYS cross-reference multiple sources: CV, Google Scholar, NVIDIA research page, Stanford publications
   - Verify exact titles, author order, and venue information before committing
   - Use WebFetch to pull accurate data from authoritative sources
   - Double-check recent publications (2023-2024) as they're most likely to have errors
   - **NEW**: Use DOI-based verification as the gold standard for author accuracy

2. **Author Information**
   - Maintain consistent author ID format in authors.yml
   - Verify author spelling and affiliations against DOI sources
   - Include proper website links when available
   - Mark the main author (is_me: true) correctly
   - **NEW**: When adding new authors, double-check spelling against official publication sources

3. **Data Verification Workflow**
   ```
   1. Extract data from primary source (CV/official websites)
   2. Cross-reference with secondary sources
   3. Find and verify DOI for each publication
   4. Add DOI to arxiv field in publications.yml
   5. Verify author lists and order against DOI source
   6. Confirm exact titles and venues
   7. Test links and project pages
   8. Commit changes
   ```

4. **Quality Assurance**
   - Read data back after updates to catch obvious errors
   - Test website functionality after major changes
   - Maintain chronological organization
   - Keep descriptions consistent in length and style
   - **NEW**: Verify all publications have DOI in arxiv field for future reference

### Technical Implementation Notes

- GitHub Pages deployment works reliably with push workflow
- Jekyll builds handle YAML data structure changes well
- Project page links from computationalimaging.org are reliable
- NVIDIA research page is the most authoritative source for recent work
- CV PDF contains the most comprehensive publication list
- **NEW**: DOI sources (journal publishers) provide most accurate author information
- **NEW**: WebFetch tool effectively retrieves publication metadata from publisher websites

### Today's Accomplishments (2024-08-20 Session)

1. **Complete Publication Database Verification**
   - Verified all 29 publications spanning 2024-2011
   - Added DOI information for every publication in arxiv field
   - Corrected multiple author errors including critical 2011 paper correction
   - Updated authors.yml with accurate author information

2. **Author Database Improvements**
   - Fixed critical author ID error: gunheepark → gilbaepark
   - Ensured all author names match exactly with official publication sources
   - Maintained author website links and affiliations

3. **Data Quality Assurance**
   - Implemented systematic DOI-based verification workflow
   - Cross-referenced author information with authoritative journal sources
   - Established reliable verification process for future updates

### Major UI/UX Overhaul (2025-01-04 Session)

1. **Highlights Section Evolution and Removal**
   - ✅ Initially added 2 new papers to highlights: "Real-time 3D Visualization of Radiance Fields" (arXiv 2024) and "AI-mediated 3D Video Conferencing" (2023)
   - ✅ Updated highlights layout from 3-column to 4-column grid (4 items per row, 2 rows total)
   - ✅ **FINAL DECISION**: Complete removal of highlights section for cleaner, publication-focused design
   - **Future Planning**: Consider adding demos/talks videos section in former highlights location

2. **New Publications Added**
   - ✅ "Real-time 3D Visualization of Radiance Fields on Light Field Displays" (arXiv:2508.18540, 2024)
     - Added to both publications.yml and highlights initially
     - Added missing authors: csun, arussell, jjung, wbraithwaite
   - ✅ "AI 3D Selfie: Real-time Single-Image 3D Face Reconstruction for Light Field Displays" (SID 2025, DOI:10.1002/sdtp.18377)
     - Extracted information from PDF document provided by user
     - Created image folder structure for both new papers

3. **Publication Display Simplification**
   - ✅ **Phase 1**: Removed arXiv and PDF buttons, kept only Project Page button
   - ✅ **Phase 2**: Removed all buttons completely for ultra-clean design
   - ✅ **Final Implementation**: Made both publication titles AND images clickable to project pages
   - ✅ Images open project pages in new tabs for better user experience

4. **Site Navigation Updates**
   - ✅ Updated GitHub link to https://github.com/jkim89
   - ✅ Removed Twitter button (acknowledged as outdated social platform)
   - ✅ Maintained CV, Google Scholar, and GitHub buttons only

5. **Technical Corrections Made**
   - ✅ Fixed dual-dimensional microscopy paper metadata:
     - Venue: Scientific Reports 2015 → Journal of Biomedical Optics 2018
     - Added proper DOI project page
     - Corrected author list and order
   - ✅ Fixed image file extension case sensitivity (capture.png → capture.PNG)

### Design Philosophy Decisions Made

1. **Minimalist Approach Adopted**
   - Removed highlights section entirely for focus on publications
   - Eliminated all publication action buttons
   - Simplified click interactions to title/image only
   - Maintained clean, academic professional appearance

2. **User Experience Improvements**
   - Publication images now clickable (major usability improvement)
   - Consistent new-tab opening behavior for external links
   - Reduced cognitive load with fewer buttons and cleaner layout
   - Preserved all functionality while simplifying interface

3. **Future Development Considerations**
   - Former highlights section space available for demos/talks videos
   - Site structure ready for multimedia content addition
   - Maintained flexible YAML data structure for easy content updates

### Common Pitfalls to Avoid

1. Don't assume author lists - always verify from primary sources
2. Don't copy-paste without cross-checking accuracy
3. Don't commit large data changes without reviewing output
4. Don't ignore venue vs conference vs journal distinctions
5. Don't skip verification of publication years and chronological order
6. **NEW**: Don't skip DOI verification - it's the most reliable source for author accuracy
7. **NEW**: Don't assume author spellings are correct without checking against official publications