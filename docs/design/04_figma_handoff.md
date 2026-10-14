# ERUM Interior Studio — Figma Design Handoff & UI Specification

> **Document Status:** Planning & Design System Handoff (Phase: Pre-Figma UI Design)  
> **Target Audience:** UI/UX Designers, Figma Design Leads, Creative Directors, and Frontend Engineers  
> **Classification Key:**  
> - `[CONFIRMED]`: Established requirement or verified project constraint.  
> - `[PROPOSED]`: Design decision, layout recommendation, or token proposed for client review.  
> - `[PENDING CLIENT CONFIRMATION]`: Open parameter awaiting client validation or asset delivery.

---

## 1. Project Design Objectives

The ERUM Interior Studio website is an engineering-driven, editorial-grade digital experience serving six core functions:
1. **Premium Architectural Portfolio:** Present completed residential, commercial, and administrative projects with uncompromising visual quality.
2. **Brand Authority Platform:** Establish ERUM as an engineering-led interior design, turnkey execution, and project management studio, distinctly separated from informal finishing contractors.
3. **Personal Brand Anchor:** Position Engineer Abdelrahman Abdelrazek as an approachable, authoritative design and execution mentor.
4. **Knowledge & Video Platform:** Distribute practical finishing guides, material education, and site walkthroughs that organically capture high-intent organic and social search traffic.
5. **High-Conversion Lead Generation:** Streamline qualified client inquiries through a structured, reassuring project onboarding flow.
6. **Bilingual Parity:** Deliver identical aesthetic, spatial, and typographical excellence in both Arabic (RTL) and English (LTR).

---

## 2. Confirmed Design Principles `[CONFIRMED]`

The following eight principles are non-negotiable and must guide all Figma layouts, component variants, and prototyping:

1. **Real Projects First:** Real interior photography and architectural craftsmanship take center stage. UI elements (cards, borders, navigation) exist solely to frame and elevate the physical work.
2. **Restrained Luxury:** Luxury is expressed through generous whitespace, disciplined 8px modular rhythm, and sophisticated editorial typography. Avoid gaudy gold gradients, heavy 3D bevels, decorative swirls, or cheap promotional banners.
3. **Navy & Gold Anchor:** Ground the experience with deep architectural navy (`#203D73` / `#0E1B33`); deploy warm gold (`#F5A000`) with surgical restraint for focal triggers (CTAs, play buttons, active indicators).
4. **Integrated Content Ecosystem:** Content is not an isolated blog; every article and video directly surfaces related completed projects and service engagement options.
5. **Mobile-First Primacy:** Over 70% of inbound client traffic originates from mobile social channels (TikTok, Instagram, Facebook). Mobile screens require zero horizontal overflow, 44px+ touch targets, and sticky direct consultation triggers.
6. **Intentional Symmetrical Localization:** Arabic (RTL) is designed as a native architectural layout with custom line-heights and tailored font sizes—never an auto-flipped mirror.
7. **Accessibility by Default (WCAG 2.1 AA):** High text contrast (minimum 4.5:1), visible focus indicators, readable type hierarchies, and full support for reduced-motion preferences.
8. **High Performance Framework:** Standardized image aspect ratios (`16:9`, `4:3`, `3:2`, `1:1`, `9:16`) to ensure zero Cumulative Layout Shift (CLS = 0) and predictable asset scaling.

---

## 3. Proposed Visual Direction `[PROPOSED]`

- **Aesthetic Identity:** Architectural Minimalist, Contemporary Editorial, Monograph-inspired.
- **Section Pacing:** Alternating rhythm between full-bleed photographic hero views, structured 3-column project grids, technical 2-column editorial splits, and generous white/light-grey breathing pauses (80px–120px desktop padding).
- **Surface Strategy:**
  - *Light Canvas (90% of experience):* Pure white (`#FFFFFF`) and warm off-white (`#F8F9FA`) allowing colorful interior photography to breathe.
  - *Dark Canvas (10% of experience):* Deep midnight navy (`#0E1B33`) reserved strictly for the Global Footer, video modal viewers, and high-impact CTA banners.

---

## 4. Provisional Color Tokens & Figma Styles

> [!WARNING]
> The color hex codes below are **provisional estimates** derived from the provided logo reference and are subject to client confirmation (`docs/05_open_questions.md#brand`). Designers must define these as **Figma Color Variables** so values can be updated globally in one click.

