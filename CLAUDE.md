# Personal Website - Claude Code Configuration

## Project Overview
Modern, minimal landing page for nathanculley.com serving as a social media hub and gateway to Nathan's Substack blog.

## Tech Stack
- **React 18** - UI framework
- **Vite 6** - Build tool and dev server
- **Modern CSS** - Custom properties, responsive design, dark mode support
- **GitHub Actions** - Automated deployment to GitHub Pages

## Project Structure

```
personal-website/
├── .github/workflows/     # GitHub Actions deployment
├── public/               # Static assets (favicon)
├── src/                  # Source code
│   ├── App.css          # Component styles
│   ├── App.jsx          # Main application component
│   ├── index.css        # Global styles, CSS reset, design tokens
│   └── main.jsx         # React entry point
├── index.html           # HTML entry with SEO meta tags
├── vite.config.js       # Vite configuration
└── package.json         # Dependencies and scripts
```

## Development Guidelines

### Code Style
- Use functional components with hooks (no class components)
- Keep components simple and focused
- Use semantic HTML elements
- Follow accessibility best practices (ARIA labels, keyboard navigation)
- Prefer inline SVG icons over icon libraries for performance

### CSS Approach
- CSS custom properties for theming and design tokens
- Mobile-first responsive design
- Dark mode via `prefers-color-scheme` media query
- Respect user motion preferences (`prefers-reduced-motion`)
- Use BEM-like naming for clarity

### Performance Considerations
- Minimal dependencies (React + Vite only)
- Inline SVG icons (no icon library)
- Optimized fonts (Inter from Google Fonts with preconnect)
- Fast build times with Vite
- Lazy loading not needed (single page, minimal content)

### Accessibility Requirements
- Proper semantic HTML structure
- ARIA labels on all interactive elements
- Focus-visible states for keyboard navigation
- Sufficient color contrast (check with tools)
- Respect user preferences (dark mode, reduced motion, high contrast)

## Design System

### Colors
- Light mode: Neutral grays with blue accent (#2563eb)
- Dark mode: Dark background with lighter text, brighter accent
- Automatically switches based on system preference

### Typography
- Font: Inter (Google Fonts)
- Scale: Responsive with clamp() for fluid typography
- Weights: 300 (light), 400 (regular), 500 (medium), 600 (semibold)

### Spacing
- Based on rem units
- Scale: xs (0.5rem) to 3xl (6rem)
- Consistent gaps and padding throughout

### Animations
- Subtle transitions (150-250ms)
- Hover effects on social links
- Disabled for users who prefer reduced motion

## Development Commands

- `npm install` - Install dependencies
- `npm run dev` - Start dev server (localhost:5173)
- `npm run build` - Build for production
- `npm run preview` - Preview production build locally

## Deployment

### GitHub Pages (Primary Method)
- Automatic deployment via GitHub Actions on push to main
- Workflow: `.github/workflows/deploy.yml`
- Build artifacts uploaded to GitHub Pages

### Custom Domain Setup
Domain: nathanculley.com
- Configure A records pointing to GitHub Pages IPs
- Add CNAME file in /public directory
- Enable in GitHub repository settings

Substack subdomain: blog.nathanculley.com
- CNAME record pointing to Substack
- Configure in Substack settings

## Customization Points

### Social Links
Edit `socialLinks` array in `/src/App.jsx`:
- name: Display name
- href: URL
- icon: SVG component
- description: Subtitle text
- primary: boolean (for prominent styling)

### Colors
Edit CSS custom properties in `/src/index.css`:
- Light mode colors in `:root`
- Dark mode colors in `@media (prefers-color-scheme: dark)`

### Typography
Change font in two places:
1. Font import in `/index.html` (Google Fonts)
2. `--font-family` variable in `/src/index.css`

## Content Guidelines

### Hero Section
- Keep bio concise (1-2 sentences)
- Professional but approachable tone
- Highlight key identities (firefighter-paramedic, writer, creator)

### Social Links
- Substack blog is primary call-to-action
- Other platforms in priority order
- Clear, descriptive link text
- Icons enhance recognition

## Testing Checklist

Before deploying changes:
- [ ] Test responsive design (mobile, tablet, desktop)
- [ ] Verify all social links work and open in new tabs
- [ ] Check dark mode appearance
- [ ] Test keyboard navigation (tab through all links)
- [ ] Verify hover states work smoothly
- [ ] Check reduced motion preference handling
- [ ] Run build successfully
- [ ] Preview production build locally

## Future Enhancements (Optional)

Potential additions if needed:
- Blog post previews from Substack RSS
- Newsletter signup form
- Analytics integration (Plausible, Fathom)
- Open Graph image for social sharing
- Micro-interactions and animations
- Contact form

Keep in mind: The goal is simplicity. Only add features if they serve a clear purpose.

## Reference Material
- React docs: https://react.dev
- Vite docs: https://vite.dev
- GitHub Pages docs: https://docs.github.com/pages
- MDN Web Docs: https://developer.mozilla.org
