# Nuvue Studio Design System

## 1. Purpose

This document defines the reusable visual and interaction system for the Nuvue Studio website. It serves as a reference for maintaining consistency across pages, sections, and future updates.

## 2. Brand Direction

Nuvue Studio presents itself as a digital marketing and creative growth agency. The brand should feel:

- professional
- modern
- premium but approachable
- strategic and data-aware
- bold and conversion-focused

## 3. Design Goals

The visual system supports the following goals:

- strengthen brand trust
- make call-to-action elements obvious
- create a premium digital-agency impression
- keep content readable and structured
- support conversion-focused user journeys

## 4. Visual Identity Overview

### Core Style

- High-contrast dark base with green accent highlights
- Clean typography
- Rounded, soft-edged component shapes
- Layered cards and clear spacing
- Minimal but polished motion effects

### Brand Tone

The site should communicate:

- innovation
- integrity
- bold planning
- creative execution
- measurable business outcome

## 5. Color System

### Theme Tokens

Use the following CSS variable foundation from `css/style.css`:

- `--primary`: `#eff6e0`
- `--secondary`: `#01161E`
- `--text-color`: `#FFFFFF`
- `--text-color-2`: `var(--secondary)`
- `--accent-color`: `#84A98C`
- `--accent-color-2`: `#FFFFFF`
- `--accent-color-3`: `#52796F`
- `--accent-color-4`: `#354F52`
- `--accent-color-5`: `#01161E7D`
- `--accent-color-6`: `#84A98C85`

### Color Usage Rules

- Use `--secondary` for the main page background and dark layout surfaces.
- Use `--primary` for soft, light content surfaces and container contrast.
- Use `--accent-color` for emphasis, CTA styling, links, icon highlights, and key interactive states.
- Use `--accent-color-3` and `--accent-color-4` for layered gradients and subtle depth.
- Use `--text-color` for primary content on dark surfaces.
- Use `--text-color-2` when content appears on light surfaces.

### Semantic Color Roles

To keep color usage predictable as new sections are built, map tokens to semantic roles rather than reaching for raw hex values:

- **action-text** → `--accent-color` (`#84A98C`): primary CTA fills, links, icon highlights, active nav states.
- **action-hover** → `--accent-color-3` (`#52796F`): hover/pressed feedback on accent-colored buttons and links.
- **surface-background** → `--secondary` (`#01161E`): main page background and dark section surfaces.
- **surface-elevated** → `--accent-color-4` (`#354F52`): layered cards, gradient depth, secondary dark surfaces.
- **surface-light** → `--primary` (`#eff6e0`): light content panels and contrast blocks.
- **border-primary** → `--accent-color-6` (`#84A98C85`): card borders, input outlines, hover borders.
- **overlay-dark** → `--accent-color-5` (`#01161E7D`): image and video overlays for text contrast.

Referencing roles instead of hex values keeps new components aligned with the same visual logic used across the existing site.

## 6. Typography System

### Font

- Primary font: `Plus Jakarta Sans`
- Fallback: sans-serif

### Hierarchy

- `H1`: large display style for hero banners and page-wide leadership messaging
- `H2`: section headings
- `H3`: sub-section and card titles
- `H4`, `H5`, `H6`: smaller card and feature headings

### Text Rules

- Keep headings bold and confident.
- Use clear line spacing to avoid cramped content blocks.
- Body text should remain highly legible on the dark background.
- Link text should inherit the accent color and remain visually consistent across pages.

### Typeface Pairing Pattern

Borrowing the dual-typeface discipline from Ngital's system, Nuvue should treat Plus Jakarta Sans as a single family used across two distinct roles rather than one flat style:

- **Display role** (h1–h3, hero headline, section titles): heavier weights (`700`–`900`), tight-ish spacing, used sparingly for maximum impact.
- **UI/body role** (paragraphs, form labels, nav items, buttons): medium weight (`500`), relaxed line-height for legibility.
- **Eyebrow / label role**: a new tracked-uppercase treatment for section tags and overline text above headings — `12px`, weight `600`, `letter-spacing: 2px`, uppercase, set in `--accent-color`. This mirrors Ngital's `label-uppercase` pattern and gives Nuvue a lightweight way to introduce hierarchy above a headline without adding a second typeface.

### Typography Scale Reference

