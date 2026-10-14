# ERUM Interior Studio — Design System Specification

> **Document Status:** Planning & Specification (Phase: Visual Direction & Design System)  
> **Target Audience:** UI/UX Designers, Frontend Architects, Content Editors, and QA Engineers  
> **Classification Key:**  
> - `[CONFIRMED]`: Verified requirement or architectural standard.  
> - `[PROPOSED]`: Design token or component standard proposed for implementation.  
> - `[PENDING CLIENT CONFIRMATION]`: Open parameter awaiting client validation.

---

## 1. Design System Goals

The ERUM Design System provides a single, unified source of design truth for the ERUM digital ecosystem. Its core objectives are:

1. **Brand Cohesion & Restrained Luxury:** Elevate ERUM above ordinary contracting companies by enforcing an editorial, architectural visual language across all pages.
2. **Bilingual Parity (Arabic RTL & English LTR):** Ensure symmetrical design quality in both Arabic and English without visual degradation or layout breakage.
3. **High Performance & Asset Optimization:** Deliver sub-second page loads on mobile networks for visitors arriving from Instagram, TikTok, and Facebook.
4. **Content Hub Scalability:** Provide modular, reusable UI components for projects, services, articles, video explainers, and lead generation forms.
5. **Strict Accessibility (WCAG 2.1 AA):** Guarantee high typographic legibility, clear interactive targets, accessible contrast ratios, and screen-reader friendliness.

---

## 2. Design Principles

| Principle | Description | Implementation Impact |
| :--- | :--- | :--- |
| **1. Real Projects First** | Real architectural work commands the user’s focus. Design frames the work; it never competes with it. | Minimalist UI chrome, edge-to-edge photography containers, unobtrusive metadata tags. |
| **2. Restrained Luxury** | Luxury is conveyed through generous whitespace, precise proportion, and refined typography rather than garish ornament. | Generous section padding (80–120px desktop), disciplined 8px modular spacing, zero clutter. |
| **3. Navy & Gold Grounding** | Ground the experience with deep architectural navy; use gold as an intentional, purposeful accent. | Navy forms structural baselines, headers, and footers; gold highlights CTAs, badges, and focus rings. |
| **4. Content Ecosystem Integration** | Unified component language across projects, services, educational articles, and videos. | Cross-linked card components with standardized metadata chips and shared visual hierarchy. |
| **5. Mobile-First Primacy** | The majority of client acquisition starts on mobile devices via social video channels. | 44px+ touch targets, single-column reading ergonomics, sticky mobile CTA bars, zero horizontal overflow. |
| **6. Intentional Bilingual Design** | Arabic RTL is designed intentionally from cultural and spatial perspectives, not auto-mirrored. | Script-specific typographic scale, balanced line-heights, tailored punctuation, and preserved numbers. |
| **7. Accessibility by Default** | High-contrast text, visible focus rings, keyboard navigability, and reduced-motion support. | WCAG 2.1 AA compliance across all color token combinations; semantic HTML structuring. |
| **8. Performance-Driven Polish** | Target Core Web Vitals excellence (CLS < 0.1), efficient modern image containers, and lightweight micro-interactions. | Standardized aspect ratios to minimize layout shifts, responsive image testing across devices, CSS-driven hardware-accelerated animations. |

---

## 3. Color Tokens

> [!WARNING]
> Brand base values (`#203D73` and `#F5A000`) are **provisional estimates** based on the supplied logo image and are subject to client confirmation (`docs/design/01_brand_foundation.md#9-preliminary-color-palette`).

### 3.1 Brand & Semantic Token Architecture

The token system employs a semantic tier to decouple interface components from raw color codes.

#### Brand Primitive Tokens (Provisional)
```text
brand.navy.900 = #0E1B33   /* Midnight architectural navy */
brand.navy.700 = #203D73   /* Core ERUM Navy (Provisional) */
brand.navy.500 = #32589D   /* Mid-tone navy */
brand.navy.100 = #E8EEF8   /* Soft navy canvas tint */
brand.navy.50  = #F3F6FB   /* Ultra-light cool canvas */

brand.gold.700 = #B47100   /* Darkened Gold (WCAG AA compliant for text on white) */
brand.gold.500 = #F5A000   /* Core ERUM Gold (Provisional - Accents & Dark surfaces) */
brand.gold.300 = #FFC14D   /* Soft gold highlight */
brand.gold.100 = #FFF3D6   /* Subtle gold tint for badges */
```

#### Semantic Color Tokens

