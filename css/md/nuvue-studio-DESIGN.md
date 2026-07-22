---
version: alpha
name: "Dark Indigo Glow"
description: "Nuvue Studio is a dark-mode digital marketing agency site built on a deep navy/indigo foundation (oklch 14% chroma 0.04 hue 275) with a vivid violet primary accent (oklch 60% chroma 0.22 hue 275). The hero section uses massive Space Grotesk display type at 104px with tight negative letter-spacing, contrasted by DM Sans body copy. Radial gradient overlays create atmospheric depth without hard shadows. CTAs use fully-rounded pill buttons with a violet glow shadow. Cards and surfaces use slightly elevated dark surfaces (oklch 19–24%) with subtle violet-tinted borders."
colors:
  primary-violet: "#6b5ce7"
  secondary-violet-deep: "#3b2a7a"
  accent-glow: "#8b6ff0"
  background: "#0d0d14"
  badge-background: "#1b1b1b"
  surface: "#171724"
  surface-2: "#1e1e32"
  badge-text: "#c5c1b9"
  foreground: "#f9f9fb"
  muted-foreground: "#9999b0"
  border-violet: "#6b5ce7"
typography:
  display-hero:
    fontFamily: "Space Grotesk"
    fontSize: "104px"
    fontWeight: "700"
    lineHeight: "104px"
    letterSpacing: "-2.6px"
  display-large:
    fontFamily: "Space Grotesk"
    fontSize: "60px"
    fontWeight: "700"
    lineHeight: "60px"
    letterSpacing: "-1.8px"
  heading-2xl:
    fontFamily: "Space Grotesk"
    fontSize: "24px"
    fontWeight: "700"
    lineHeight: "32px"
    letterSpacing: "-0.72px"
  heading-xl:
    fontFamily: "Space Grotesk"
    fontSize: "20px"
    fontWeight: "700"
    lineHeight: "28px"
    letterSpacing: "-0.6px"
  label-uppercase:
    fontFamily: "Space Grotesk"
    fontSize: "11px"
    fontWeight: "600"
    lineHeight: "16.5px"
    letterSpacing: "2.5px"
  label-medium:
    fontFamily: "Space Grotesk"
    fontSize: "15px"
    fontWeight: "600"
    lineHeight: "22.5px"
  label-small:
    fontFamily: "Space Grotesk"
    fontSize: "14px"
    fontWeight: "600"
    lineHeight: "20px"
  body-base:
    fontFamily: "DM Sans"
    fontSize: "16px"
    fontWeight: "400"
    lineHeight: "24px"
  body-small:
    fontFamily: "DM Sans"
    fontSize: "14px"
    fontWeight: "400"
    lineHeight: "20px"
  body-medium-weight:
    fontFamily: "DM Sans"
    fontSize: "14px"
    fontWeight: "500"
    lineHeight: "20px"
rounded:
  radius-badge: "6px"
  radius-base: "24px"
  radius-card: "28px"
  radius-card-lg: "36px"
  radius-pill: "9999px"
spacing:
  spacing-1: "4px"
  spacing-2: "8px"
  spacing-3: "12px"
  spacing-4: "16px"
  spacing-5: "20px"
  spacing-6: "24px"
  spacing-7: "28px"
  spacing-8: "32px"
  spacing-10: "40px"
  spacing-12: "48px"
  spacing-14: "56px"
  spacing-16: "64px"
  spacing-24: "96px"
  spacing-26: "104px"
---

## Overview

Nuvue Studio is a dark-mode digital marketing agency site built on a deep navy/indigo foundation (oklch 14% chroma 0.04 hue 275) with a vivid violet primary accent (oklch 60% chroma 0.22 hue 275). The hero section uses massive Space Grotesk display type at 104px with tight negative letter-spacing, contrasted by DM Sans body copy. Radial gradient overlays create atmospheric depth without hard shadows. CTAs use fully-rounded pill buttons with a violet glow shadow. Cards and surfaces use slightly elevated dark surfaces (oklch 19–24%) with subtle violet-tinted borders.

**Signature traits:**
- Dual typeface system: Pairs Space Grotesk and DM Sans across the type hierarchy.
- Soft, rounded geometry: Generous corner rounding up to 9999px.
- Layered elevation: Depth comes from 1 validated shadow token.

## Colors