| Role | Size | Weight | Line Height | Letter Spacing | Usage |
|------|------|--------|-------------|-----------------|-------|
| Display / H1 | 100px | 900 | 1.05 | normal | Hero headline |
| H2 | 64px | 700 | 1.1 | normal | Section headings |
| H3 | 46px | 700 | 1.15 | normal | Sub-section, card titles |
| H4 | 28px | 600 | 1.2 | normal | Card/feature headings |
| H5 | 24px | 600 | 1.25 | normal | Minor headings |
| H6 | 20px | 600 | 1.3 | normal | Small headings |
| Body | 16px | 500 | 1.5 | normal | Paragraph text |
| Body small | 14px | 500 | 1.5 | normal | Captions, secondary text |
| Eyebrow label | 12px | 600 | 1.25 | 2px | Section tags, overline text |

## 7. Spacing and Layout System

### Layout Foundation

- Use a centered main container with `max-width: 1280px`.
- Use consistent horizontal and vertical section spacing.
- Maintain alignment with the site’s modular grid.

### Standard Spacing Pattern

- Section spacing: `120px 20px`
- Banner spacing: `0 30px`
- Footer spacing: `0 30px 30px 30px`

### Spacing Token Scale

Beyond the section/banner/footer padding above, adopt a 4px-based token scale for internal component spacing (gaps, padding, margins within cards, forms, and buttons) — the same granular approach used in Ngital's system, giving finer control than the large section paddings alone:

| Token | Value | Typical Use |
|-------|-------|--------------|
| `--space-4` | 4px | Icon-to-label gaps |
| `--space-8` | 8px | Tight internal padding |
| `--space-12` | 12px | Form field internal padding |
| `--space-16` | 16px | Card internal spacing |
| `--space-20` | 20px | Default section side padding |
| `--space-24` | 24px | Card-to-card gaps |
| `--space-32` | 32px | Sub-section spacing |
| `--space-48` | 48px | Block-level spacing |
| `--space-64` | 64px | Large internal section spacing |

### Grid Strategy

- Use Bootstrap grid layout to create responsive multi-column arrangements.
- On large screens, prefer two-column and three-column content blocks for clarity.
- On mobile, stack content vertically for readability and ease of use.

## 8. Border Radius and Surface Treatment

### Shape System

- Global border radius: `25px`
- Buttons and inputs use pill-like or strongly rounded shapes
- Cards use soft corners for a premium modern feel

### Radius Role Mapping