| Semantic Token | Value Reference | Purpose / Role | Minimum Contrast Ratio |
| :--- | :--- | :--- | :--- |
| `color.brand.primary` | `brand.navy.700` (`#203D73`) | Primary brand anchor, key headings, primary buttons, header surface. | 7.9:1 on `#FFFFFF` (AAA) |
| `color.brand.primary-dark` | `brand.navy.900` (`#0E1B33`) | Deep footer background, immersive video containers, dark card surfaces. | 13.8:1 on `#FFFFFF` (AAA) |
| `color.brand.accent` | `brand.gold.500` (`#F5A000`) | Standout CTA backgrounds, video play icons, active indicators, focus rings. | 5.2:1 on `brand.navy.900` |
| `color.brand.accent-text` | `brand.gold.700` (`#B47100`) | Gold text or links placed on white/light backgrounds. | 4.6:1 on `#FFFFFF` (AA) |
| `color.brand.accent-muted`| `brand.gold.100` (`#FFF3D6`) | Subtle background for category chips and highlight tags. | Non-text visual token |
| `color.background.primary` | `#FFFFFF` | Core light canvas, project detail page body, card surfaces. | Baseline |
| `color.background.secondary`| `#F8F9FA` | Off-white canvas for alternating sections, subtle card containers. | 1.05:1 on `#FFFFFF` |
| `color.background.tertiary` | `brand.navy.50` (`#F3F6FB`) | Cool architectural tint for technical data tables and BOQ highlights. | 1.1:1 on `#FFFFFF` |
| `color.background.surface-dark`| `brand.navy.900` (`#0E1B33`)| Solid midnight background for footer, dark hero banners, modal backdrops. | Base Dark |
| `color.background.overlay` | `rgba(14, 27, 51, 0.75)` | Modal backdrops, mobile menu scrim, photographic hero scrim. | Dependent |
| `color.text.primary` | `#111827` | Headings, primary body copy, form input text (Slate Charcoal). | 16.1:1 on `#FFFFFF` (AAA) |
| `color.text.secondary` | `#4B5563` | Subtitles, project metadata (area, location), article dates, field labels. | 4.6:1 on `#FFFFFF` (AA) |
| `color.text.tertiary` | `#9CA3AF` | Placeholder text, disabled inputs, secondary icons. | 3.0:1 on `#FFFFFF` |
| `color.text.inverse-primary`| `#FFFFFF` | Body and title text on dark navy surfaces. | 13.8:1 on `#0E1B33` (AAA) |
| `color.text.inverse-secondary`| `#D1D5DB`| Secondary metadata on dark navy surfaces. | 8.2:1 on `#0E1B33` (AAA) |
| `color.border.default` | `#E5E7EB` | Standard card borders, divider rules, subtle input outlines. | 1.2:1 (Structural) |
| `color.border.subtle` | `#F3F4F6` | Secondary divider lines between list items. | Non-text visual token |
| `color.border.focus` | `brand.gold.500` (`#F5A000`)| Accessible focus ring indicator on interactive elements. | 3.1:1 on `#FFFFFF` |
| `color.action.primary` | `brand.navy.700` (`#203D73`) | Primary interactive buttons and active links. | 7.9:1 on `#FFFFFF` |
| `color.action.primary-hover`| `brand.navy.900` (`#0E1B33`)| Hover state for primary action buttons. | 13.8:1 on `#FFFFFF` |
| `color.action.accent` | `brand.gold.500` (`#F5A000`)| High-conversion CTA buttons ("Start Your Project"). | 5.2:1 on `#0E1B33` |
| `color.feedback.success` | `#15803D` | Form submission success, verified status badges. | 4.8:1 on `#FFFFFF` (AA) |
| `color.feedback.error` | `#DC2626` | Form validation errors, required field indicators. | 4.6:1 on `#FFFFFF` (AA) |

---

## 4. Typography Tokens

### 4.1 Recommended Type Families `[PROPOSED]`
- **Latin Font Family:** `Plus Jakarta Sans`, `-apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif`
- **Arabic Font Family:** `Alexandria` or `IBM Plex Sans Arabic`, `"Segoe UI", Tahoma, Arial, sans-serif`
- **Monospace / Spec Family:** `ui-monospace, SFMono-Regular, Menlo, Monaco, Consolas, monospace` *(used for architectural project numbers, CAD dimensions, and BOQ items)*

### 4.2 Typographic Hierarchy & Scale

Tokens follow a major-third / perfect-fourth modular scale optimized for responsive editorial reading:

