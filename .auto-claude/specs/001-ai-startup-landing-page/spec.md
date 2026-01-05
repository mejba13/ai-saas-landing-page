# Specification: AI Startup Landing Page

## Overview

Build a modern, professional landing page for an AI SaaS startup (branded as "Twinkle.ai" - an AI Web orchestration platform). The landing page replicates the design shown in the reference screenshot, featuring a clean header with navigation, a compelling hero section with large typography, floating UI element cards over a gradient-styled product image, and a social proof logo bar. The implementation prioritizes responsive design, subtle animations, and a polished premium aesthetic that conveys trust and innovation.

## Workflow Type

**Type**: feature

**Rationale**: This is a new feature implementation building an entire landing page from scratch. The project has no existing code, so we're creating all components, styles, and structure. This requires a comprehensive implementation plan with multiple connected components.

## Task Scope

### Services Involved
- **frontend** (primary) - Single-page landing page application with all UI components

### This Task Will:
- [ ] Set up project structure with modern frontend tooling (Vite + React + TypeScript)
- [ ] Implement responsive navigation header with logo and menu items
- [ ] Create hero section with large headline, subtext, and dual CTA buttons
- [ ] Build product showcase section with floating UI cards over gradient background
- [ ] Implement social proof logo bar with company logos
- [ ] Add subtle animations and hover effects throughout
- [ ] Ensure full responsiveness across mobile, tablet, and desktop

### Out of Scope:
- Backend API development
- User authentication flows
- Database integration
- Additional pages beyond the landing page
- Payment/pricing functionality
- Actual download functionality (buttons will be placeholder)

## Service Context

### Frontend (Primary Service)

**Tech Stack:**
- Language: TypeScript
- Framework: React 18
- Build Tool: Vite
- Styling: Tailwind CSS
- Animations: Framer Motion (optional, CSS animations for simple effects)
- Package Manager: npm

**Entry Point:** `src/main.tsx`

**How to Run:**
```bash
npm install
npm run dev
```

**Port:** 5173 (Vite default)

## Files to Create

| File | Purpose |
|------|---------|
| `package.json` | Project dependencies and scripts |
| `vite.config.ts` | Vite configuration |
| `tailwind.config.js` | Tailwind CSS configuration with custom colors |
| `tsconfig.json` | TypeScript configuration |
| `index.html` | HTML entry point |
| `src/main.tsx` | React entry point |
| `src/App.tsx` | Main application component |
| `src/index.css` | Global styles and Tailwind imports |
| `src/components/Header.tsx` | Navigation header component |
| `src/components/Hero.tsx` | Hero section component |
| `src/components/ProductShowcase.tsx` | Product image with floating cards |
| `src/components/LogoBar.tsx` | Social proof logo section |
| `src/components/Button.tsx` | Reusable button component |
| `src/components/FloatingCard.tsx` | Floating UI card components |
| `public/images/` | Static images directory |

## Design Specifications

### Color Palette

| Color | Hex | Usage |
|-------|-----|-------|
| Primary Black | `#000000` | Headlines, primary buttons, logo |
| Pure White | `#FFFFFF` | Background, secondary button text |
| Off-White | `#FAFAFA` | Page background |
| Light Gray | `#E5E7EB` | Borders, secondary elements |
| Medium Gray | `#6B7280` | Body text, subtitles |
| Gradient Yellow | `#E5F52A` | Hero gradient start |
| Gradient Green | `#7FE67C` | Hero gradient middle |
| Gradient Purple | `#9B87F5` | Hero gradient end |
| Success Green | `#22C55E` | "Secure" badge |
| Notification Red | `#EF4444` | Notification indicators |

### Typography

| Element | Font | Weight | Size (Desktop) | Size (Mobile) |
|---------|------|--------|----------------|---------------|
| Logo | Inter/System | 600 | 20px | 18px |
| Nav Links | Inter/System | 500 | 14px | 14px |
| H1 (Hero) | Inter/System | 700 | 72px | 40px |
| Subtitle | Inter/System | 400 | 18px | 16px |
| Button Primary | Inter/System | 600 | 16px | 14px |
| Button Secondary | Inter/System | 500 | 16px | 14px |

### Spacing & Layout