Rather than applying `25px` uniformly everywhere, break it into graduated roles (following Ngital's role-based radius pattern) so smaller controls don't look over-rounded next to large surfaces:

| Token | Value | Role |
|-------|-------|------|
| `--radius-sm` | 8px | Small controls, tags, chips |
| `--radius-base` | 12px | Inputs, small buttons |
| `--radius-card` | 20px | Cards, feature blocks |
| `--radius-pill` | 9999px | Primary CTAs, nav pill, badges |

The existing `25px` global radius remains the default for cards and large surfaces; the table above gives smaller components a proportionate, less rounded treatment.

### Surface Layers

- Keep backgrounds dark and layered
- Use accent gradients sparingly for emphasis
- Use visual hierarchy to separate major content blocks

## 9. Shadows and Elevation

The system uses controlled shadow tokens to create visual depth:

- `--box-shadow-top-left`
- `--box-shadow-bottom-right`
- `--box-shadow-top-left-wide`
- `--box-shadow-bottom-right-wide`

### Usage Guidance

- Use subtle shadow to elevate cards and action buttons.
- Avoid excessive shadow to preserve a clean and minimal design language.
- Keep shadow consistent through all interactive components.

## 10. Component System

### 10.1 Navigation

The navbar should be:

- compact
- bordered
- highly readable
- aligned with the site’s dark premium visual language

Navigation should clearly surface the primary brand paths: Home, About, Services, Contact, and other action items.

### 10.2 Banner / Hero

The hero block should include:

- a strong headline
- a concise value proposition
- one primary CTA
- optional media or video trigger

This section is the strongest brand-introduction area on the homepage.

### 10.3 Cards

Use cards for:

- services
- expertise highlights
- stats
- testimonial fragments
- feature summaries

Each card should have:

- a bordered or gradient-backed base
- rounded corners
- clear internal spacing
- accent-based emphasis for headings or CTAs

### 10.4 Buttons

Button styling should follow a consistent design pattern:

- rounded pill shape
- dark teal base with accent text
- soft hover motion
- optional icon element within the CTA

Recommended button states:

- default: dark accent background
- hover: slight interaction feedback and highlight
- focus: consistent contrast and readable outline

### CTA Pairing Pattern

Where a section needs two calls to action (e.g. "Get Started" + "Learn More"), pair a **filled pill** with a **ghost pill** rather than two filled buttons competing for attention — a pattern borrowed from Ngital's CTA system:

- **Filled pill (primary):** solid `--accent-color` or dark teal background, light text, used for the single most important action in the section.
- **Ghost pill (secondary):** transparent background, `1px` border in `--accent-color-6`, text in `--accent-color`, fills in on hover. Used for lower-priority actions placed next to a primary CTA.

This keeps hierarchy clear on banners and CTA blocks where more than one action is offered.

### 10.5 Forms

Form components should be:

- dark-themed
- user-friendly
- rounded and spacious
- easy to scan
- consistent with overall content styling

Input fields should use:

- dark neutral background
- rounded pill shape
- crisp text contrast
- visible focus styling

### 10.6 Footer

The footer should remain organized and information-rich:

- logo block
- quick links
- services links
- contact details
- social media icons

## 11. Interaction and Motion System

### Motion Principles

Motion should support clarity, not distract from it.

- Use subtle entrance animations for content reveal
- Use gentle hover transitions for buttons and links
- Use smooth panel transitions for sidebars and overlays
- Avoid noisy or excessive animation on primary content areas

### Animation Library

- `animate.min.css`
- custom CSS transitions
- modal and sidebar slide effects

### Interaction & Focus Signals

Beyond entrance animation, define lightweight interaction feedback for accessibility and polish:

- **Hover:** buttons and cards shift to `--accent-color-3`, with a soft transition (150–250ms).
- **Focus outline:** `2px` solid `--accent-color`, offset `2px`, visible on all interactive elements (buttons, links, inputs) for keyboard navigation.
- **Overlay blur:** modals and video overlays use a subtle background blur (`backdrop-filter: blur(8px)`) over `--accent-color-5` to keep focus on foreground content — a treatment adapted from Ngital's overlay pattern.

## 12. Responsive Behavior

The design system should support a smooth responsive experience across desktop, tablet, and mobile devices.

### Responsive Rules

- Use grid stacking on smaller screens
- Reduce column complexity on narrow viewports
- Preserve CTA visibility and hierarchy on mobile
- Maintain readable typography and spacing across breakpoints

### Breakpoint Notes

- Larger desktop layout: multiple-column content arrangement
- Tablet layout: adjust content widths and spacing
- Mobile layout: stack sections and preserve touch-friendly button sizes

## 13. Accessibility and Readability

The design should remain accessible and easy to scan.

### Guidelines

- Ensure strong contrast between text and background
- Keep clickable elements clearly visible
- Use readable font sizing and spacing
- Preserve focus styles for links, buttons, and form controls
- Avoid low-contrast overlays on text-heavy areas

## 14. Content-to-Design Alignment

The visual system supports the website’s content strategy:

- service-led positioning
- trust-building contact paths
- lead conversion through CTA placement
- polished agency presentation

The design should always reinforce that Nuvue Studio is a strategic digital partner, not a generic template website.

## 15. Practical Use Guidance

When adding new pages or sections:

1. Reuse the established color variables.
2. Match the typography hierarchy already defined.
3. Keep cards, banners, and CTAs visually consistent.
4. Maintain rounded, premium surfaces.
5. Prefer the existing dark-accent visual language over introducing unrelated styles.

## 16. Do's and Don'ts

A quick-reference guardrail table to keep new work consistent with the system above:

| Do | Don't |
|----|-------|
| Do use `--accent-color` for the single most important action per screen | Don't use the accent color for more than one primary CTA in the same view |
| Do pair a filled pill with a ghost pill when two CTAs sit side by side | Don't place two filled-pill buttons next to each other |
| Do use the eyebrow/label style for section tags above headings | Don't introduce a second typeface — vary weight and tracking instead |
| Do reference spacing and radius tokens from the tables above | Don't hand-pick arbitrary px values for padding or corner radius |
| Do keep a visible focus outline on every interactive element | Don't remove focus states for visual cleanliness |

## 17. Summary

The Nuvue Studio design system is built around a premium dark theme, green-accent emphasis, clean modern typography, rounded UI components, and modular page layouts. It is designed to present the company as a credible, creative, and results-driven digital marketing agency.

This revision layers in a few proven patterns from Ngital's agency design system — semantic color roles, a graduated spacing and radius token scale, an eyebrow-label typography treatment, and a filled-pill/ghost-pill CTA pairing — without changing Nuvue's core brand identity, colors, or typeface.