| Token | Desktop Size / Line-Height | Mobile Size / Line-Height | Weight | Application |
| :--- | :--- | :--- | :--- | :--- |
| `font.size.display` | `56px` / `1.1` (`62px`) | `36px` / `1.15` (`42px`) | Bold (700) | Hero Homepage Title, Major Brand Statement |
| `font.size.h1` | `42px` / `1.2` (`50px`) | `30px` / `1.25` (`38px`) | Bold (700) | Primary Page Title (Project Name, Service Title) |
| `font.size.h2` | `32px` / `1.25` (`40px`) | `24px` / `1.3` (`31px`) | SemiBold (600)| Major Section Headings ("Selected Projects", "Process") |
| `font.size.h3` | `24px` / `1.3` (`31px`) | `20px` / `1.35` (`27px`) | SemiBold (600)| Card Titles, Sub-sections, Accordion Headers |
| `font.size.h4` | `18px` / `1.4` (`25px`) | `16px` / `1.4` (`22px`) | Medium (500) | Subsection Titles, Modal Titles, Feature Headings |
| `font.size.body-lg` | `18px` / `1.6` (`29px`) | `16px` / `1.6` (`26px`) | Regular (400) | Article lead paragraphs, About intro, Project Story |
| `font.size.body-md` | `16px` / `1.6` (`26px`) | `15px` / `1.6` (`24px`) | Regular (400) | Standard body text, card descriptions, form fields |
| `font.size.body-sm` | `14px` / `1.5` (`21px`) | `13px` / `1.5` (`20px`) | Regular (400) | Metadata (Location, Area m²), Captions, Breadcrumbs |
| `font.size.caption` | `12px` / `1.4` (`17px`) | `11px` / `1.4` (`15px`) | Medium (500) | Category Badges, Overline Labels, Legal Copyright |

### 4.3 Arabic Typographic Adjustment Tokens
```text
typography.arabic.line-height-multiplier = 1.15  /* Arabic requires 15% more vertical line space */
typography.arabic.font-size-offset      = +1px   /* Arabic glyphs optical size normalization */
```

---

## 5. Spacing Scale

The spacing scale is built upon an 8px base grid, supplemented by a 4px half-step for micro-alignment.

| Token | Size | Typical Use Cases |
| :--- | :--- | :--- |
| `spacing.1` | `4px` | Fine badge padding, micro gaps between icon and text. |
| `spacing.2` | `8px` | Space between related metadata items, pill tag padding, compact chip gap. |
| `spacing.3` | `12px` | Form field internal horizontal padding, small card gap. |
| `spacing.4` | `16px` | Standard component internal padding, mobile horizontal gutters, button padding. |
| `spacing.5` | `20px` | Medium card inner padding, space below sub-headings. |
| `spacing.6` | `24px` | Standard desktop card inner padding, gap between card grid items on tablet. |
| `spacing.8` | `32px` | Desktop card grid gap, space between major card rows, form section margins. |
| `spacing.10` | `40px` | Small section padding, hero text-to-CTA margin. |
| `spacing.12` | `48px` | Mobile section vertical spacing, medium container padding. |
| `spacing.16` | `64px` | Tablet section vertical padding, prominent callout blocks. |
| `spacing.20` | `80px` | Standard desktop section padding (`padding-block: 80px`). |
| `spacing.24` | `96px` | Generous desktop section padding on homepage hero and major showcases. |
| `spacing.32` | `128px` | Maximum luxury breathing room for editorial showcases and transition zones. |

---

## 6. Layout Containers

```text
container.sm    = 640px    /* Lead forms, single-column reading articles, privacy policy */
container.md    = 768px    /* Knowledge hub reading view, Engineer's Advice detail */
container.lg    = 1024px   /* Service detail pages, About page content blocks */
container.xl    = 1280px   /* Standard content container (Home, Projects list, Services list) */
container.2xl   = 1440px   /* Wide portfolio showcases, panoramic gallery displays */
container.fluid = 100%     /* Edge-to-edge hero sections, full-width footer surface */
```

### Container Gutter Tokens
```text
container.gutter.mobile  = 16px
container.gutter.tablet  = 24px
container.gutter.desktop = 32px
```

---

## 7. Grid Guidelines

| Viewport | Proposed Breakpoint | Columns | Gutter | Margin | Layout Behavior |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **Mobile** | `< 640px` | 4 columns | `16px` | `16px` | Single-column cards; 2-column compact chips. |
| **Tablet** | `640px – 1023px` | 8 columns | `24px` | `24px` | 2-column project cards; split form layouts. |
| **Desktop** | `1024px – 1439px` | 12 columns | `32px` | `32px` | 3-column project cards; asymmetric editorial splits (7/5 or 8/4). |
| **Wide Desktop**| `1440px+` | 12 columns | `32px` | Centered (`max-width: 1440px`) | Expansive portfolio displays, high-density project matrices. |

---

## 8. Border Radius Tokens

To preserve an **architectural, precision-engineered** aesthetic, border radii are kept disciplined and subtle. Soft rounded corners are permitted only for small interactive chips.

```text
radius.none = 0px      /* Sharp architectural corners, edge-to-edge photographic containers */
radius.sm   = 2px      /* Subtle framing for technical tags, CAD thumbnails, input fields */
radius.md   = 6px      /* Standard interactive buttons, project cards, service cards, modals */
radius.lg   = 10px     /* Prominent feature cards, video player overlay frames */
radius.full = 9999px   /* Pill tags, status badges ("Residential", "Completed"), circular avatars */
```

