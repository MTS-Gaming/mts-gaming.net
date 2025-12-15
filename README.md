# MTS-Gaming Website

The official website for MTS-Gaming - an elite gaming clan featuring cyberpunk aesthetics and mouse-reactive animations.

## About

This is a fully static website built with [Eleventy (11ty)](https://www.11ty.dev/) featuring:

- 🎮 **Gaming Aesthetics**: Cyberpunk/neon theme with cyan, magenta, yellow, and green color palette
- ✨ **Animated Background**: Particle system with 100+ particles that react to mouse movement
- 🖱️ **Interactive Effects**: Particles attracted to cursor, dynamic connections, and radial glow
- 📱 **Fully Responsive**: Mobile-friendly design with touch support
- ⚡ **Client-Side Only**: Zero server-side rendering - all code runs in the browser
- 🎨 **Visual Effects**: Glitch effects, CRT scanlines, neon glow, and smooth hover transitions

## Local Development

### Prerequisites

- Node.js (v18 or higher)
- npm

### Getting Started

1. **Clone the repository**
   ```bash
   git clone https://github.com/MTS-Gaming/mts-gaming.net.git
   cd mts-gaming.net
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Start the development server**
   ```bash
   npm run start
   ```
   This will start a local server at `http://localhost:8080` with live reload enabled.

4. **Build for production**
   ```bash
   npm run build
   ```
   This generates static files in the `_site/` directory.

### Available Commands

- `npm run start` - Start development server with live reload
- `npm run build` - Build static site to `_site/` directory

## Project Structure

```
/
├── .eleventy.js              # Eleventy configuration
├── src/                      # Source files
│   ├── _layouts/             # Page templates
│   │   └── base.njk          # Base layout with canvas and effects
│   ├── css/                  # Stylesheets
│   │   └── style.css         # Main styles with gaming theme
│   ├── js/                   # Client-side JavaScript
│   │   └── background.js     # Particle system and animations
│   ├── assets/               # Static assets (images, fonts)
│   └── index.njk             # Homepage
└── _site/                    # Build output (gitignored)
```

## Features

### Particle Background
- Canvas-based particle system with 100 particles
- Particles attracted to mouse/touch position
- Dynamic connections between nearby particles
- Radial glow effect following the cursor

### Design Elements
- Neon color scheme with glow effects
- Glitch animation on the logo
- CRT scanline overlay
- Hover effects with color transitions
- Stats display (victories, members, online status)
- Link cards for social platforms (Discord, Twitch, YouTube, Twitter, Instagram, Tournaments)

## Deployment

The `_site/` directory contains the complete static website and can be deployed to:
- GitHub Pages
- Netlify
- Vercel
- Any static hosting service

Simply copy the contents of `_site/` to your hosting provider after running `npm run build`.

## Contributing

This is a clan website. For development guidelines and architecture details, see `.github/copilot-instructions.md`.

## License

© 2024 MTS-Gaming. All rights reserved. GG WP.
