# PRD: Paul's Personal Site v2.0

## Executive Summary
Redesigned personal landing page with improved visual hierarchy. Adds a developer character illustration on the left, reorganizes toolbar with GitHub link and vertical theme toggle on the right.

---

## 1. Product Overview

### Vision
Get visitors to book a 15-minute call with Paul in under 10 seconds. No friction, no distractions. **v2.0 adds personality with a developer character.**

### Target Audience
- Potential clients/collaborators
- Recruiters
- Developers interested in Paul's work
- Anyone landing on the domain

### Success Metrics
- **Conversion Rate**: % of visitors who click "Book a Call"
- **Time to CTA**: Average time before clicking button
- **Mobile vs Desktop**: Conversion split
- **Theme Preference**: Dark vs light usage
- **Page Load Time**: < 1s (Lighthouse score > 90)
- **Character Recognition**: Does the developer illustration increase engagement?

---

## 2. Core Features

### 2.1 Hero Section
- **Full viewport height** on desktop, responsive on mobile
- **Left side**: Developer character illustration (SVG)
  - Simple, friendly, approachable
  - Thinking/coding pose
  - Scales responsively
  - Subtle animation on load (optional)
  
- **Right side**: 
  - **Centered name** ("Paul Vudmaska") — large, bold, gradient text
  - **Taglines**:
    - "Available for hire"
    - "Rails · Astro · 17+ years shipping code"
  - **Bio quote**: "Question Everything"
  - **Primary CTA**: "Book a Call" button (links to cal.com/paul-vudmaska/15min)

### 2.2 Navigation Bar (Fixed Top)
- **Left**: Developer character illustration (smaller version, matches hero)
- **Right**: 
  - GitHub icon/link (links to github.com/voodoo)
  - **Theme toggle** — Vertical radio button:
    - Moon icon (dark mode)
    - Sun icon (light mode)
    - Selected state highlighted
    - Smooth transition between themes

### 2.3 Theme System
- **Dark Theme**:
  - Background: `#0a1628` (dark blue)
  - Text: `#f5f5f0` (off-white)
  - Accent: `#d4af37` (gold)
  - Button: Gold background, dark text
  - Developer illustration: Light colors
  
- **Light Theme**:
  - Background: `#f5f5f0` (off-white)
  - Text: `#2d2d2d` (dark gray)
  - Accent: `#4a5568` (slate)
  - Button: Dark background, light text
  - Developer illustration: Dark colors

- **Default**: System preference (respects `prefers-color-scheme`)
- **Persistence**: Saved to localStorage
- **Toggle**: Vertical radio button (moon/sun) — top right of toolbar

### 2.4 Design Principles
- **Minimal**: No nav menu, no footer, no clutter
- **Personality**: Developer character adds warmth
- **Fast**: Static HTML, no JavaScript frameworks
- **Responsive**: Mobile-first, works on all screen sizes
- **Accessible**: ARIA labels, semantic HTML, keyboard navigation
- **Modern**: Clean typography, subtle gradients, smooth transitions

---

## 3. Technical Specifications

### 3.1 Tech Stack
- **Framework**: Astro (static site generator)
- **Output**: Static HTML/CSS/JS
- **Styling**: Scoped CSS (no external dependencies)
- **Deployment**: GitHub Pages / Vercel (configured)
- **Build**: `npm run build` → `./dist/`

### 3.2 Developer Illustration
- **Format**: SVG (inline in HTML)
- **Size**: 
  - Hero: ~300-400px (responsive)
  - Toolbar: ~40-50px
- **Style**: Simple, friendly, approachable
- **Animation**: Optional subtle animation on load
- **Accessibility**: `<title>` and `<desc>` tags for screen readers

### 3.3 Theme Toggle
- **Type**: Vertical radio button group
- **Options**: 
  - Moon icon (dark mode)
  - Sun icon (light mode)
- **Interaction**:
  - Click to toggle
  - Keyboard: Arrow keys (up/down) to switch
  - Selected state: Highlighted/underlined