*Design Rule:* Avoid large bubbly curves (`16px+` or `24px+`) on main cards, as they evoke casual consumer apps rather than an architectural studio.

---

## 9. Shadow & Elevation Tokens

Shadows are calibrated to be soft, diffuse, and ambient, mimicking natural daylight in a well-designed interior rather than harsh digital drop shadows.

```text
shadow.none = none
shadow.sm   = 0 1px 2px 0 rgba(14, 27, 51, 0.05)
shadow.md   = 0 4px 6px -1px rgba(14, 27, 51, 0.07), 0 2px 4px -2px rgba(14, 27, 51, 0.05)
shadow.lg   = 0 10px 15px -3px rgba(14, 27, 51, 0.08), 0 4px 6px -4px rgba(14, 27, 51, 0.04)
shadow.xl   = 0 20px 25px -5px rgba(14, 27, 51, 0.10), 0 8px 10px -6px rgba(14, 27, 51, 0.05)
shadow.dark = 0 8px 24px 0 rgba(0, 0, 0, 0.35) /* Used exclusively on dark navy surfaces */
```

---

## 10. Button Variants & Interactive States

Every interactive component must explicitly define 5 states:
1. **Default**
2. **Hover**
3. **Focus-visible** (Keyboard accessibility)
4. **Active** (Pressed state)
5. **Disabled**

```
┌────────────────────────────────────────────────────────┐
│                   BUTTON ANATOMY                       │
│  ┌──────┐ ┌──────────────────────────────────┐ ┌─────┐ │
│  │ ICON │ │       LABEL (Medium / 500)       │ │ARROW│ │
│  └──────┘ └──────────────────────────────────┘ └─────┘ │
│  Height: 48px (Desktop) / 44px (Mobile Min Target)     │
└────────────────────────────────────────────────────────┘
```

### 10.1 Button Specifications Table

| Variant | State | Background | Text Color | Border | Elevation | Focus Ring |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **Primary (Navy)** | **Default** | `brand.navy.700` (`#203D73`) | `#FFFFFF` | None | `shadow.sm` | — |
| | **Hover** | `brand.navy.900` (`#0E1B33`) | `#FFFFFF` | None | `shadow.md` | — |
| | **Focus-visible** | `brand.navy.700` | `#FFFFFF` | None | `shadow.sm` | `2px solid #F5A000` (offset 2px) |
| | **Active** | `#0A1324` | `#E5E7EB` | None | `shadow.none` | — |
| | **Disabled** | `#E5E7EB` | `#9CA3AF` | None | `shadow.none` | Cursor: not-allowed |
| **Accent (Gold CTA)** | **Default** | `brand.gold.500` (`#F5A000`) | `brand.navy.900` (`#0E1B33`) | None | `shadow.sm` | — |
| | **Hover** | `#E09300` | `brand.navy.900` | None | `shadow.md` | — |
| | **Focus-visible** | `brand.gold.500` | `brand.navy.900` | None | `shadow.sm` | `2px solid #203D73` (offset 2px) |
| | **Active** | `#C78200` | `brand.navy.900` | None | `shadow.none` | — |
| | **Disabled** | `#F3F4F6` | `#9CA3AF` | None | `shadow.none` | Cursor: not-allowed |
| **Secondary (Outline)** | **Default** | `transparent` | `brand.navy.700` (`#203D73`) | `1px solid #203D73` | None | — |
| | **Hover** | `brand.navy.50` (`#F3F6FB`) | `brand.navy.900` (`#0E1B33`) | `1px solid #0E1B33` | None | — |
| | **Focus-visible** | `transparent` | `brand.navy.700` | `1px solid #203D73` | None | `2px solid #F5A000` (offset 2px) |
| | **Active** | `brand.navy.100` | `brand.navy.900` | `1px solid #0E1B33` | None | — |
| | **Disabled** | `transparent` | `#9CA3AF` | `1px solid #E5E7EB` | None | Cursor: not-allowed |
| **Tertiary (Ghost/Text)**| **Default** | `transparent` | `brand.navy.700` (`#203D73`) | None | None | — |
| | **Hover** | `rgba(32, 61, 115, 0.06)` | `brand.navy.900` | None | None | — |
| | **Focus-visible** | `transparent` | `brand.navy.700` | None | None | `2px solid #F5A000` (offset 2px) |
| | **Active** | `rgba(32, 61, 115, 0.12)` | `brand.navy.900` | None | None | — |
| | **Disabled** | `transparent` | `#9CA3AF` | None | None | Cursor: not-allowed |

---

## 11. Link Styles

1. **Inline Editorial Link:**
   - *Default:* `color.action.primary` (`#203D73`), with an underline positioned at `text-underline-offset: 4px` and `text-decoration-thickness: 1px`.
   - *Hover:* `color.brand.accent-text` (`#B47100`), underline expands to `2px`.
   - *Focus-visible:* Outline `2px solid #F5A000`, `border-radius: 2px`.
