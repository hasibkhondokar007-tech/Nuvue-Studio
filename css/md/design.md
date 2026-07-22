# Nuvue Studio Design Documentation

## 1. Design Overview

Nuvue Studio’s website uses a polished, modern digital-agency visual style with a strong contrast between dark background surfaces and soft green accent highlights. The design communicates professionalism, creativity, and growth-oriented marketing expertise.

The overall aesthetic is:

- Premium and digital-first
- Clean and structured
- Bold but minimal
- High-contrast for readability
- Service-focused with strong calls to action

## 2. Brand Visual Identity

### Core Look and Feel

- Theme: modern corporate + creative agency
- Primary background: deep dark navy/black
- Accent color: muted sage green
- Visual tone: confident, clean, upscale, data-led

### Primary Personality Traits

- Innovative
- Trustworthy
- Bold
- Strategic
- Growth-focused

## 3. Color System

The website uses CSS custom properties defined in `css/style.css`.

### Primary Palette

- `--primary`: `#eff6e0` — soft off-white / light background tone
- `--secondary`: `#01161E` — deep dark base color
- `--text-color`: `#FFFFFF` — main white text
- `--text-color-2`: `var(--secondary)` — secondary text on light backgrounds

### Accent Palette

- `--accent-color`: `#84A98C` — main green accent
- `--accent-color-2`: `#FFFFFF` — white accent text
- `--accent-color-3`: `#52796F` — darker green support tone
- `--accent-color-4`: `#354F52` — deep teal/green support tone
- `--accent-color-5`: `#01161E7D` — semi-transparent dark overlay
- `--accent-color-6`: `#84A98C85` — translucent accent

### Utility Colors

- `--success-color`: `#06D6A0`
- `--error-color`: `#EF233C`
- `--star-color`: `#EFBC2A`
- `--accent-transparent`: `#00000000`
- `--accent-transparent-2`: `#00000073`

### Color Usage

- Dark backgrounds use `--secondary`
- Light content surfaces use `--primary`
- Interactive and emphasis elements use `--accent-color`
- Gradients and layered cards often combine `--accent-color-3` and `--accent-color-4`

### Semantic Color Roles

- **action-text** → `--accent-color`: primary CTA fills, links, icon highlights, active nav states
- **action-hover** → `--accent-color-3`: hover/pressed feedback on accent-colored buttons and links
- **surface-background** → `--secondary`: main page background and dark section surfaces
- **surface-elevated** → `--accent-color-4`: layered cards, gradient depth, secondary dark surfaces
- **surface-light** → `--primary`: light content panels and contrast blocks
- **border-primary** → `--accent-color-6`: card borders, input outlines, hover borders
- **overlay-dark** → `--accent-color-5`: image and video overlays for text contrast

## 4. Typography

### Font Family

- Primary font: `Plus Jakarta Sans`
- Imported through `font-family-plus-jakarta-sans.css`

### Typography Scale

The stylesheet defines a strong heading hierarchy:

- `h1`: 100px
- `h2`: 64px
- `h3`: 46px
- `h4`: 28px
- `h5`: 24px
- `h6`: 20px

### Font Weights

- `400` normal
- `500` medium
- `600` semibold
- `700` bold
- `900` black

### Text Style Rules

- Body text uses a modern sans-serif look
- Paragraphs are medium-weight and highly legible
- Headings are bold and spacious
- Accent text and links use the primary green accent color

### Typeface Pairing Pattern

Plus Jakarta Sans is used across two distinct roles rather than one flat style:

- **Display role** (h1–h3, hero headline, section titles): heavier weights (`700`–`900`), used sparingly for maximum impact
- **UI/body role** (paragraphs, form labels, nav items, buttons): medium weight (`500`), relaxed line-height
- **Eyebrow / label role**: tracked-uppercase treatment for section tags and overline text above headings — `12px`, weight `600`, `letter-spacing: 2px`, uppercase, set in `--accent-color`

## 5. Layout System

### Core Layout Structure

The site uses a consistent page pattern:

1. Header / Navigation
2. Main hero/banner section
3. Content section(s)
4. CTA / service / testimonial blocks
5. Footer

### Main Width Constraints

- `hero-container` uses `max-width: 1280px`
- Standard page sections use generous horizontal padding
- Most major content is centered and organized using Bootstrap grid classes

### Section Spacing

- Standard section padding: `120px 20px`
- Banner padding: `0 30px`
- Footer section padding: `0 30px 30px 30px`

### Spacing Token Scale

For internal component spacing (gaps, padding, margins within cards, forms, and buttons), a 4px-based token scale is used alongside the larger section paddings above:

- `--space-4`: 4px — icon-to-label gaps
- `--space-8`: 8px — tight internal padding
- `--space-12`: 12px — form field internal padding
- `--space-16`: 16px — card internal spacing
- `--space-20`: 20px — default section side padding
- `--space-24`: 24px — card-to-card gaps
- `--space-32`: 32px — sub-section spacing
- `--space-48`: 48px — block-level spacing
- `--space-64`: 64px — large internal section spacing

## 6. Spacing and Surface Styling

### Border Radius

- Global radius: `25px`
- Inputs and buttons are rounded with pill-like radii
- Cards and layouts generally use curved corners for a softer premium finish

### Radius Role Mapping

The global `25px` radius remains the default for cards and large surfaces. Smaller controls use a graduated scale so they don't look over-rounded next to large surfaces:

- `--radius-sm`: 8px — small controls, tags, chips
- `--radius-base`: 12px — inputs, small buttons
- `--radius-card`: 20px — cards, feature blocks
- `--radius-pill`: 9999px — primary CTAs, nav pill, badges

### Shadows

The CSS defines subtle accent-based shadow tokens:

- `--box-shadow-top-left`
- `--box-shadow-bottom-right`
- `--box-shadow-top-left-wide`
- `--box-shadow-bottom-right-wide`

These are used to create a soft layered depth effect around buttons, cards, and elevated UI elements.

## 7. Components and UI Patterns

### 7.1 Navbar

The navbar uses:

- a dark bordered container
- a rounded pill-like main wrapper
- a logo on the left
- navigation links on the right
- a mobile-friendly toggle behavior

The navigation is designed to feel professional and uncluttered.

### 7.2 Sidebar

The site includes a sliding sidebar for navigation and additional content. Styling includes:

- fixed positioning
- dark background
- green accent border and hover states
- smooth sliding transitions

### 7.3 Buttons

Buttons use a rounded capsule shape and a high-contrast accent treatment.

#### Button Style Pattern

- Primary CTA button: deep teal background
- Light text
- Rounded pill layout
- Subtle hover transitions
- Icon circle integrated into the button area

#### CTA Pairing Pattern

Where a section needs two calls to action (e.g. "Get Started" + "Learn More"), pair a **filled pill** with a **ghost pill** rather than two filled buttons competing for attention:

- **Filled pill (primary):** solid `--accent-color` or dark teal background, light text — the single most important action in the section
- **Ghost pill (secondary):** transparent background, `1px` border in `--accent-color-6`, text in `--accent-color`, fills in on hover

### 7.4 Cards

Cards are a central design element across pages. They are used for:

- service features
- expertise highlight blocks
- testimonial content
- contact information
- stat or benefit highlights

Typical card pattern:

- glassy or dark background
- green border or accent treatment
- soft internal spacing
- rounded corners
- layered shadow or highlight overlay

### 7.5 Banner Sections

The site uses large banner sections with:

- large headline typography
- strong CTA positioning
- layered content blocks
- optional video or image background treatment

The hero/banner is a key visual anchor on the homepage and service pages.

### 7.6 Forms

The contact and newsletter forms follow a minimal dark-tech style:

- dark input backgrounds
- rounded pill inputs
- green accent border/hover emphasis
- clear spacing and easy readability
- validation and error display blocks styled for contrast

### 7.7 Footer

The footer uses a structured four-column layout with:

- logo area
- quick links
- services links
- contact details and social media