The palette uses 11 validated color tokens across 1 theme profile. Semantic roles stay attached to observed usage so generation agents can choose accents without inventing new color meaning.

**Semantic naming:**
- **surface-background** maps to `background`: Role "background" is grounded by usage context "Page-level background, deep navy-indigo base".
- **surface-text** maps to `foreground`: Role "text" is grounded by usage context "Primary text on dark backgrounds, headings and body copy".
- **content-background** maps to `surface-2`: Role "background" is grounded by usage context "Secondary card layer, stat blocks inside hero card".
- **action-primary** maps to `primary-violet`: Role "primary" is grounded by usage context "Primary CTA buttons, active nav links, accent text highlights, glow shadows".

### Primary Brand
- **Primary Violet** (#6b5ce7): Primary CTA buttons, active nav links, accent text highlights, glow shadows. Role: primary.
- **Accent Glow** (#8b6ff0): Gradient highlights, glow overlays, accent-glow variable. Role: accent.

### Text Scale
- **Badge Text** (#c5c1b9): Lovable badge label text — warm gray. Role: text.
- **Foreground** (#f9f9fb): Primary text on dark backgrounds, headings and body copy. Role: text.
- **Muted Foreground** (#9999b0): Secondary/muted body text, captions, supporting copy. Role: text.

### Interactive
- **Secondary Violet Deep** (#3b2a7a): Gradient start, deep accent fills, accent-deep surfaces. Role: secondary.
- **Border Violet** (#6b5ce7): Card borders, input outlines — violet-tinted semi-transparent. Role: border. {authored: #6b5ce738, alpha: 0.22}

### Surface & Shadows
- **Background** (#0d0d14): Page-level background, deep navy-indigo base. Role: background.
- **Badge Background** (#1b1b1b): Lovable badge background — dark neutral chip. Role: background.
- **Surface** (#171724): Card and panel backgrounds, slightly elevated from page base. Role: background.
- **Surface 2** (#1e1e32): Secondary card layer, stat blocks inside hero card. Role: background.

## Typography

Typography uses Space Grotesk, DM Sans across extracted hierarchy roles. Keep hierarchy mapped to these token rows before adding decorative type styles.

Mixes Space Grotesk and DM Sans for visual contrast. Weight range spans bold, semi-bold, regular, medium. Sizes range from 11px to 104px.

### Font Roles
- **Headline Font**: Space Grotesk
- **Body Font**: Space Grotesk

### Type Scale Evidence
| Role | Font | Size | Weight | Line Height | Letter Spacing | Stack / Features | Notes |
|------|------|------|--------|-------------|----------------|------------------|-------|
| Hero headline — maximum visual impact, tight leading | Space Grotesk | 104px | 700 | 104px | -2.6px | Space Grotesk, ui-sans-serif, system-ui, sans-serif | Extracted token |
| Section hero headings | Space Grotesk | 60px | 700 | 60px | -1.8px | Space Grotesk, ui-sans-serif, system-ui, sans-serif | Extracted token |
| Card headings, section sub-headings | Space Grotesk | 24px | 700 | 32px | -0.72px | Space Grotesk, ui-sans-serif, system-ui, sans-serif | Extracted token |
| Feature headings, card titles | Space Grotesk | 20px | 700 | 28px | -0.6px | Space Grotesk, ui-sans-serif, system-ui, sans-serif | Extracted token |
| Section eyebrow labels, category tags — spaced uppercase | Space Grotesk | 11px | 600 | 16.5px | 2.5px | Space Grotesk, ui-sans-serif, system-ui, sans-serif | Extracted token |
| Navigation items, button labels, UI labels | Space Grotesk | 15px | 600 | 22.5px | normal | Space Grotesk, ui-sans-serif, system-ui, sans-serif | Extracted token |
| Small UI labels, stat captions | Space Grotesk | 14px | 600 | 20px | normal | Space Grotesk, ui-sans-serif, system-ui, sans-serif | Extracted token |
| Primary body copy, paragraph text | DM Sans | 16px | 400 | 24px | normal | DM Sans, ui-sans-serif, system-ui, sans-serif | Extracted token |
| Secondary body text, card descriptions, captions | DM Sans | 14px | 400 | 20px | normal | DM Sans, ui-sans-serif, system-ui, sans-serif | Extracted token |
| Emphasized body text, button secondary labels | DM Sans | 14px | 500 | 20px | normal | DM Sans, ui-sans-serif, system-ui, sans-serif | Extracted token |

## Layout

Responsive system uses 1 breakpoint tier(s): desktop.

This system uses a 4px base grid with scale values 4, 8, 12, 16, 20, 24, 28, 32, 40, 48, 56, 64, 96, 104.

### Responsive Strategy
- **desktop (Unknown)**: Expand layout density and horizontal composition for wide viewports.

### Spacing System
| Token | Value | Px | Notes |
|------|-------|----|-------|
| spacing-1 | 4px | 4 | Mapped to --spacing |
| spacing-2 | 8px | 8 | Extracted spacing token |
| spacing-3 | 12px | 12 | Extracted spacing token |
| spacing-4 | 16px | 16 | Extracted spacing token |
| spacing-5 | 20px | 20 | Extracted spacing token |
| spacing-6 | 24px | 24 | Extracted spacing token |
| spacing-7 | 28px | 28 | Extracted spacing token |
| spacing-8 | 32px | 32 | Extracted spacing token |
| spacing-10 | 40px | 40 | Extracted spacing token |
| spacing-12 | 48px | 48 | Extracted spacing token |
| spacing-14 | 56px | 56 | Extracted spacing token |
| spacing-16 | 64px | 64 | Extracted spacing token |
| spacing-24 | 96px | 96 | Extracted spacing token |
| spacing-26 | 104px | 104 | Extracted spacing token |

## Elevation & Depth

Keep depth flat unless validated shadow or interaction evidence appears in the extraction payload. Do not invent shadows beyond this evidence boundary.

### Shadow Evidence
| Shadow Token | Layers | Details |
|--------------|--------|---------|
| shadow-glow-primary | 1 | 0.22 0px 10px 30px |

### Interaction Signals
| Theme | Signal | Evidence |
|-------|--------|----------|
| Light | backdrop-filter | blur(8px) ; blur(16px) |
| Light | outline-color | oklch(0.98 0.005 260) ; oklch(0.6 0.22 275) ; oklch(0.72 0.03 270) |
| Light | outline-width | 3px |
| Light | outline-offset | 0px |
| Light | transform | matrix(1, 0, 0, 1, 0, 0) |

## Shapes

Shape language maps directly to rounded tokens. Keep component corners consistent with the role mapping below before introducing bespoke geometry.

### Radius Roles
| Token | Value | Px | Role Mapping |
|------|-------|----|--------------|
| radius-badge | 6px | 6 | Subtle corner |
| radius-base | 24px | 24 | Large surface corner |
| radius-card | 28px | 28 | Large surface corner |
| radius-card-lg | 36px | 36 | Large surface corner |
| radius-pill | 9999px | 9999 | Large surface corner |

### Geometry Evidence
| Radius Token | Shape | Units |
|--------------|-------|-------|
| radius-badge | 6px | px |
| radius-base | 24px | px |
| radius-card | 28px | px |
| radius-card-lg | 36px | px |
| radius-pill | 9999px | px |

## Components

(none detected)

## Do's and Don'ts

Guardrails protect Dual typeface system, Soft, rounded geometry, Layered elevation without adding unsupported visual claims.

| Do | Don't |
|----|---------|
| Do maintain consistent spacing using the base grid | Don't make unsupported claims about absent visual features |
| Do maintain WCAG AA contrast ratios (4.5:1 for normal text) | Don't mix rounded and sharp corners in the same view |
| Do use the primary color only for the single most important action per screen |  |
| Do verify evidence before writing new design-system guidance |  |

## Responsive Evidence

### Breakpoints
| Name | Width | Key Changes |
|------|-------|-------------|
| Breakpoint 1 | Unknown | (prefers-contrast: high) |

## Agent Prompt Guide

### Example Component Prompts
- Create button component using validated primary color role and spacing tokens.
- Create card component with mapped radius role and evidence-backed elevation.
- Create form input component using inferred typography hierarchy and border roles.

### Iteration Guide
1. Start with extracted palette and typography roles only.
2. Map spacing and radius directly from token tables before visual polish.
3. Apply component patterns one section at a time and compare against source intent.
4. Keep elevation claims tied to explicit evidence in output.
5. Iterate with smallest diffs and re-check section hierarchy after each change.