2. **Navigational Header Link:**
   - *Default:* `color.text.primary` (`#111827`), no underline.
   - *Hover:* `color.brand.primary` (`#203D73`).
   - *Active/Current Page:* `color.brand.primary` (`#203D73`) accompanied by a 2px bottom indicator bar in `brand.gold.500`.
3. **Card Micro-Action Link ("View Project →"):**
   - Incorporates a directional arrow icon that smoothly translates `4px` in the inline reading direction on hover (`translateX(4px)` in LTR, `translateX(-4px)` in RTL).

---

## 12. Project Card Principles

The Project Card is the primary currency of the portfolio.

```
┌────────────────────────────────────────────────────────┐
│ ┌────────────────────────────────────────────────────┐ │
│ │                                                    │ │
│ │                  PROJECT IMAGE                     │ │
│ │                  (Aspect 4:3)                      │ │
│ │                                                    │ │
│ │ [BADGE: Residential]       [TAG: Render vs Reality]│ │
│ └────────────────────────────────────────────────────┘ │
│                                                        │
│  Villa Al-Noor Residence                               │
│  Beni Suef, Egypt · 420 m² · Turnkey Execution         │
│                                                        │
│  Explore Project ──────►                               │
└────────────────────────────────────────────────────────┘
```

### Card Architecture & Rules
1. **Image Container:**
   - Strict `4:3` or `16:10` aspect ratio.
   - `overflow: hidden; border-radius: radius.md;`
   - Image uses `object-fit: cover; transition: transform 300ms ease;`
   - On card hover, image scales smoothly to `1.03x`.
2. **Status & Category Badges:**
   - Positioned over image top-left (LTR) or top-right (RTL) with `8px` offset.
   - Background: `rgba(14, 27, 51, 0.85)` (Frosted Midnight Navy) with white text.
   - Special Badge: "Render vs. Reality" badge uses `brand.gold.500` text highlight.
3. **Metadata Block:**
   - `padding-block-start: spacing.3;`
   - Project Title: `font.size.h3` (`20px–24px`), SemiBold, `color.text.primary`.
   - Secondary Line: Location · Area in m² · Service Scope (`font.size.body-sm`, `color.text.secondary`).
4. **Entire Card Surface Clickable:**
   - Uses an accessible stretched-link pattern (`::after` overlay on the anchor) so keyboard users navigate cleanly without nested anchor conflicts.

---

## 13. Service Card Principles

Communicates ERUM's technical scope with clarity.

1. **Card Layout Structure:**
   - Visual header with a dedicated architectural icon (e.g., floorplan icon, compass, hardhat, joinery vector) or an authentic detail photograph.
   - Service Title: `font.size.h3` (`20px`), SemiBold.
   - Summary Paragraph: 2–3 sentences defining scope and value (`font.size.body-md`).
   - Deliverables Tags: A cluster of subtle pill chips (e.g., "3D Renders", "BOQ", "Site Supervision", "Woodwork Shop Drawings").
   - Action: "Learn More" tertiary link with directional micro-arrow.
2. **Surface Treatment:**
   - Clean white surface with `1px solid color.border.default`.
   - Hover state: Elevates from `shadow.none` to `shadow.md` and border shifts to `brand.navy.500`.

---

## 14. Article and Video Card Principles

### 14.1 Article Card (Knowledge Hub)
- **Cover Image:** `16:9` aspect ratio.
- **Header Meta:** Category Chip (e.g., "Finishing Guide") + Estimated Reading Time (e.g., "4 min read").
- **Title:** `font.size.h4`, maximum 2-line clamp to maintain uniform card grid heights.
- **Excerpt:** 2-line clamp of the summary paragraph.
- **Footer:** Publication Date.

### 14.2 Video Card (Video Library & Engineer's Advice)
- **Thumbnail:** `16:9` (Landscape) or `9:16` (Vertical Reel/Short).
- **Video Overlay Trigger:**
  - Centered circular play button: `48px` diameter, background `brand.gold.500`, dark navy triangle icon.
  - Hover state: Scales to `1.1x` with subtle glow shadow.
- **Duration Badge:** Bottom-right corner (LTR) / Bottom-left corner (RTL), e.g., `04:15`, dark translucent background.
- **Format Tag:** Badge indicating "Full Video" or "Quick Tip / Short".
- **Title & Topic Tags:** Cleanly listed below the thumbnail.

---

## 15. Form Elements (Lead Generation System)

Lead generation ("Start Your Project") is ERUM's primary business conversion goal. The form must feel effortless, prestigious, and clear on mobile devices.

