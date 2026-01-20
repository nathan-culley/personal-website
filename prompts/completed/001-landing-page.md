<objective>
Build a modern, minimal landing page for nathanculley.com that serves as a social media hub and gateway to Nathan's Substack blog. This is a professional landing page for a firefighter-paramedic who writes and creates content across multiple platforms.
</objective>

<context>
This website will be the central landing page for Nathan Culley, linking to his various online presences:
- Substack blog (to be hosted at blog.nathanculley.com)
- Twitter: @nathan_culley
- Personal Instagram: @_nathanculley_
- Photography Instagram: @aion_imagery
- GitHub: https://github.com/nathan-culley

The current domain (nathanculley.com) is owned by Nathan and currently runs through WordPress.com. This new site needs to be deployable to either replace the WordPress site or be hosted on GitHub Pages.

Design preference: Minimal/clean with typography focus, lots of whitespace, subtle interactions.

Tech stack: React + Vite for modern development experience with fast builds.
</context>

<requirements>
1. **Hero Section**:
   - Brief bio/tagline about Nathan (firefighter-paramedic, writer, content creator)
   - Professional but approachable tone
   - Clean typography with good hierarchy

2. **Social Links Section**:
   - Prominent link to Substack (blog.nathanculley.com subdomain)
   - Links to Twitter, Instagram (personal), Instagram (photography), GitHub
   - Use recognizable icons for each platform
   - Hover states with subtle animations

3. **Design Requirements**:
   - Fully responsive (mobile-first approach)
   - Minimal/clean aesthetic
   - Typography-focused with excellent readability
   - Generous whitespace
   - Subtle interactions (hover effects, smooth transitions)
   - Professional color scheme (consider muted/neutral palette)

4. **Technical Requirements**:
   - React + Vite setup
   - Clean, semantic HTML
   - Modern CSS (CSS modules, styled-components, or Tailwind - choose what fits best)
   - Optimized for performance (fast load times)
   - SEO-friendly (proper meta tags, Open Graph tags)
   - Accessibility considerations (ARIA labels, keyboard navigation)

5. **Deployment Preparation**:
   - Include build configuration for GitHub Pages
   - Add instructions for custom domain setup (nathanculley.com)
   - Document Substack subdomain setup requirements
</requirements>

<implementation>
1. Initialize a React + Vite project with appropriate configuration
2. Create a simple, elegant single-page layout
3. Implement responsive design that works beautifully on all screen sizes
4. Use icon library for social media icons (React Icons, Lucide React, or similar)
5. Add smooth transitions and hover effects for interactivity
6. Ensure excellent typography (consider using a web font like Inter, Lato, or similar)
7. Include meta tags for SEO and social sharing
8. Set up build process for deployment

**What to avoid and WHY**:
- Avoid complex animations or heavy JavaScript since this is a simple landing page and should load instantly
- Avoid cluttered layouts since the goal is a minimal, focused design that directs visitors to specific platforms
- Avoid excessive dependencies since this keeps the site lightweight and maintainable
</implementation>

<output>
Create the following files:
- `./package.json` - Dependencies and scripts
- `./vite.config.js` - Vite configuration with GitHub Pages setup
- `./index.html` - Entry HTML file with meta tags
- `./src/main.jsx` - React entry point
- `./src/App.jsx` - Main application component
- `./src/index.css` - Global styles and CSS reset
- `./src/components/` - Component directory (if breaking into components)
- `./public/` - Static assets (favicon, etc.)
- `./README.md` - Update with setup and deployment instructions
- `./.github/workflows/deploy.yml` - GitHub Actions workflow for automatic deployment (if using GitHub Pages)
</output>

<verification>
Before declaring complete, verify:
1. Run `npm install` successfully
2. Run `npm run dev` and view the site at localhost
3. Test responsive design at multiple breakpoints (mobile, tablet, desktop)
4. Verify all social links are correct and open in new tabs
5. Check that hover states work smoothly
6. Verify SEO meta tags are present in the HTML
7. Run `npm run build` to ensure production build works
8. Test keyboard navigation through all interactive elements
</verification>

<success_criteria>
- Clean, modern landing page loads quickly
- All social media links work correctly
- Site is fully responsive and looks great on all devices
- Minimal design aesthetic is achieved
- Code is well-organized and documented
- Build process is configured for GitHub Pages deployment
- Instructions for custom domain setup are included
- Site meets accessibility standards (keyboard navigable, proper ARIA labels)
</success_criteria>
