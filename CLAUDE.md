# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Static HTML website ranking SEO companies in Encinitas, California. No build tools, frameworks, or package managers - just pure HTML/CSS files that can be served directly.

## Project Structure

**Main Content Pages:**
- `index.html` - Main ranking page listing top 10 SEO companies with Schema.org ItemList markup
- `encinitas-seo-guide.html` - Comprehensive 10-section SEO educational guide with Article schema

**EEAT (Trust & Authority) Pages:**
- `about.html` - Company story, team overview, editorial independence statement
- `authors.html` - Detailed author profiles with credentials and expertise
- `methodology.html` - Ranking criteria, research process, data sources
- `contact.html` - Contact form, business info, FAQs

**Legal Pages:**
- `privacy.html` - Privacy policy with CCPA compliance
- `terms.html` - Terms of service with affiliate disclosure

## Development

No build step required. Open HTML files directly in a browser or serve with any static file server.

## Design System

All styles are embedded in `<style>` tags within each HTML file using CSS custom properties:

```css
--deep-navy: #0a1628      /* Primary dark background */
--warm-gold: #c9a227      /* Accent/highlight */
--soft-cream: #faf8f5     /* Page background */
--muted-sage: #8b9a7d     /* Secondary accent */
--rich-burgundy: #722f37  /* Warning/badge */
```

Typography uses Google Fonts: Playfair Display (headings) and Source Sans 3 (body).

## Key Patterns

- **Responsive breakpoint**: 900px for mobile/desktop layouts
- **Schema.org structured data**: Organization (sitewide), ItemList (rankings), Article (guide), Person (authors)
- **Accessibility**: Uses `.sr-only` class for screen reader text, ARIA labels throughout
- **EEAT signals**: Author bylines, publication dates, expert review badges, editorial disclosures

## Navigation Structure

Header nav (all pages): Rankings | SEO Guide | About | Contact

Footer links (all pages):
- Resources: SEO Company Rankings, Encinitas SEO Guide, Our Methodology
- Company: About Us, Our Authors, Contact, Privacy Policy, Terms of Service

## When Making Changes

- Maintain consistent header/footer across all pages
- Update navigation links in all files when adding new pages
- Preserve Schema.org structured data when modifying content
- Include author attribution on content pages
- Keep responsive behavior - use CSS clamp() for fluid typography