```
┌────────────────────────────────────────────────────────┐
│ Project Type *                                         │
│ ┌────────────────────────────────────────────────────┐ │
│ │ Residential Villa                              [▼] │ │
│ └────────────────────────────────────────────────────┘ │
│                                                        │
│ Area (Approximate m²)                                  │
│ ┌────────────────────────────────────────────────────┐ │
│ │ e.g. 350                                           │ │
│ └────────────────────────────────────────────────────┘ │
│                                                        │
│ Service Scope                                          │
│ ┌──────────────┐ ┌──────────────┐ ┌──────────────────┐ │
│ │ (•) Full D&E │ │ ( ) Design   │ │ ( ) Execution    │ │
│ └──────────────┘ └──────────────┘ └──────────────────┘ │
└────────────────────────────────────────────────────────┘
```

### 15.1 Form Input States

| State | Border | Background | Text Color | Helper / Error Text |
| :--- | :--- | :--- | :--- | :--- |
| **Default** | `1px solid color.border.default` (`#E5E7EB`) | `#FFFFFF` | `color.text.primary` (`#111827`) | `color.text.secondary` (`#4B5563`) |
| **Hover** | `1px solid brand.navy.500` (`#32589D`) | `#FFFFFF` | `color.text.primary` | — |
| **Focus-visible**| `1px solid brand.navy.700` (`#203D73`) | `#FFFFFF` | `color.text.primary` | Focus Ring: `2px solid #F5A000` (offset 1px) |
| **Error** | `1.5px solid color.feedback.error` (`#DC2626`)| `#FEF2F2` (Soft red) | `color.text.primary` | Red error icon + text in `#DC2626` |
| **Success / Valid**| `1px solid color.feedback.success` (`#15803D`)| `#FFFFFF` | `color.text.primary` | Green check icon |
| **Disabled** | `1px solid #E5E7EB` | `#F3F4F6` | `#9CA3AF` | Cursor: not-allowed |

### 15.2 Form Dimension Standards
- **Input Height:** `48px` (Ensures comfortable 44px+ mobile touch targets).
- **Input Padding:** `padding-inline: 16px; padding-block: 12px;`
- **Label Typography:** `font.size.body-sm` (`14px`), Medium (500), `color.text.primary`.
- **Segmented / Radio Pills (Service & Budget Selection):**
  - Minimum touch target: `44px` height.
  - Selected state: Background `brand.navy.700`, text `#FFFFFF`, border `brand.navy.700`.
- **File Upload Dropzone (Floorplans / CAD / PDFs):**
  - Dashed border: `2px dashed color.border.default`.
  - Background: `brand.navy.50`.
  - Icon: Architectural blueprint / upload arrow in `brand.navy.700`.
  - Drag-over state: Background `brand.navy.100`, border `brand.gold.500`.

---

## 16. Header and Navigation

### 16.1 Desktop Navigation (Viewport ≥ 1024px)
- **Bar Height:** `80px` fixed height; resting state transparent or crisp white depending on section backdrop.
- **Scroll State:** Transitions to sticky white background (`#FFFFFF`) with `backdrop-filter: blur(8px)` and `shadow.sm`.
- **Layout Architecture:**
  - *Left (LTR) / Right (RTL):* Official ERUM logo mark (height: `44px`).
  - *Center:* Primary navigation links (`font.size.body-md`, Medium weight) `[PROPOSED NAVIGATION]`:
    1. Projects
    2. Services
    3. About
    4. Knowledge
    5. Contact
  - *Right (LTR) / Left (RTL):* Utility group:
    - Language switcher pill (`AR` / `EN` toggle button).
    - Primary CTA Button: "Start Your Project" (Accent Gold or Navy variant).
  - *Navigation Rationale:* Keeping the top navigation focused on 5 items prevents visual crowding on intermediate desktop screens (1024px–1280px) and maintains symmetrical breathing room. *Process* and *Meet The Engineer* are prominently integrated into the Home page, contextual project/service deep links, and the global footer.

### 16.2 Mobile Navigation (Viewport < 1024px)
- **Bar Height:** `64px` sticky header.
- **Elements:**
  - Responsive logo mark (height: `32px`).
  - Quick WhatsApp direct-action icon button (instant consultation access).
  - Clean animated hamburger trigger (minimum target: `48px × 48px`).
- **Mobile Menu Drawer:**
  - Full-screen or slide-in sheet from start edge.
  - Deep midnight navy surface (`brand.navy.900`) with high-contrast white typographic links.
  - Integrated direct phone, WhatsApp, and social media channels at the base of the drawer.

---

## 17. Footer

The footer serves as the architectural grounding of the digital experience, utilizing the midnight navy token (`brand.navy.900` / `#0E1B33`).

