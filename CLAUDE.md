# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is the official website for Fairway Hills Association, a 79-unit condominium community in Lake City, Florida. The site is a static GitHub Pages website hosted at fairwayhillscondo.com that provides public access to governing documents as required by Florida law.

## Architecture

**Static Single-Page Website:**
- Single HTML file (`index.html`) with embedded CSS
- No build process, JavaScript framework, or external dependencies
- Pure HTML/CSS with inline styles
- Hosted via GitHub Pages with custom domain (CNAME file)

**Content Structure:**
- Hero section with community welcome
- Photo gallery showcasing community features
- Amenities section
- Board of Directors roster (updated annually)
- Official documents section with PDF links
- Contact information footer

**Asset Organization:**
- `/documents/` - PDF files for legal documents, bylaws, rules, floor plans, annual reports
- `/images/` - Community photos in .webp and .jpg formats
- `CNAME` - Custom domain configuration for GitHub Pages

## Development Workflow

**Making Content Updates:**
Since this is a static site, edit `index.html` directly:
- Board member updates: Lines 329-356
- Amenity information: Lines 315-326
- Document links: Lines 362-416
- Contact information: Lines 419-426

**Adding New Documents:**
1. Place PDF in `/documents/` directory
2. Add corresponding document card in the "Official Documents & Compliance" section
3. Follow the existing pattern with document-card div structure

**Deployment:**
- Changes pushed to the `main` branch are automatically deployed via GitHub Pages
- No build or deployment commands needed
- Site typically updates within 1-2 minutes of push

**Testing Changes:**
Open `index.html` directly in a browser to preview changes locally before committing.

## Design System

**Color Palette:**
- Primary green: `#2d5016` (dark forest green)
- Secondary green: `#4a7c2b` (medium green)
- Light green background: `#e8f5e9`
- Gradient backgrounds used throughout for visual interest

**Layout Approach:**
- CSS Grid for responsive layouts (document cards, board members, photo gallery)
- Mobile-first responsive design with breakpoint at 768px
- System font stack for fast loading and native appearance

**Interactive Elements:**
- Hover effects on document cards and photos
- Transform and box-shadow transitions for depth
- Google Maps link for address

## Key Considerations

**Legal Compliance:**
This site exists primarily to fulfill Florida statutory requirements for HOA/condominium associations to provide public access to governing documents. The document section must always remain accessible and up-to-date.

**Annual Updates Required:**
- Board of Directors roster (typically in January)
- Annual Report document link
- Pool season dates if they change

**Accessibility:**
- Semantic HTML structure
- Alt text on images
- Adequate color contrast
- Clickable areas with clear hover states

**Performance:**
- Uses .webp images for photos (smaller file size)
- Inline CSS eliminates additional HTTP requests
- No external dependencies or JavaScript means instant page loads