### Figma Variable Collection: `Colors`

| Token Name | Provisional Value | Figma Style Role | Contrast Ratio & Usage |
| :--- | :--- | :--- | :--- |
| `color/brand/primary` | `#203D73` | Core ERUM Navy | 7.9:1 on `#FFFFFF` (AAA). Used for primary headers, text emphasis, and primary buttons. |
| `color/brand/primary-dark` | `#0E1B33` | Midnight Navy | 13.8:1 on `#FFFFFF` (AAA). Used for footer background and dark hero surfaces. |
| `color/brand/primary-light`| `#F3F6FB` | Cool Architectural Tint | Subtle background for technical specifications and data tables. |
| `color/brand/accent` | `#F5A000` | Warm Gold Accent | 5.2:1 on Midnight Navy. Used for CTA buttons, play buttons, and active indicator bars. **Do not use for small text on white.** |
| `color/brand/accent-text` | `#B47100` | Darkened Accessible Gold | 4.6:1 on `#FFFFFF` (AA). Used specifically for gold text or category links on light backgrounds. |
| `color/background/primary` | `#FFFFFF` | Core Canvas | Crisp white background for cards, project pages, and main content. |
| `color/background/secondary`| `#F8F9FA` | Soft Off-White | Alternating section backgrounds. |
| `color/text/primary` | `#111827` | Slate Charcoal | Primary body copy and headings. Avoids harsh pure black. |
| `color/text/secondary` | `#4B5563` | Muted Gray | Metadata (Location, Area m², Dates, Field Labels). |
| `color/text/inverse-primary`| `#FFFFFF` | White on Dark | Text on midnight navy surfaces. |
| `color/text/inverse-secondary`| `#D1D5DB`| Light Gray on Dark | Subtitles on midnight navy surfaces. |
| `color/border/default` | `#E5E7EB` | Hairline Divider | Card borders, table dividers, input borders. |
| `color/border/focus` | `#F5A000` | Focus Ring | 2px accessible focus outline for keyboard navigation. |
| `color/feedback/error` | `#DC2626` | Error Red | Form validation error text and input outlines. |
| `color/feedback/success` | `#15803D` | Success Green | Form submission confirmations and verified badges. |

---

## 5. Typography Candidates & Pending Decisions

### Proposed Font Families `[PROPOSED CANDIDATES]`
- **Latin Sans:** `Plus Jakarta Sans` (Primary Recommendation) or `Outfit`
- **Arabic Sans:** `Alexandria` (Primary Recommendation) or `IBM Plex Sans Arabic`
- **Architectural Spec / Mono:** `SF Mono`, `Roboto Mono`, or `Consolas` (for project numbers and CAD dimensions)

### Typography Scale & Specs for Figma Text Styles

| Text Style Name | Latin Spec (Size / Line-Height) | Arabic Spec (Size / Line-Height) | Weight | Application |
| :--- | :--- | :--- | :--- | :--- |
| `Display` | `56px` / `64px` | `56px` / `72px` | Bold (700) | Homepage Hero Title |
| `Heading 1 (H1)` | `40px` / `48px` | `40px` / `56px` | Bold (700) | Primary Page Titles (Project Name, Service Title) |
| `Heading 2 (H2)` | `32px` / `40px` | `32px` / `46px` | SemiBold (600)| Major Section Headings |
| `Heading 3 (H3)` | `24px` / `32px` | `24px` / `36px` | SemiBold (600)| Card Titles, Accordion Headers |
| `Heading 4 (H4)` | `18px` / `26px` | `18px` / `28px` | Medium (500) | Subsection Headings, Form Group Titles |
| `Body Large` | `18px` / `28px` | `19px` / `32px` | Regular (400) | Article intros, lead paragraphs, manifesto |
| `Body Regular` | `16px` / `26px` | `16px` / `28px` | Regular (400) | Standard body copy, form inputs, descriptions |
| `Body Small` | `14px` / `22px` | `14px` / `24px` | Regular (400) | Metadata (Area, Location, Year, Captions) |
| `Caption / Overline`| `12px` / `16px` | `12px` / `18px` | Medium (500) | Badges, category tags, legal notices |

*Design Rule for Arabic:* Arabic scripts require approximately 15% more vertical line-height than Latin scripts to prevent character clashing on diacritics and tall ascenders/descenders.

---