```
┌────────────────────────────────────────────────────────────────────────┐
│  ERUM INTERIOR STUDIO                                                  │
│  Interior Design · Execution · Project Management                      │
│  Eng. Abdelrahman Abdelrazek                                           │
│ ────────────────────────────────────────────────────────────────────── │
│  PROJECTS             SERVICES            KNOWLEDGE         CONTACT    │
│  Residential          Interior Design     Articles          Phone      │
│  Commercial           Execution           Videos            WhatsApp   │
│  Administrative       Project Mgmt        Advice            Address    │
│ ────────────────────────────────────────────────────────────────────── │
│  © 2026 ERUM Interior Studio. All rights reserved.     [Privacy] [Terms]│
└────────────────────────────────────────────────────────────────────────┘
```

### Footer Structural Zones
1. **Brand Statement:** Official logo, studio positioning tagline, and founder attribution.
2. **Columnar Navigation:** Four structured link columns (Projects, Services, Knowledge Hub, Company).
3. **Contact & Location:** Verified official phone, WhatsApp, studio physical address (Beni Suef), and working hours.
4. **Social Hub:** Verified links to Facebook, Instagram, TikTok, YouTube, and Google Maps.
5. **Bottom Bar:** Bilingual copyright statement, privacy policy link, terms of service link, and LTR/RTL language switch shortcut.

---

## 18. Image Aspect Ratios

To ensure layout stability and target **Cumulative Layout Shift (CLS < 0.1)** in accordance with Core Web Vitals standards, all image containers must enforce fixed proportional aspect ratios and explicit dimension attributes.

| Ratio Token | Proportion | Application |
| :--- | :--- | :--- |
| `aspect.cinema` | `16:9` | Homepage hero video, landscape educational videos, project panoramic walkthroughs. |
| `aspect.photo` | `3:2` | Editorial project feature photography, DSLR architectural captures. |
| `aspect.card` | `4:3` | Standard project grid cards, service cards, render vs. reality comparison cards. |
| `aspect.square` | `1:1` | Material detail vignettes, Eng. Abdelrahman portrait avatar, team member photos. |
| `aspect.reel` | `9:16` | Vertical mobile video reels, TikTok/Instagram story format embeds. |

---

## 19. Responsive Design Guidelines

### Proposed Breakpoint System `[PROPOSED]`

```text
breakpoint.sm = 640px    /* Phablets and large phones */
breakpoint.md = 768px    /* Tablets in portrait */
breakpoint.lg = 1024px   /* Tablets in landscape & compact laptops */
breakpoint.xl = 1280px   /* Standard desktop monitors */
breakpoint.2xl= 1536px   /* Ultra-wide desktop screens */
```

### Responsive Design Rules
1. **Mobile First:** All CSS styles should be declared for the mobile viewport first, with `@media (min-width: ...)` queries enhancing layouts as screen width expands.
2. **Fluid Typography:** Major titles should utilize responsive fluid clamping (e.g., `clamp(2rem, 5vw, 3.5rem)`) to prevent awkward line wraps on intermediate screens.
3. **Single-Column Mobile Default:** Project details, BOQ tables, and multi-step forms must collapse gracefully to single-column flows on mobile.
4. **Touch Target Protection:** No interactive element (button, link, form control, close trigger) may measure less than `44px × 44px` on touch screens.

---

## 20. Arabic RTL and English LTR

### 20.1 Logical CSS Properties (Not Physical Left/Right)
All spacing, margins, paddings, and borders in the design system must be conceptualized using CSS Logical Properties:

```text
margin-inline-start / margin-inline-end  (replaces margin-left / margin-right)
padding-inline-start / padding-inline-end (replaces padding-left / padding-right)
inset-inline-start / inset-inline-end    (replaces left / right for absolute positioning)
text-align: start / text-align: end      (replaces text-align: left / right)
```

### 20.2 Bidirectional Component Behavior

| Component | English (LTR) Behavior | Arabic (RTL) Behavior | Exception / Special Rule |
| :--- | :--- | :--- | :--- |
| **Brand Logo & Name** | Top-left in header | Top-right in header | Symmetrical placement. |
| **Navigation Links** | Reads left-to-right | Reads right-to-left | Ordered by priority. |
| **Project Card Arrow** | Points right (`→`) | Points left (`←`) | Directional iconography flips. |
| **Phone & WhatsApp** | Displayed LTR (`+20 1X...`) | **Displayed LTR** (`+20 1X...`) | **Never flipped; telecommunications standards are LTR.** |
| **Media Player Bar** | Progresses left-to-right | **Progresses left-to-right** | **Universal media standard remains LTR.** |
| **Dimensions / Units** | `450 m²` | `٤٥٠ م²` or `450 م²` | Client confirmation on Eastern vs. Western numerals. |
| **Process Steps** | Step 1 starts on left | Step 1 starts on right | Visual timeline flow is mirrored. |

---

## 21. Accessibility (a11y) Standards

The ERUM platform targets full **WCAG 2.1 Level AA** compliance.