It reinforces the brand with a consistent dark background and accent colors.

## 8. Imagery and Visual Treatment

The website relies on:

- branded logo assets
- service and expertise photography
- background gradients
- dark overlays for contrast
- image cards with layered text overlays

Images are styled to stay clean and professional, while supporting the site’s digital marketing identity.

## 9. Motion and Animation

The design uses animation for premium interaction and UI polish.

### Animation System

- Imported animation library: `animate.min.css`
- Animation speed variables:
  - `--animation-normal: 1.25s`
  - `--animation-slow: 2s`
  - `--animation-fast: 0.75s`

### Animation Behavior

- Fade and slide transitions appear on content sections
- Hover transitions soften interactive feedback
- Sidebar and modal elements animate in/out
- Video modal uses overlay interaction patterns

### Interaction & Focus Signals

- **Hover:** buttons and cards shift to `--accent-color-3`, with a soft transition (150–250ms)
- **Focus outline:** `2px` solid `--accent-color`, offset `2px`, visible on all interactive elements for keyboard navigation
- **Overlay blur:** modals and video overlays use a subtle background blur (`backdrop-filter: blur(8px)`) over `--accent-color-5` to keep focus on foreground content

## 10. Responsive Design

The stylesheet includes responsive rules for common breakpoints.

### Key Responsive Breakpoints

- `min-width: 1024px` for larger desktop layouts
- `max-width: 1024px` for tablet and mid-sized screen adjustments
- `min-width: 767px` and `max-width: 767px` for tablet/mobile adaptation

### Responsive Strategy

- Use Bootstrap grid columns with stacked layouts on smaller screens
- Reduce headline scale and spacing for mobile view
- Adapt the content width and service grids to single-column stacking
- Convert the navigation into a compact, mobile-friendly experience

## 11. Design Principles

The current design follows these principles:

- Clarity over clutter
- Strong contrast for readability
- Professional digital branding
- CTA-first page composition
- Clean modular layout with reusable section styles

### Do's and Don'ts

| Do | Don't |
|----|-------|
| Do use `--accent-color` for the single most important action per screen | Don't use the accent color for more than one primary CTA in the same view |
| Do pair a filled pill with a ghost pill when two CTAs sit side by side | Don't place two filled-pill buttons next to each other |
| Do use the eyebrow/label style for section tags above headings | Don't introduce a second typeface — vary weight and tracking instead |
| Do reference spacing and radius tokens from the design system | Don't hand-pick arbitrary px values for padding or corner radius |
| Do keep a visible focus outline on every interactive element | Don't remove focus states for visual cleanliness |

## 12. Page Design Patterns

Across the site, recurring page patterns include:

- banner header with breadcrumb navigation
- two-column content layout
- service card grids
- choice/benefit blocks
- CTA callouts
- FAQ and testimonial sections
- contact and lead form sections

## 13. UX and Conversion Style

The site is structured around conversion and service positioning rather than purely editorial content. Key UX characteristics:

- clear service messaging
- visible call-to-action buttons
- structured information blocks
- trust-building contact details
- direct funnel toward inquiry or consultation

## 14. Technical Design Stack Behind the UI

The design uses a combination of:

- custom CSS in `css/style.css`
- Bootstrap layout components
- Font Awesome icons
- Swiper for sliders
- Animate.css for entrance effects
- a dark premium visual theme with reusable CSS variables

## 15. Design Summary

Nuvue Studio’s website design is a dark, modern, conversion-oriented digital agency aesthetic built around:

- deep navy base backgrounds
- soft sage green accents
- bold typography
- rounded UI components
- layered cards and gradients
- clean responsive structure
- premium motion and hover states

This design is well suited for a digital marketing brand that wants to feel both credible and creative.

This document has been aligned with the updated `design-system.md`: semantic color roles, a graduated spacing and radius token scale, an eyebrow-label typography treatment, a filled-pill/ghost-pill CTA pairing pattern, and interaction/focus signals are now consistent across both files, with Nuvue's core brand colors and typeface unchanged.