## 6. Global Header and Footer Architecture

### 6.1 Global Desktop Header `[PROPOSED NAVIGATION - ALIGNED]`
- **Height:** `80px` fixed.
- **Background:** White (`#FFFFFF`) with subtle bottom border (`#E5E7EB`) or transparent over dark hero with automatic solid background on scroll (`backdrop-filter: blur(8px)`).
- **Navigation Alignment (5 Primary Links):**
  1. **Projects**
  2. **Services**
  3. **About**
  4. **Knowledge**
  5. **Contact**
- **Utility Group:**
  - Language Switcher Pill: Segmented toggle button (`AR` | `EN`).
  - Primary CTA Button: "Start Your Project" (Accent Gold `#F5A000` or Navy `#203D73`).
- **Placement Rationale:** Keeping top navigation to 5 primary links prevents cognitive overload and avoids horizontal wrapping on 1024px–1280px laptop screens. *Process* and *Meet The Engineer* are accessible via contextual page links and the global footer.

### 6.2 Global Mobile Header
- **Height:** `64px` sticky.
- **Elements:** Compact brand mark (height 32px), WhatsApp direct-action icon button (`44px × 44px` touch target), and hamburger menu trigger (`48px × 48px`).
- **Mobile Menu Drawer:** Full-screen sheet in Midnight Navy (`#0E1B33`) with large accessible links (`24px`), language toggle, phone, WhatsApp, and social channels.

### 6.3 Global Footer
- **Background:** Solid Midnight Navy (`#0E1B33`).
- **Structure:** 4-column layout on desktop; single-column stacked accordion on mobile:
  - *Column 1:* ERUM logo, positioning tagline, and Eng. Abdelrahman attribution.
  - *Column 2 (Projects):* Residential, Commercial, Administrative, Turnkey Execution.
  - *Column 3 (Services & Process):* Interior Design, Execution, Project Management, 12-Step Process link.
  - *Column 4 (Contact & Studio):* Official phone, WhatsApp, Beni Suef address, studio hours.
- **Bottom Bar:** Bilingual copyright statement, Privacy Policy, Terms, and social icons.

---

## 7. Required Pages & Prioritization Matrix

All 19 pages specified in `docs/design/03_page_wireframes.md` must be designed in Figma across **Desktop (1440px)** and **Mobile (390px)** viewports:

| Priority Tier | Page Name | Page Slug | Core Focus |
| :--- | :--- | :--- | :--- |
| **Tier 1 (Core)** | **Home** | `/` | Brand triad, flagship project proof, Render vs. Reality, Process overview, Founder authority, primary lead driver. |
| | **Projects Listing** | `/projects` | Filterable portfolio matrix (Type, Scope, Render vs. Reality toggle). |
| | **Project Details** | `/projects/[slug]` | Modular case study template with conditional gallery rendering. |
| | **Services Listing** | `/services` | 5 service pillars, deliverables matrix, and service FAQs. |
| | **Service Details** | `/services/[slug]` | Deep-dive scope, deliverables checklist, and pre-filtered related projects. |
| | **Start Your Project** | `/start-project` | 3-step lead onboarding form, budget tiers, and floorplan dropzone. |
| **Tier 2 (Authority)**| **Knowledge Hub** | `/knowledge` | Central content index, search bar, and "Engineer's Advice" carousel. |
| | **Article Details** | `/knowledge/[slug]` | Editorial finishing guide, author card, and related project proof. |
| | **Video Library** | `/videos` | Dual-format video grid (16:9 Landscape & 9:16 Vertical Reels). |
| | **Video Details** | `/videos/[slug]` | Responsive player, summary, transcript, and connected project CTA. |
| | **About ERUM** | `/about` | Studio manifesto, execution philosophy, and craftsmanship gallery. |
| | **Meet The Engineer** | `/about/engineer` | Eng. Abdelrahman personal brand, credentials, and advice videos. |
| | **Process** | `/process` | The 12-Step ERUM Standard across 4 execution phases. |
| | **Contact** | `/contact` | Phone, WhatsApp, Beni Suef location, Google Map embed, and contact form. |
| **Tier 3 (Utility)** | **Articles Listing** | `/knowledge/articles` | Filterable editorial articles repository. |
| | **Search Results** | `/search` | Multi-entity search tabs (Projects, Articles, Videos, Services). |
| | **404 Not Found** | `/404` | Architectural error recovery layout. |
| | **Privacy Policy** | `/privacy` | Legal policy and data protection terms. |
| | **Terms & Conditions**| `/terms` | Intellectual property and digital estimate disclaimers. |

