# Nathan Culley - Personal Website

Modern, minimal landing page serving as a social media hub and gateway to nathanculley.com.

## Overview

A clean, typography-focused single-page website featuring:
- Hero section with bio
- Social media links (Substack blog, Twitter, Instagram, GitHub)
- Responsive design with dark mode support
- Optimized for performance and accessibility

## Tech Stack

- **React 18** - UI framework
- **Vite 6** - Build tool and dev server
- **Modern CSS** - Custom properties, responsive design, dark mode
- **GitHub Actions** - Automated deployment

## Local Development

### Prerequisites

- Node.js 18 or higher
- npm or yarn

### Setup

1. Clone the repository:
```bash
git clone https://github.com/nathan-culley/personal-website.git
cd personal-website
```

2. Install dependencies:
```bash
npm install
```

3. Start development server:
```bash
npm run dev
```

The site will be available at `http://localhost:5173`

### Available Scripts

- `npm run dev` - Start development server with hot reload
- `npm run build` - Build for production
- `npm run preview` - Preview production build locally

## Deployment

### GitHub Pages Deployment

The site is configured for automatic deployment to GitHub Pages via GitHub Actions.

#### Initial Setup

1. **Enable GitHub Pages:**
   - Go to repository Settings > Pages
   - Source: Select "GitHub Actions"
   - Save settings

2. **Push to main branch:**
```bash
git add .
git commit -m "Initial commit"
git push origin main
```

The GitHub Actions workflow will automatically build and deploy the site.

#### Deployment Workflow

Every push to the `main` branch triggers:
1. Build process (npm install, npm build)
2. Upload build artifacts
3. Deploy to GitHub Pages

The workflow file is located at `.github/workflows/deploy.yml`

### Custom Domain Setup (nathanculley.com)

#### Option 1: GitHub Pages with Custom Domain

1. **Configure DNS at your domain registrar:**

   Add the following DNS records:

   **For Apex Domain (nathanculley.com):**
   ```
   Type: A
   Name: @
   Value: 185.199.108.153

   Type: A
   Name: @
   Value: 185.199.109.153

   Type: A
   Name: @
   Value: 185.199.110.153

   Type: A
   Name: @
   Value: 185.199.111.153
   ```

   **For www subdomain:**
   ```
   Type: CNAME
   Name: www
   Value: nathan-culley.github.io
   ```

2. **Configure GitHub Pages custom domain:**
   - Go to repository Settings > Pages
   - Under "Custom domain", enter: `nathanculley.com`
   - Check "Enforce HTTPS" (after DNS propagation)
   - Create a file named `CNAME` in the `/public` directory containing:
     ```
     nathanculley.com
     ```

3. **Wait for DNS propagation:**
   - Can take 24-48 hours
   - Test with: `dig nathanculley.com` or `nslookup nathanculley.com`

#### Option 2: Alternative Hosting (Vercel, Netlify, etc.)

If you prefer other hosting platforms:

**Vercel:**
1. Import repository to Vercel
2. Build command: `npm run build`
3. Output directory: `dist`
4. Add custom domain in Vercel dashboard

**Netlify:**
1. Import repository to Netlify
2. Build command: `npm run build`
3. Publish directory: `dist`
4. Add custom domain in Netlify dashboard

### Substack Subdomain Setup (blog.nathanculley.com)

For your Substack blog to appear at `blog.nathanculley.com`:

1. **In your domain registrar's DNS settings:**
   ```
   Type: CNAME
   Name: blog
   Value: <your-substack-subdomain>.substack.com
   ```
   Replace `<your-substack-subdomain>` with your actual Substack subdomain.

2. **In Substack settings:**
   - Go to Settings > Domain
   - Enter: `blog.nathanculley.com`
   - Follow Substack's verification process

3. **Wait for DNS propagation** (typically 1-24 hours)

## Project Structure

```
personal-website/
├── .github/
│   └── workflows/
│       └── deploy.yml        # GitHub Actions deployment
├── public/
│   └── favicon.svg           # Site favicon
├── src/
│   ├── App.css              # Component styles
│   ├── App.jsx              # Main application component
│   ├── index.css            # Global styles and CSS reset
│   └── main.jsx             # React entry point
├── index.html               # HTML entry point with meta tags
├── vite.config.js           # Vite configuration
├── package.json             # Dependencies and scripts
└── README.md               # This file
```

## Customization

### Updating Social Links

Edit the `socialLinks` array in `src/App.jsx`:

```jsx
const socialLinks = [
  {
    name: 'Blog',
    href: 'https://blog.nathanculley.com',
    icon: SubstackIcon,
    description: 'Read my writing on Substack',
    primary: true
  },
  // Add or modify links here
]
```

### Changing Colors

Edit CSS custom properties in `src/index.css`:

```css
:root {
  --color-accent: #2563eb;
  --color-bg: #fafafa;
  /* etc. */
}
```

Dark mode colors are defined in the `@media (prefers-color-scheme: dark)` block.

### Typography

The site uses the Inter font family from Google Fonts. To change:

1. Update the font import in `index.html`
2. Update `--font-family` in `src/index.css`

## Features

- **Responsive Design:** Mobile-first approach, works on all screen sizes
- **Dark Mode:** Automatically respects system preferences
- **Accessibility:** ARIA labels, keyboard navigation, focus states
- **Performance:** Minimal dependencies, optimized builds
- **SEO:** Meta tags, Open Graph, Twitter Card support
- **Icons:** Inline SVG icons for performance (no icon library needed)

## Browser Support

- Chrome/Edge (last 2 versions)
- Firefox (last 2 versions)
- Safari (last 2 versions)
- Mobile browsers (iOS Safari, Chrome Android)

## License

Copyright © 2026 Nathan Culley. All rights reserved.

## Contact

- Website: [nathanculley.com](https://nathanculley.com)
- Blog: [blog.nathanculley.com](https://blog.nathanculley.com)
- Twitter: [@nathan_culley](https://twitter.com/nathan_culley)
- GitHub: [@nathan-culley](https://github.com/nathan-culley)

---

Built with React and Vite. Deployed via GitHub Pages.