| Element | Value |
|---------|-------|
| Container Max Width | 1280px |
| Container Padding | 24px (mobile) / 32px (desktop) |
| Header Height | 72px |
| Section Spacing | 80px (mobile) / 120px (desktop) |
| Button Padding | 16px 24px |
| Border Radius (Buttons) | 9999px (pill shape) |
| Border Radius (Cards) | 12px |

### Component Specifications

#### 1. Header Navigation
- **Left**: Logo with icon ("Twinkle.ai" with X/star symbol)
- **Center**: Navigation links - Product (dropdown), Solutions (dropdown), FAQ, Support
- **Right**: "Pricing" text link, "Download for Web" black pill button
- **Behavior**: Sticky on scroll, white background with subtle shadow on scroll
- **Mobile**: Hamburger menu with slide-out drawer

#### 2. Hero Section
- **Headline**: "The Leading AI Web orchestration Platform"
- **Subtext**: "Build and ship AI workflows in minutes—no IT bottlenecks"
- **Primary CTA**: "Get Started — It's Free" (black pill button)
- **Secondary CTA**: "Download — Mobile App" (white pill button with black border)
- **Alignment**: Center-aligned
- **Animation**: Fade-in on load, subtle hover effects on buttons

#### 3. Product Showcase
- **Central Image**: Grayscale person figure
- **Background**: Yellow-green to purple gradient blob shape
- **Floating Cards**: 4 UI element cards positioned around the figure
  - Top-left: Notification card with avatar and "12 New" badge
  - Left: User message card "Andrew Jr." with timestamp
  - Top-right: "Co-Pilot" card with verified badge and action icons
  - Right: "Automate" card with "Secure" badge
- **Animation**: Subtle floating animation on cards

#### 4. Logo Bar
- **Layout**: Horizontal row of company logos
- **Logos**: Rakuten, NCR, monday.com, Disney, Dropbox (placeholder SVGs)
- **Style**: Grayscale, consistent height
- **Spacing**: Even distribution with generous margins

## Requirements

### Functional Requirements

1. **Responsive Navigation**
   - Description: Header with logo, navigation links, and CTA that adapts to all screen sizes
   - Acceptance: Navigation collapses to hamburger menu on mobile (<768px)

2. **Hero Section Display**
   - Description: Large headline with supporting text and dual action buttons
   - Acceptance: Text is legible, buttons are clickable, layout centers properly

3. **Product Showcase with Floating Elements**
   - Description: Central image with gradient background and animated floating cards
   - Acceptance: Cards float subtly, responsive layout maintains visual hierarchy

4. **Social Proof Logo Bar**
   - Description: Row of partner/client logos showing trust signals
   - Acceptance: Logos display evenly, grayscale filter applied, responsive

5. **Responsive Design**
   - Description: Layout adapts seamlessly from mobile (320px) to desktop (1920px+)
   - Acceptance: No horizontal scroll, proper stacking on mobile, optimal spacing

6. **Interactive Animations**
   - Description: Subtle animations enhance UX without distraction
   - Acceptance: Hover states on buttons, fade-in on scroll, floating card animation

### Edge Cases

1. **Very Small Screens (<320px)** - Ensure text doesn't overflow, buttons stack vertically
2. **Very Large Screens (>1920px)** - Content remains centered, max-width prevents over-stretching
3. **Slow Network** - Images load progressively, layout doesn't shift on load
4. **No JavaScript** - Basic layout should still display (graceful degradation)
5. **Touch Devices** - Hover states work appropriately, tap targets are large enough

## Implementation Notes

### DO
- Use Tailwind CSS utility classes for consistent styling
- Follow mobile-first responsive approach
- Use semantic HTML elements (header, main, section, nav)
- Implement component-based architecture with clear separation
- Use CSS variables in Tailwind config for the color palette
- Optimize images (use WebP format, implement lazy loading)
- Add proper aria labels for accessibility
- Use Inter font from Google Fonts or system font stack

### DON'T
- Don't use inline styles when Tailwind classes suffice
- Don't create overly complex animation sequences
- Don't neglect keyboard navigation
- Don't hard-code colors - use Tailwind theme values
- Don't forget hover/focus states on interactive elements
- Don't use px units for typography - use rem/em

## Development Environment

### Project Setup