---

## 8. Required Sections per Page (Figma Layout Blueprint)

```text
1. HOME
   ├── Header (Global)
   ├── Hero Section (Cinematic project hero + dual CTAs)
   ├── Selected Projects (3 flagship cards)
   ├── The ERUM Triad (Design Studio + Execution + Project Management)
   ├── Design → Reality (Interactive split comparison widget)
   ├── Process Preview (4-phase condensed timeline)
   ├── Featured Knowledge & Video Hub (1 hero video + 2 articles)
   ├── Meet The Engineer (Portrait + Engineering philosophy quote)
   ├── Testimonials (Verified client quote cards)
   ├── Final CTA Banner (Midnight navy background)
   └── Footer (Global)

2. PROJECTS LISTING
   ├── Header & Breadcrumbs
   ├── Title & Horizontal Filter Bar (Type, Scope, Render vs Reality toggle)
   ├── Project Grid (3-column desktop / 1-column mobile)
   ├── Pagination / Load More
   ├── Inquiries CTA Banner
   └── Footer

3. PROJECT DETAILS (Modular Case Study Template)
   ├── Header & Breadcrumbs
   ├── Project Hero & Metadata Bar (Name, Location, Area m², Scope, Year)
   ├── Design Concept & Spatial Solution
   ├── 3D Render Gallery (Conditional)
   ├── Site Construction Photos (Conditional)
   ├── Final Handover Photography
   ├── Before & After Slider (Conditional)
   ├── Render vs. Reality Widget (Conditional)
   ├── Architectural Floorplans (Conditional)
   ├── Project Walkthrough Video (Conditional)
   ├── Related Services & Related Projects
   ├── Contextual Project CTA ("Build a Space Like This")
   └── Footer

4. SERVICES LISTING
   ├── Header & Breadcrumbs
   ├── Page Title & Scope Intro
   ├── 5 Service Pillar Cards with Deliverable Chips
   ├── Quality & Supervision Standards Block
   ├── Service FAQs Accordion
   ├── Service Inquiry CTA
   └── Footer

5. SERVICE DETAILS
   ├── Header & Breadcrumbs
   ├── Service Hero & Direct Action CTA
   ├── Scope & Methodology
   ├── Deliverables Checklist
   ├── Step-by-Step Service Workflow
   ├── Filtered Projects Executed Under This Service (Top 3)
   ├── Related Knowledge Articles & Videos
   ├── Service Inquiry CTA (Pre-selected service tag)
   └── Footer

6. PROCESS (Design → Execution → Reality)
   ├── Header & Breadcrumbs
   ├── Process Philosophy Headline
   ├── 4-Phase Interactive Progress Navigator
   ├── Phase 1: Consultation & Site Survey (Steps 1–2)
   ├── Phase 2: Design & BOQ Costing (Steps 3–6)
   ├── Phase 3: Preparation & Procurement (Steps 7–8)
   ├── Phase 4: Execution & Handover (Steps 9–12)
   ├── Quality Control & Supervision Protocol Box
   ├── Process FAQs
   ├── Start Your Project CTA
   └── Footer

7. KNOWLEDGE HUB
   ├── Header & Breadcrumbs
   ├── Title & Predictive Search Bar
   ├── Category Filter Pills (Design, Finishing, BOQ, Advice)
   ├── Featured Knowledge Story (Hero card)
   ├── "Engineer's Advice" Video Carousel (Shorts & Walkthroughs)
   ├── Latest Articles Grid
   ├── Consultation Callout
   └── Footer

8. ARTICLE DETAILS
   ├── Header & Breadcrumbs
   ├── Article Header (Category, Title, Author: Eng. Abdelrahman, Date, Reading Time)
   ├── 16:9 Hero Image
   ├── Key Takeaways Callout Box
   ├── Rich Text Body (H2, H3, images, pull-quotes)
   ├── Proof Block ("How ERUM Executes This on Site")
   ├── Related Project Card
   ├── Author Bio Card
   ├── Share Bar & Related Articles
   ├── Contextual Lead CTA
   └── Footer

9. VIDEO LIBRARY
   ├── Header & Breadcrumbs
   ├── Title & Format Toggle (All, 16:9 Landscape, 9:16 Vertical Reels)
   ├── Topic Filter Chips
   ├── Featured Video of the Month
   ├── Responsive Video Grid
   ├── Video Inquiry CTA
   └── Footer

10. VIDEO DETAILS
    ├── Header & Breadcrumbs
    ├── Video Player Container (Cinema 16:9 or Smartphone 9:16)
    ├── Video Meta Block (Title, Category, Date)
    ├── Description & Takeaways Summary
    ├── Collapsible Transcript Accordion
    ├── Related Project Showcase
    ├── Up Next Videos Carousel
    ├── Contextual Consultation CTA
    └── Footer

11. START YOUR PROJECT (Lead Onboarding)
    ├── Header & Breadcrumbs
    ├── Title & Reassurance Subhead ("Tell Us About Your Space")
    ├── Trust Badges (Engineer Review, No Spam, Free Initial Call)
    ├── Step Progress Indicator (Step 1 of 3)
    ├── Step 1: The Space (Type, Location, Area m²)
    ├── Step 2: The Scope (Service, Current Status, Budget Tier)
    ├── Step 3: Contact & Plans (Name, Phone/WhatsApp, File Dropzone)
    ├── What Happens Next? (3-step timeline)
    ├── Direct WhatsApp Alternative Action
    └── Footer

12. ABOUT ERUM
    ├── Header & Breadcrumbs
    ├── Studio Manifesto
    ├── Founding Story & Engineering Philosophy
    ├── Core Value Pillars (Precision, Transparency, Material Quality)
    ├── Operational Reach & Areas Served (Beni Suef & Egypt)
    ├── On-Site Craftsmanship Photo Gallery
    ├── Lead CTA
    └── Footer

13. MEET THE ENGINEER
    ├── Header & Breadcrumbs
    ├── Founder Hero (Portrait, Name, Official Title)
    ├── Engineering Philosophy
    ├── Verified Credentials & Experience Highlights
    ├── Curated Advice Videos
    ├── Selected Projects Directed
    ├── Social Channels Touch Grid
    ├── Direct Consultation CTA
    └── Footer

14. CONTACT
    ├── Header & Breadcrumbs
    ├── Title & Direct Contact Prompt
    ├── Direct Channel Cards (Phone, WhatsApp, Email)
    ├── Studio Location & Opening Hours (Beni Suef)
    ├── Interactive Google Map Embed Frame
    ├── General Inquiries Form
    └── Footer

15. SEARCH RESULTS
    ├── Header & Search Query Bar
    ├── Entity Filter Tabs (All, Projects, Articles, Videos, Services)
    ├── Results Card Matrix
    ├── Empty State Recovery Block
    └── Footer

16. 404 NOT FOUND
    ├── Header
    ├── Architectural Blueprint Visual
    ├── Clear Recovery Message & Helpful Links
    ├── Search Input
    └── Footer

17. PRIVACY POLICY & 18. TERMS AND CONDITIONS
    ├── Header & Breadcrumbs
    ├── Legal Document Header & Date
    ├── Formatted Legal Content Body (Container max 680px)
    └── Footer
```

