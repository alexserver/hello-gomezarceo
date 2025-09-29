# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a static landing page for Alejandro Gómez's fractional CTO consultancy services, built with Astro and styled with TailwindCSS. The site presents a professional, Silicon Valley startup-themed design to attract non-technical founders who need help bringing their tech ideas to life.

## Development Commands

```bash
# Start development server (localhost:4321)
npm run dev

# Build for production
npm run build

# Preview production build locally
npm run preview

# Run Astro CLI commands
npm run astro [command]
```

## Architecture

### Tech Stack
- **Astro 5.14.1**: Static site generator with minimal JavaScript
- **TailwindCSS 4.1.13**: Utility-first CSS framework via Vite plugin
- **TypeScript**: Strict configuration extending Astro's defaults

### Project Structure
```
src/
├── pages/
│   └── index.astro          # Main landing page
└── styles/
    └── global.css           # TailwindCSS imports

specs/
└── homepage.md              # Content specifications and copy

astro.config.mjs             # Astro + TailwindCSS Vite plugin config
```

### Landing Page Architecture
The main page (`src/pages/index.astro`) is a single-page layout with these sections:

1. **Hero Section**: Main headline with gradient text effect and primary CTA
2. **Pain Point Section**: Addresses technical overwhelm for founders
3. **Tech Co-pilot Section**: 4-card grid explaining services
4. **Credentials Section**: Experience and tech stack highlights
5. **Process Section**: 4-step numbered workflow
6. **Reassurance Section**: Non-technical friendly messaging
7. **Final CTA Section**: Strong call-to-action with booking link
8. **Footer**: Bio and contact information

### Design System
- **Color Scheme**: Dark gradients (slate-900, purple-900, blue-600)
- **Typography**: Large, bold headings with gradient text effects
- **Layout**: Responsive design with max-width containers
- **Interactive Elements**: Hover effects, scaling animations, gradient buttons
- **Spacing**: Generous padding (py-20) between sections

## Content Management

All copy and content specifications are maintained in `specs/homepage.md`. This file contains:
- Section-by-section copy
- Headlines and sub-headlines
- CTA button text
- Contact information
- Bio content

When updating content, modify both the spec file and the corresponding Astro page sections to maintain consistency.

## TailwindCSS Integration

TailwindCSS is integrated via the Vite plugin (`@tailwindcss/vite`) in `astro.config.mjs`. The global stylesheet is imported directly in the index.astro file. The project uses TailwindCSS v4 syntax with modern features like arbitrary value support and improved performance.