- **Styling**: 
  - Unselected: Muted color
  - Selected: Accent color (gold in dark, slate in light)
  - Smooth transition (0.3s)

### 3.4 Performance Requirements
- **Lighthouse Score**: > 90 (Performance, Accessibility, Best Practices, SEO)
- **Page Load Time**: < 1 second (3G)
- **Bundle Size**: < 50KB (gzipped)
- **First Contentful Paint (FCP)**: < 1s
- **Largest Contentful Paint (LCP)**: < 2.5s
- **SVG Illustration**: < 10KB (optimized)

### 3.5 Browser Support
- Modern browsers (Chrome, Firefox, Safari, Edge)
- Mobile browsers (iOS Safari, Chrome Mobile)
- Fallback for no-JS (button still works)

### 3.6 SEO
- **Meta Title**: "Paul Vudmaska"
- **Meta Description**: "Paul Vudmaska - Book a call"
- **Open Graph**: (optional v2.1)
  - og:title, og:description, og:image
  - og:url, og:type
- **Favicon**: SVG favicon included

---

## 4. User Flows

### 4.1 Primary Flow: Book a Call
1. User lands on site
2. Sees developer character + Paul's name + taglines
3. Clicks "Book a Call" button
4. Redirected to cal.com booking page
5. Books 15-minute call

### 4.2 Secondary Flow: Learn More
1. User lands on site
2. Clicks GitHub icon (top right)
3. Redirected to Paul's GitHub profile
4. Explores projects/code

### 4.3 Theme Toggle
1. User clicks moon or sun icon (top right)
2. Theme switches (dark ↔ light)
3. Preference saved to localStorage
4. Persists across sessions
5. Developer illustration colors adjust

---

## 5. Content

### 5.1 Copy
- **Name**: "Paul Vudmaska"
- **Tagline 1**: "Available for hire"
- **Tagline 2**: "Rails · Astro · 17+ years shipping code"
- **Bio**: "Question Everything"
- **Button Text**: "Book a Call"

### 5.2 Links
- **CTA Button**: https://cal.com/paul-vudmaska/15min
- **GitHub**: https://github.com/voodoo
- **Favicon**: `/favicon.svg`

### 5.3 Developer Illustration
- **Description**: Simple, friendly developer character
- **Pose**: Thinking/coding (TBD based on design)
- **Style**: Minimalist, matches site aesthetic
- **Colors**: Adapt to theme (light in dark mode, dark in light mode)

---

## 6. Layout Changes (v1.0 → v2.0)

### Toolbar (Before)
```
[GitHub Icon] ........................... [Theme Toggle] [Book a Call Button]
```

### Toolbar (After)
```
[Developer Illustration] ........................... [GitHub Icon] [Theme Toggle]
```

### Hero Section (Before)
```
[Centered Name + Taglines + Button]
```

### Hero Section (After)
```
[Developer Illustration] | [Name + Taglines + Button]
```

---

## 7. Deployment

### 7.1 Current Setup
- **Vercel**: Configured (`.vercel/` directory present)
- **Netlify**: Configured (`.netlify/` directory present)
- **GitHub Pages**: Ready (static output)

### 7.2 Build & Deploy
```bash
npm install
npm run build
# Output: ./dist/
# Deploy to Vercel/Netlify/GitHub Pages
```

### 7.3 Environment
- **Node**: 18+ (Astro requirement)
- **Package Manager**: npm

---

## 8. Accessibility

### WCAG 2.1 AA Compliance
- ✅ Semantic HTML (`<main>`, `<nav>`, `<h1>`)
- ✅ ARIA labels on interactive elements
- ✅ Color contrast ratios meet standards
- ✅ Keyboard navigation (Tab, Enter, Arrow keys)
- ✅ Theme respects `prefers-color-scheme`
- ✅ Focus indicators visible
- ✅ SVG illustrations have alt text / descriptions
- ✅ Theme toggle is keyboard accessible

---

## 9. Out of Scope (v2.0)