---

## 9. Reusable Component Inventory (Document Once)

Figma designers must build these components in a dedicated `❖ Components` frame with complete auto-layout and interactive variants:

### 1. Navigation Components
- `❖ Header / Desktop`: Auto-layout horizontal, logo, 5 navigation links, language switch, CTA button.
- `❖ Header / Mobile`: Auto-layout horizontal, logo, WhatsApp icon button, hamburger toggle.
- `❖ Mobile Drawer`: Full-screen overlay, vertical link stack, contact quick-links.
- `❖ Footer`: Auto-layout 4-column desktop / 1-column mobile accordion.
- `❖ Breadcrumb`: Horizontal auto-layout, home icon, chevron divider, active leaf label.

### 2. Cards
- `❖ Card / Project`: 
  - Image container (Aspect `4:3`, `overflow: hidden`, `radius.md`).
  - Badges top-start: Category Chip (`rgba(14, 27, 51, 0.85)`), optional "Render vs Reality" highlight.
  - Text block: Title (`H3`), secondary meta line (Location · Area m² · Scope).
  - Hover variant: Image scales to `1.03x`, card elevation shifts to `shadow.md`.
- `❖ Card / Service`:
  - Architectural icon / image vignette.
  - Service title (`H3`), 2-line summary paragraph.
  - Deliverable chips cluster.
  - "Learn More →" directional link.
