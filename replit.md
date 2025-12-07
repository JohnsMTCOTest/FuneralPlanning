# Thoughtful Choice

## Overview

A single-page, static website that provides a comprehensive, accessible guide for end-of-life planning. The application walks users through ceremony options, disposition methods, memorialization ideas, and includes practical guidance and checklists. Built as a simple HTML/CSS project with no build tools or backend dependencies, optimized for clarity and ease of reading.

**Purpose**: Help individuals make informed, meaningful decisions about their final arrangements by presenting options in plain, compassionate language.

## User Preferences

Preferred communication style: Simple, everyday language.

## System Architecture

### Frontend Architecture

**Technology Stack**:
- Pure HTML5 (semantic markup)
- CSS3 (custom properties for theming)
- Google Fonts (Inter for body, Playfair Display for headings)

**Design Patterns**:
- **Single-page application**: All content lives in `index.html` with anchor-based navigation
- **Component-based CSS**: Reusable classes (`.section-card`, `.option`, `.grid-two`) for consistent layout patterns
- **CSS Custom Properties**: Centralized theming via `:root` variables for colors, spacing, and shadows
- **Mobile-first responsive**: Grid and flexbox layouts that adapt to viewport size
- **Sticky navigation**: Fixed header with smooth scroll behavior for section navigation

**Key Architectural Decisions**:
- **No JavaScript**: Eliminates complexity and dependencies; relies on CSS and HTML features for interactivity (smooth scroll, focus states)
- **Inline content**: All text embedded directly in HTML for easy customization without templating systems
- **Gradient-only hero**: Ships without binary image assets to keep the project lightweight and portable

**Accessibility Considerations**:
- Semantic HTML5 elements (`<header>`, `<nav>`, `<main>`, `<section>`, `<article>`)
- ARIA labels for navigation
- Keyboard-friendly focus states with visible outlines
- Readable contrast ratios and scalable typography

### File Structure

```
/
├── index.html           # Single-page application with all content
├── assets/
│   └── styles.css      # Complete styling and layout system
└── README.md           # Documentation and customization guide
```

**Content Organization** (within `index.html`):
1. Hero section with call-to-action
2. Ceremony options (home funeral, funeral service, memorial, graveside, burial at sea)
3. Disposition methods (traditional burial, green burial, cremation, aquamation, natural organic reduction)
4. Memorialization ideas (merchandise and service-based options)
5. Guidance section (decision-making framework)
6. Checklist (verification questions)

### Styling Architecture

**CSS Organization**:
- **Root variables**: Color palette, typography scale, spacing units
- **Reset/base styles**: Box-sizing, scroll behavior, body defaults
- **Component classes**: Modular, reusable patterns (cards, grids, buttons)
- **Layout utilities**: Flexbox/grid containers for responsive behavior
- **State styles**: Focus, hover, and active states

**Key CSS Features**:
- Sticky header with backdrop blur effect
- Box shadows for depth and visual hierarchy
- Responsive grid system (`.grid-two` adapts to single column on mobile)
- Custom font loading from Google Fonts CDN

### Customization Points

The application is designed for easy customization:
- **Visual theming**: Modify CSS custom properties in `:root`
- **Content adaptation**: Edit HTML text for regional/cultural variations
- **Hero image**: Add background image to `.hero` class
- **Typography**: Swap font imports in `<head>` and update CSS font-family

## External Dependencies

### Third-Party Services

**Google Fonts API**:
- **Purpose**: Typography (Inter for UI, Playfair Display for headings)
- **Integration**: CDN links with preconnect optimization
- **Fonts loaded**: 
  - Inter: weights 400, 500, 600, 700
  - Playfair Display: weights 600, 700
- **Fallbacks**: System fonts (Segoe UI, system-ui, -apple-system) if CDN fails

### Browser Requirements

- Modern browser with CSS Grid and Custom Properties support
- HTML5 semantic element support
- No JavaScript required (progressive enhancement approach)

### No Backend Infrastructure

- **Static hosting**: Can be served from any web server or CDN
- **No database**: All content is static HTML
- **No authentication**: Public-facing informational site
- **No APIs**: No dynamic data fetching or form submissions