- About section / bio page
- Portfolio / projects showcase
- Blog
- Contact form
- Email newsletter signup
- Social media links (except GitHub)
- Analytics integration
- Open Graph / Twitter Card meta tags
- Sitemap / robots.txt
- 404 page
- Custom domain email
- Developer illustration animation (v2.1+)

---

## 10. Testing Checklist

### Manual Testing
- [ ] Desktop (Chrome, Firefox, Safari)
- [ ] Mobile (iOS Safari, Chrome Mobile)
- [ ] Theme toggle works (dark ↔ light)
- [ ] Theme persists after refresh
- [ ] CTA button links to cal.com
- [ ] GitHub link works
- [ ] Developer illustration displays correctly
- [ ] Developer illustration colors change with theme
- [ ] Responsive at breakpoints (320px, 768px, 1024px)
- [ ] No console errors
- [ ] Toolbar layout is correct (dev illustration left, GitHub + toggle right)

### Performance Testing
- [ ] Lighthouse score > 90
- [ ] Page load < 1s (3G)
- [ ] No layout shift (CLS < 0.1)
- [ ] SVG illustration loads quickly

### Accessibility Testing
- [ ] Keyboard navigation works (Tab, Arrow keys)
- [ ] Screen reader friendly
- [ ] Color contrast OK
- [ ] Focus indicators visible
- [ ] Theme toggle is keyboard accessible

---

## 11. Deliverables

### v2.0 (Current)
- [ ] `src/pages/index.astro` — Updated main page with new layout
- [ ] `src/components/DeveloperIllustration.astro` — Developer character SVG
- [ ] `src/components/ThemeToggle.astro` — Vertical radio button toggle
- [ ] `src/styles/` — Updated styles for new layout
- [ ] `public/` — SVG assets (if needed)
- [ ] `dist/` — Built output (static HTML)

### v2.1 (Future)
- [ ] Developer illustration animation
- [ ] Analytics integration
- [ ] Open Graph meta tags
- [ ] Sitemap
- [ ] robots.txt
- [ ] 404 page

---

## 12. Known Issues / Notes

### Current State (v1.0)
- ✅ Fully functional
- ✅ Responsive
- ✅ Theme toggle works
- ✅ Deployed and live

### Changes for v2.0
- 🔄 Toolbar reorganization (dev illustration left, GitHub + toggle right)
- 🔄 Hero section split (illustration left, content right)
- 🔄 Theme toggle redesigned (vertical radio button)
- 🔄 Developer illustration added (SVG)

### Potential Improvements
- Consider adding subtle animations on load
- Add loading state for cal.com redirect
- Consider adding "Copy email" fallback
- Add structured data (JSON-LD) for SEO

---

## 13. Success Criteria

### Launch (v2.0)
- [ ] New layout renders correctly
- [ ] Developer illustration displays in both themes
- [ ] Theme toggle works (vertical radio button)
- [ ] Page loads in < 1 second
- [ ] Lighthouse score > 90
- [ ] CTA button converts
- [ ] Mobile responsive
- [ ] No console errors
- [ ] Toolbar layout matches design (dev left, GitHub + toggle right)

### Post-Launch (v2.1+)
- [ ] Track conversion rate (compare to v1.0)
- [ ] Analyze theme preference split
- [ ] Monitor page load times
- [ ] Gather user feedback on new design
- [ ] Consider animation enhancements

---

## 14. Design Notes

### Toolbar Width
- v2.0 makes the toolbar wider to accommodate vertical theme toggle
- This is intentional — cleaner separation of concerns
- Left: Branding (developer illustration)
- Right: Actions (GitHub, theme)

### Developer Illustration
- Should be simple and friendly
- Matches the "Question Everything" vibe
- Scales responsively (large in hero, small in toolbar)
- Colors adapt to theme

### Theme Toggle
- Vertical layout (moon above sun, or vice versa)
- Selected state is clear (highlighted/underlined)
- Keyboard accessible (arrow keys)
- Smooth transition between themes

---

**Last Updated**: 2026-03-10
**Status**: 🔄 In Development (v2.0)
**Version**: 2.0
**Branch**: (TBD — create feature branch for this work)
