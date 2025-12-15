# GitHub Copilot Instructions for MTS-Gaming Website

## Project Overview
This is a static website for MTS-Gaming, an elite gaming clan. The site is built using Eleventy (11ty) as a static site generator and requires **zero server-side rendering**. All code execution happens client-side.

## Technology Stack
- **Static Site Generator**: Eleventy (11ty)
- **Template Engine**: Nunjucks (.njk files)
- **Styling**: Pure CSS with gaming/cyberpunk aesthetics
- **JavaScript**: Vanilla JS for client-side interactions
- **Build Output**: Static HTML/CSS/JS files in `_site/` directory

## Design Philosophy
### Gaming Aesthetics
- **Theme**: Cyberpunk/Neon gaming aesthetic
- **Color Palette**:
  - Neon Cyan: `#00ffff`
  - Neon Magenta: `#ff00ff`
  - Neon Yellow: `#ffff00`
  - Neon Green: `#00ff00`
  - Dark Background: `#0a0a0a`
- **Effects**:
  - Glitch effects on text
  - Scanline overlay for CRT monitor feel
  - Neon glow and text shadows
  - Particle system background
  - Mouse-reactive animations

## Code Guidelines

### Static-Only Requirements
- **NO server-side code**: Everything must run in the browser
- **NO backend APIs**: All functionality is client-side
- **NO databases**: Use static data only
- **Build once, serve anywhere**: Output should be deployable to any static host

### File Structure
```
/
├── .eleventy.js          # Eleventy configuration
├── src/                  # Source files
│   ├── _layouts/         # Nunjucks layout templates
│   ├── css/              # Stylesheets
│   ├── js/               # Client-side JavaScript
│   ├── assets/           # Images, fonts, etc.
│   └── index.njk         # Main page
└── _site/                # Build output (gitignored)
```

### CSS Guidelines
- Use CSS custom properties (CSS variables) for theming
- Maintain gaming aesthetic with neon colors and glow effects
- Ensure responsive design for mobile devices
- Use animations and transitions for interactive elements
- Keep scanline and glitch effects for authenticity

### JavaScript Guidelines
- All JavaScript must be client-side only
- Use vanilla JavaScript (no frameworks required for core functionality)
- Implement particle systems for animated backgrounds
- Make background reactive to mouse position
- Support both mouse and touch events for mobile
- Keep performance in mind (60fps target)

### Content Guidelines
- Use gaming terminology and lingo (GG, WP, 1337, etc.)
- Maintain an energetic, competitive tone
- Include sections for:
  - Welcome/Hero section
  - Links to social media and platforms
  - Statistics/achievements
  - Any other gaming-relevant content

### Build Commands
- `npm run build` - Build static site to `_site/`
- `npm run start` - Start development server with live reload

### Adding New Pages
1. Create a `.njk` file in `src/`
2. Add front matter with layout reference
3. Use the base layout for consistent styling
4. Eleventy will automatically generate the static HTML

### Modifying Styles
- Primary styles are in `src/css/style.css`
- Maintain neon color scheme and gaming aesthetic
- Keep dark theme as base
- Ensure all hover effects work smoothly

### Background Animation
- Particle system implemented in `src/js/background.js`
- Particles are attracted to mouse cursor
- Connections drawn between nearby particles
- Radial glow follows mouse position
- Adjustable particle count for performance

## Testing
- Build the site: `npm run build`
- Test locally: `npm run start`
- Verify all links work
- Check responsive design on mobile sizes
- Ensure animations run smoothly

## Deployment
The `_site/` directory contains the complete static website and can be deployed to:
- GitHub Pages
- Netlify
- Vercel
- Any static hosting service

Simply copy the contents of `_site/` to your hosting provider.

## Important Notes
- Never add server-side code or API routes
- Keep all assets in the static paths (css/, js/, assets/)
- Test builds before committing
- Maintain the gaming aesthetic in all changes
- Optimize images before adding to assets/