- `❖ Card / Article`:
  - Cover image (Aspect `16:9`).
  - Category pill + reading time badge.
  - 2-line clamped title (`H4`), excerpt, date.
- `❖ Card / Video`:
  - Thumbnail (Aspect `16:9` Landscape or `9:16` Reel).
  - Play button overlay (`48px` diameter, gold circle, navy play icon).
  - Duration pill bottom-end (`04:15`).
  - Title & topic chips.

### 3. Interactive Widgets
- `❖ Widget / RenderVsReality`: Interactive split container with center drag handle and "Render" / "Reality" label pills. Mobile variant includes tap-to-flip toggle.
- `❖ Widget / BeforeAfterSlider`: Dual-image container with horizontal drag divider.
- `❖ Player / VideoModal`: 16:9 video player with dismiss trigger (`✕`) and blurred midnight navy scrim.

### 4. Form Elements
- `❖ Input / Text & Tel`: `48px` height, label above, optional prefix (e.g. `+20`), placeholder, error text state.
- `❖ Input / Select`: `48px` height, dropdown chevron, native select styling.
- `❖ Input / Textarea`: Min height `120px`, resize handle disabled.
- `❖ Pill / SegmentedControl`: Radio toggle chips for Service Type and Budget Ranges (`44px` touch height; selected state = solid navy background).
- `❖ Dropzone / FileUpload`: Dashed border (`2px dashed #E5E7EB`), blueprint icon, drag-and-drop prompt, max 25MB label.

### 5. Buttons & Controls
- `❖ Button / Primary (Navy)`: Background `#203D73`, text `#FFFFFF`, radius `6px`.
- `❖ Button / Accent (Gold CTA)`: Background `#F5A000`, text `#0E1B33`, radius `6px`.
- `❖ Button / Secondary (Outline)`: Transparent, border `1px solid #203D73`, text `#203D73`.
- `❖ Button / Ghost`: Transparent, text `#203D73`, subtle background on hover.
- `❖ Filter / Chip`: Rounded pill tag (`radius.full`), active variant with navy fill and white text.

---

## 10. Viewport & Breakpoint Specifications

Design frames must be constructed using Figma Auto-Layout at these exact dimensions:

| Viewport | Frame Width | Margin | Gutter | Columns | Notes |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **Desktop (Primary)** | `1440px` | `32px` | `32px` | 12 columns | Standard presentation canvas. |
| **Tablet (Responsive)** | `834px` | `24px` | `24px` | 8 columns | iPad / tablet portrait reference. |
| **Mobile (Primary)** | `390px` | `16px` | `16px` | 4 columns | iPhone 14/15/16 baseline. Single-column cards. |

---

## 11. Arabic RTL and English LTR Requirements

Every component and template must have a corresponding **Arabic RTL** variant in Figma:

1. **Horizontal Flipping:** Navigation order, card layouts, bullet points, and breadcrumbs mirror horizontally (`Start` ↔ `End`).
2. **Directional Iconography:** Directional arrows (`→` becomes `←`) flip direction; universal glyphs (play icon, search magnifying glass, social icons, checkmarks) do **not** flip.
3. **Telecommunications Formats:** Phone numbers, WhatsApp numbers, and country codes (`+20 1X...`) must remain strictly LTR in both languages.
4. **Typographic Proportions:** Set Arabic text using the Arabic typography styles defined in [Section 5](#5-typography-candidates--pending-decisions).

---

## 12. Accessibility Requirements for Figma Files

- **Contrast Ratios:** All text styles must pass WCAG 2.1 AA (4.5:1 for body copy; 3:1 for large display titles).
- **Focus Rings:** Every interactive button and form field must include a visible `:focus-visible` variant with a `2px solid #F5A000` ring offset by `2px`.
- **Text Layers:** No text may be baked directly into flat raster image files. All headings, captions, and badges must remain live, editable text layers.

---

## 13. Component Interaction States

Every interactive component must declare 5 states in Figma component sets:
1. **Default**
2. **Hover** (Desktop cursor)
3. **Focus-visible** (Keyboard navigation ring)
4. **Active / Pressed** (Click feedback)
5. **Disabled** (Muted `#E5E7EB` background, cursor not-allowed)

---

## 14. Required Project & Brand Assets Checklist

The following client assets are required before final design sign-off (`docs/04_asset_checklist.md`):

- [ ] **Vector Logo Files:** Official `.SVG` or `.AI` vector files (Monogram mark, horizontal lockup, dark and light versions).
- [ ] **Verified Brand Colors:** Official CMYK / Hex codes confirming or replacing provisional `#203D73` and `#F5A000`.
- [ ] **Top 3 Flagship Projects:** High-res photography folders (Render, Construction, Final, Before/After).
- [ ] **Founder Portrait & Bio:** Professional studio/site portrait of Eng. Abdelrahman and verified biography copy.
- [ ] **Official Contact Data:** Single confirmed phone number, WhatsApp number, and physical studio address in Beni Suef.

---

## 15. Temporary Content & Placeholder Guidelines

Until official client assets are delivered, Figma designers must observe these strict placeholder rules:

- **No Lorem Ipsum:** Use realistic architectural placeholder copy (e.g. *"Villa Al-Noor — Modern Residential Finishing in Beni Suef"* instead of *"Lorem ipsum dolor sit amet"*).
- **No Stock Mansions:** If real project photos are unavailable for secondary cards, use monochromatic architectural wireframe renders with a clear watermark: `[TEMPORARY PLACEHOLDER — ERUM PROJECT ASSET PENDING]`.
- **Do Not Invent Credentials:** State `[Degree / Certification Pending Client Confirmation]` rather than inventing universities or accolades.

---

## 16. Client Decisions Required Before Final UI Approval

| Decision ID | Item | Current Status | Impact on Figma Design |
| :--- | :--- | :--- | :--- |
| **CD-01** | **Brand Color Confirmation** | `[PENDING CLIENT CONFIRMATION]` | Verification of navy and gold hex codes. |
| **CD-02** | **Arabic Brand Name** | `[PENDING CLIENT CONFIRMATION]` | Exact Arabic spelling for header lockup ("إي روم" vs. "إرم"). |
| **CD-03** | **Font Family Approval** | `[PROPOSED CANDIDATE]` | Sign-off on Plus Jakarta Sans + Alexandria. |
| **CD-04** | **Lead Form Step Model** | `[PROPOSED: 3-STEP WIZARD]` | Single-page vs. multi-step form design. |
| **CD-05** | **Numeral Format in Arabic** | `[PENDING CLIENT CONFIRMATION]` | Western (1, 2, 3) vs. Eastern Arabic (١، ٢، ٣) numerals for areas/dimensions. |

---

## 17. Recommended Figma Design Sequence (Phase 3 Workflow)

Figma design must follow this strict 11-step sequence to avoid redundant redesign work:

```text
Step 01: Design Foundations (Color variables, typography styles, spacing grid, elevation)
   ↓
Step 02: Shared Component Library (Header, footer, cards, form inputs, buttons, widgets)
   ↓
Step 03: Homepage (Desktop & Mobile, establishing the core brand atmosphere)
   ↓
Step 04: Projects Listing & Project Details (Modular case study template)
   ↓
Step 05: Services Listing & Service Details
   ↓
Step 06: Knowledge Hub, Article Details, Video Library & Video Details
   ↓
Step 07: Lead Generation ("Start Your Project") & Contact Page
   ↓
Step 08: Remaining Pages (About, Meet The Engineer, Process, Search, 404, Legal)
   ↓
Step 09: Responsive Layouts (Tablet 834px & Mobile 390px edge cases)
   ↓
Step 10: Full Arabic (RTL) Layout Review (Typography balance & alignment symmetry)
   ↓
Step 11: Final Design QA & Client Sign-off (Replacing placeholders with real assets)
```

---

## 18. Handoff Requirements for Future Frontend Development

When the Figma designs are approved and ready for frontend implementation:
1. **Figma Dev Mode Annotations:** Every component must have explicit auto-layout constraints, padding tokens, and gap measurements.
2. **Variable Token Mapping:** Figma variables must map 1:1 to CSS Custom Properties (`--color-brand-primary`, `--spacing-4`, `--radius-md`).
3. **Asset Export Readiness:** All icons must be exported as clean, optimized SVGs with `currentColor` fills where applicable.
4. **Responsive Behavior Specs:** Breakpoint behavior (stacking order, font size clamping, hide/show rules) must be explicitly noted in Figma sticky notes.