### Accessibility Matrix
1. **Contrast Compliance:**
   - All body text must maintain a contrast ratio of at least **4.5:1** against its background.
   - Large headings (`≥ 24px` or bold `≥ 18px`) must maintain at least **3.0:1**.
   - Non-text UI controls and active borders must maintain at least **3.0:1**.
2. **Visible Focus Rings:**
   - No interactive element may have `outline: none` without an explicit `:focus-visible` replacement.
   - Standard focus ring token: `outline: 2px solid #F5A000; outline-offset: 2px;`.
3. **Screen Reader Optimization:**
   - All project images must include contextual `alt` text describing the room, style, and materials (e.g., `alt="Modern living room with walnut wood paneling and concealed warm lighting by ERUM"`).
   - Icon-only buttons (such as social links and hamburger toggles) must include an accessible `aria-label`.
4. **Semantic Document Structure:**
   - Exactly one `<h1>` per page.
   - Logical sequential heading progression (`<h1>` → `<h2>` → `<h3>`) without skipped levels.

---

## 22. Motion & Reduced Motion

### Timing & Easing Tokens

```text
motion.duration.fast   = 150ms   /* Button clicks, tag toggles, icon color changes */
motion.duration.normal = 250ms   /* Card hovers, dropdown reveals, accordion expansion */
motion.duration.slow   = 400ms   /* Modal entrances, mobile drawer slide, page transitions */

motion.easing.standard = cubic-bezier(0.2, 0.0, 0.0, 1.0) /* Natural physical deceleration */
motion.easing.enter    = cubic-bezier(0.0, 0.0, 0.2, 1.0) /* Element entrance easing */
motion.easing.exit     = cubic-bezier(0.4, 0.0, 1.0, 1.0) /* Element exit easing */
```

### Reduced Motion Override `[MANDATORY]`
For users with vestibular sensitivities who enable reduced-motion in their operating systems, all non-essential transform and translation animations must be eliminated:

```css
@media (prefers-reduced-motion: reduce) {
  * {
    animation-duration: 0.01ms !important;
    animation-iteration-count: 1 !important;
    transition-duration: 0.01ms !important;
    scroll-behavior: auto !important;
  }
}
```

---

## 23. Image Performance Guidelines

Because high-resolution architectural photography is ERUM’s primary asset, strict asset optimization rules are mandatory to prevent slow mobile experiences:

1. **Next-Generation Formats:**
   - Primary: **AVIF** (superior compression and color depth for interior gradients).
   - Secondary: **WebP** (universal fallback).
   - Legacy Fallback: **Progressive JPEG** (only for unsupported legacy browsers).
2. **Responsive Source Sets:**
   - Every project image must provide variants at `640w`, `960w`, `1280w`, `1920w`, and `2560w`.
3. **Priority Loading Rules:**
   - Above-the-fold hero imagery must load eagerly: `fetchpriority="high" loading="eager"`.
   - All below-the-fold gallery and project cards must load lazily: `loading="lazy" decoding="async"`.
4. **Dimension Attributes:**
   - Every `<img>` tag must declare explicit `width` and `height` attributes matching its natural aspect ratio to eliminate layout shifts.

---

## 24. Future Design System Implementation Notes

When moving from this specification to development:

1. **Design Token Storage:** Tokens should be stored in a centralized format (such as JSON or CSS Custom Properties) so both web platforms and future marketing assets consume identical values.
2. **Component Isolation:** Components should be built in isolation (using tools like Storybook or component previews) to verify RTL/LTR symmetry and edge cases before page assembly.
3. **Figma Component Sync:** Design tokens defined in this document should map 1:1 with Figma Variable collections (Brand, Semantic, Spacing, Radius, Typography).

---

## 25. Open Decisions

| ID | Topic | Description & Technical Impact | Current Status |
| :--- | :--- | :--- | :--- |
| **DS-01** | **Official Brand Color Codes** | Verify exact hex values for navy and gold once vector source files are delivered. | `[PENDING CLIENT CONFIRMATION]` |
| **DS-02** | **Arabic Numeral Preference** | Decide whether Arabic pages use Eastern Arabic numerals (١، ٢، ٣) or Western Arabic numerals (1, 2, 3) for areas and phone numbers. | `[PENDING CLIENT CONFIRMATION]` |
| **DS-03** | **Interactive Render-vs-Reality Widget** | Choose interaction mode: before/after slider handle vs. click-to-flip card toggle. | `[PROPOSED]` |
| **DS-04** | **Lead Form Upload Size Limit** | Determine max file size (e.g., 25MB vs. 50MB) and allowed formats (CAD/DWG vs. PDF/images only). | `[PENDING CLIENT CONFIRMATION]` |
| **DS-05** | **Dark Mode Scope** | Confirm if dark mode is limited to footers/video modals (recommended) or if a full site-wide dark toggle is desired. | `[PROPOSED: HYBRID DARK ACCENT]` |
