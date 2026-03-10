# PRD: Paul's Personal Site v2.0

## Overview
Enhanced personal landing page with improved toolbar design and visual branding.

## Goal
Get visitors to book a call with Paul while establishing a stronger personal brand through visual design.

## Requirements

### Toolbar (Header)
- **Left side:** Simple, minimalist illustration of a developer (line art style, clean)
- **Right side:** 
  - GitHub link (icon + link)
  - Theme toggle (vertical radio button with moon/sun icons)
- Toolbar intentionally wider to accommodate new layout
- Clean spacing and alignment

### Theme Toggle
- **Style:** Vertical radio button (not a switch)
- **Icons:** Moon (dark mode) and Sun (light mode)
- **Behavior:** Click to toggle between dark and light themes
- **Visual feedback:** Clear indication of active state

### Hero Section
- Full viewport height
- Paul's name centered (large, bold)
- Clean, modern typography
- Maintains existing CTA button ("Book a Call" → https://cal.com/paul-vudmaska/15min)

### Design System
- Minimal aesthetic
- Dark/light theme support (toggled via toolbar)
- Developer illustration adds personality without clutter
- No nav, no footer — focus on the call-to-action

## Technical Notes
- Astro framework
- Responsive design (mobile-first)
- Theme state persists (localStorage)
- Accessible icons and buttons

## Success Metrics
- Theme toggle works smoothly
- Developer illustration loads quickly
- Toolbar layout is clean and balanced
- CTA conversion remains high