```bash
# Create new Vite project
npm create vite@latest . -- --template react-ts

# Install dependencies
npm install

# Install Tailwind CSS
npm install -D tailwindcss postcss autoprefixer
npx tailwindcss init -p

# Install additional dependencies
npm install framer-motion lucide-react
```

### Start Development Server

```bash
npm run dev
```

### Service URLs
- Development Server: http://localhost:5173

### Build for Production

```bash
npm run build
npm run preview
```

## Success Criteria

The task is complete when:

1. [ ] Project scaffolding complete with Vite + React + TypeScript + Tailwind
2. [ ] Navigation header displays correctly with logo, links, and CTA button
3. [ ] Hero section shows headline, subtitle, and both CTA buttons
4. [ ] Product showcase displays with gradient background and floating UI cards
5. [ ] Logo bar shows partner logos in a row
6. [ ] Layout is fully responsive (320px to 1920px+)
7. [ ] Hover states and subtle animations implemented
8. [ ] No console errors
9. [ ] Page loads within 3 seconds on standard connection
10. [ ] Visual design matches reference screenshot

## QA Acceptance Criteria

**CRITICAL**: These criteria must be verified by the QA Agent before sign-off.

### Visual Verification

| Component | Check | Expected |
|-----------|-------|----------|
| Header | Logo visible | "Twinkle.ai" with icon displays |
| Header | Nav links | Product, Solutions, FAQ, Support visible |
| Header | CTA button | "Download for Web" black pill button |
| Hero | Headline | Large bold text, properly sized |
| Hero | Buttons | Two pill buttons, correct colors |
| Showcase | Image | Grayscale person with gradient bg |
| Showcase | Cards | 4 floating cards positioned correctly |
| Logo Bar | Logos | 5 company logos, grayscale, aligned |

### Responsive Testing

| Breakpoint | Width | Checks |
|------------|-------|--------|
| Mobile S | 320px | No overflow, stacked layout, readable text |
| Mobile L | 425px | Proper spacing, hamburger menu |
| Tablet | 768px | Nav may collapse, balanced layout |
| Laptop | 1024px | Full nav visible, optimal spacing |
| Desktop | 1440px | Centered content, max-width respected |

### Interaction Testing

| Element | Action | Expected Result |
|---------|--------|-----------------|
| Nav links | Hover | Subtle color change |
| CTA buttons | Hover | Scale/shadow effect |
| CTA buttons | Click | Clickable (no action needed) |
| Mobile menu | Tap | Menu opens/closes |
| Floating cards | Load | Subtle floating animation |

### Performance Testing

| Metric | Target |
|--------|--------|
| First Contentful Paint | < 1.5s |
| Largest Contentful Paint | < 2.5s |
| Cumulative Layout Shift | < 0.1 |
| No console errors | Pass |
| No broken images | Pass |

### Accessibility Testing

| Check | Tool | Expected |
|-------|------|----------|
| Color contrast | Browser DevTools | WCAG AA compliant |
| Keyboard navigation | Manual | All interactive elements reachable |
| Screen reader | VoiceOver/NVDA | Content properly announced |
| Focus indicators | Manual | Visible focus states |

### Browser Verification

| Browser | Version | Check |
|---------|---------|-------|
| Chrome | Latest | Full functionality |
| Firefox | Latest | Full functionality |
| Safari | Latest | Full functionality |
| Mobile Safari | iOS | Touch interactions work |
| Chrome Mobile | Android | Touch interactions work |

### QA Sign-off Requirements
- [ ] All visual components match reference design
- [ ] Responsive layout verified at all breakpoints
- [ ] All interactive elements have proper states
- [ ] Performance metrics within targets
- [ ] Accessibility requirements met
- [ ] No console errors or warnings
- [ ] Cross-browser compatibility verified
- [ ] Build completes without errors

## Reference Design

The design reference is available at:
`attachments/bb86f0db641a7dad44c10effc149596a.webp`

Key design elements to replicate:
1. Clean, white background with high contrast black typography
2. Rounded pill-shaped buttons (primary: black, secondary: white with border)
3. Product showcase with gradient blob (yellow-green to purple)
4. Floating UI cards with subtle shadows and rounded corners
5. Grayscale company logos in social proof section
6. Modern sans-serif typography with clear hierarchy
7. Generous white space and padding throughout
