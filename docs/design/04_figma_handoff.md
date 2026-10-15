# ERUM Interior Studio — Figma Design Handoff & UI Specification

> **Document Status:** Provisional Figma UI Design & Handoff — client validation and asset approval pending.  
> **Figma file:** [ERUM Interior Studio — Phase 1 Design Foundations](https://www.figma.com/design/wcFiQnpI3crusgQPKJgPDB/ERUM-Interior-Studio-%E2%80%94-Phase-1-Design-Foundations?node-id=2013-1568)  
> **Repo:** https://github.com/MooAli49/erum_interior_studio  
> **Target Audience:** UI/UX Designers, Figma Design Leads, Creative Directors, and Frontend Engineers  
> **Classification Key:**  
> - `[CONFIRMED]`: Established requirement or verified project constraint.  
> - `[PROPOSED]`: Design decision, layout recommendation, or token proposed for client review.  
> - `[PENDING CLIENT CONFIRMATION]`: Open parameter awaiting client validation or asset delivery.  
> - `[IN FIGMA]`: Verified on the live Figma canvas.  
> - `[NOT YET IN FIGMA]`: Specification exists in docs; native editable frame has not yet been built.

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
5. **Mobile-First Primacy:** Mobile traffic represents a primary client acquisition channel due to social media discovery (TikTok, Instagram, Facebook). Mobile screens require zero horizontal overflow, 44px+ touch targets, and sticky direct consultation triggers `[CONFIRMED DESIGN PRIORITY]`.
6. **Intentional Symmetrical Localization:** Arabic (RTL) is designed as a native architectural layout with custom line-heights and tailored font sizes—never an auto-flipped mirror.
7. **Accessibility by Default (WCAG 2.1 AA):** High text contrast (minimum 4.5:1), visible focus indicators, readable type hierarchies, and full support for reduced-motion preferences.
8. **High Performance Framework:** Standardized image aspect ratios (`16:9`, `4:3`, `3:2`, `1:1`, `9:16`) to target a Cumulative Layout Shift (CLS) of less than 0.1 in accordance with Core Web Vitals standards, supported by responsive image testing across devices.

---

## 3. Existing Figma Canvas State & Handoff Boundaries

To avoid ambiguity between specification and implementation, the current state of the live Figma file is:

### Existing Verified Figma Pages `[IN FIGMA]`
- `01 — Foundations` `[IN FIGMA]` (Node `#0:1`) — Design tokens (color variables, typography styles, elevation, grids). Frame: `01 — Foundations` (Node `#2004:28205`).
- `02 — Components` `[IN FIGMA]` (Node `#2004:31535`) — Component definitions (headers, footers, card patterns, inputs, buttons). Frame: `02 — Components` (Node `#2004:28912`); Section: `ERUM — Native component definitions` (Node `#2004:31536`).
- `03 — Homepage` `[IN FIGMA]` (Node `#2013:1568`) — Includes five verified frames:
  - `Home / EN / Desktop` (Node `#2013:20544`, width: 1440px)
  - `Home / EN / Mobile` (Node `#2013:20950`, width: 390px)
  - `Home / AR / Desktop` (Node `#2013:21402`, width: 1440px, native RTL)
  - `Home / AR / Mobile` (Node `#2013:21927`, width: 390px, native RTL)
  - `Homepage / Handoff & approvals` (Node `#2013:22432`, width: 560px handoff notes frame)
- `04 — Projects Listing (Provisional)` `[IN FIGMA]` (Node `#2048:6640`) — Includes four verified frames:
  - `Projects Listing / EN / Desktop` (Node `#2048:5503`, width: 1440px)
  - `Projects Listing / AR / Desktop` (Node `#2048:5718`, width: 1440px, native RTL)
  - `Projects Listing / EN / Mobile` (Node `#2048:6105`, width: 390px)
  - `Projects Listing / AR / Mobile` (Node `#2048:6332`, width: 390px, native RTL)
  - Detailed companion specification: [Projects Listing Figma Handoff](05_projects_listing_handoff.md).

### Next Intended Design Page `[PROPOSED]` / `[NOT YET IN FIGMA]`
- `05 — Project Details & Case Study Template (Provisional)` `[NOT YET IN FIGMA]` (Page 3 in Wireframe Architecture; proposed route: `/projects/[slug]` — proposed route only, not a confirmed implementation).
  - Do not claim that this page or any subsequent page has already been built until verified on the live Figma canvas.

---

## 4. Proposed Visual Direction `[PROPOSED]`

- **Aesthetic Identity:** Architectural Minimalist, Contemporary Editorial, Monograph-inspired.
- **Section Pacing:** Alternating rhythm between full-bleed photographic hero views, structured 3-column project grids, technical 2-column editorial splits, and generous white/light-grey breathing pauses (80px–120px desktop padding).
- **Surface Strategy:**
  - *Light Canvas (90% of experience):* Pure white (`#FFFFFF`) and warm off-white (`#F8F9FA`) allowing colorful interior photography to breathe.
  - *Dark Canvas (10% of experience):* Deep midnight navy (`#0E1B33`) reserved strictly for the Global Footer, video modal viewers, and high-impact CTA banners.

---

## 5. Provisional Color Tokens & Figma Styles

> [!WARNING]
> The color hex codes below are **provisional estimates** derived from the provided logo reference and are subject to client confirmation (`docs/05_open_questions.md#brand`). Designers must define these as **Figma Color Variables** so values can be updated globally in one click. Detailed semantic token architecture is specified in [Design System Specification](02_design_system.md#3-color-tokens).

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

## 6. Typography Candidates & Pending Decisions

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

## 7. Global Header and Footer Architecture

### 7.1 Global Desktop Header `[PROPOSED NAVIGATION - ALIGNED]`
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

### 7.2 Global Mobile Header
- **Height:** `64px` sticky.
- **Elements:** Compact brand mark (height 32px), WhatsApp direct-action icon button (`44px × 44px` touch target), and hamburger menu trigger (`48px × 48px`).
- **Mobile Menu Drawer:** Full-screen sheet in Midnight Navy (`#0E1B33`) with large accessible links (`24px`), language toggle, phone, WhatsApp, and social channels.

### 7.3 Global Footer
- **Background:** Solid Midnight Navy (`#0E1B33`).
- **Structure:** 4-column layout on desktop; single-column stacked accordion on mobile:
  - *Column 1:* ERUM logo, positioning tagline, and Eng. Abdelrahman attribution.
  - *Column 2 (Projects):* Residential, Commercial, Administrative, Turnkey Execution.
  - *Column 3 (Services & Process):* Interior Design, Execution, Project Management, 12-Step Process link.
  - *Column 4 (Contact & Studio):* Official phone, WhatsApp, Beni Suef address, studio hours.
- **Bottom Bar:** Bilingual copyright statement, Privacy Policy, Terms, and social icons.

---

## 8. Required Pages & Prioritization Matrix

All 19 pages specified in [Wireframes & Page Structure](03_page_wireframes.md) must be designed in Figma across **Desktop (1440px)** and **Mobile (390px)** viewports:

| # | Priority Tier | Page Name | Page Slug | Core Focus | Current Figma Status |
| :- | :--- | :--- | :--- | :--- | :--- |
| 1 | **Tier 1 (Core)** | **Home** | `/` | Brand triad, flagship project proof, Render vs. Reality, Process overview, Founder authority, primary lead driver. | `[CONFIRMED SCOPE / IN FIGMA]` |
| 2 | | **Projects Listing** | `/projects` | Filterable portfolio matrix (Type, Scope, Render vs. Reality toggle). | `[CONFIRMED SCOPE / PROVISIONAL DESIGN - IN FIGMA]` |
| 3 | | **Project Details & Case Study Template** | `/projects/[slug]` *(proposed route)* | Modular case study template with conditional gallery rendering. | `[CONFIRMED SCOPE / NOT YET IN FIGMA]` |
| 4 | | **Services Listing** | `/services` | Service discipline showcase (Design, Execution, Project Management [CONFIRMED]; Specific service packages [PROPOSED]). | `[PENDING CONFIRMATION / NOT YET IN FIGMA]` |
| 5 | | **Service Details** | `/services/[slug]` | Deep-dive scope, deliverables checklist, and pre-filtered related projects. | `[PROPOSED TEMPLATE / NOT YET IN FIGMA]` |
| 6 | | **Start Your Project** | `/start-project` | 3-step lead onboarding form, budget tiers, and configurable floorplan dropzone. | `[PROPOSED WIZARD / NOT YET IN FIGMA]` |
| 7 | **Tier 2 (Authority)**| **Knowledge Hub** | `/knowledge` | Central multimedia content index, predictive search, and "Engineer's Advice" carousel. | `[CONFIRMED SCOPE / NOT YET IN FIGMA]` |
| 8 | | **Articles Listing** | `/knowledge/articles` | Dedicated editorial articles archive and finishing guide repository. | `[CONFIRMED SCOPE / NOT YET IN FIGMA]` |
| 9 | | **Article Details** | `/knowledge/[slug]` | Editorial finishing guide, author card, and related project proof. | `[CONFIRMED SCOPE / NOT YET IN FIGMA]` |
| 10 | | **Video Library** | `/videos` | Dual-format video grid (16:9 Landscape & 9:16 Vertical Reels). | `[CONFIRMED SCOPE / NOT YET IN FIGMA]` |
| 11 | | **Video Details** | `/videos/[slug]` | Responsive player, summary, transcript, and connected project CTA. | `[CONFIRMED SCOPE / NOT YET IN FIGMA]` |
| 12 | | **About ERUM** | `/about` | Studio manifesto, execution philosophy, and craftsmanship gallery. | `[CONFIRMED SCOPE / NOT YET IN FIGMA]` |
| 13 | | **Meet The Engineer** | `/about/engineer` | Eng. Abdelrahman personal brand, credentials, and advice videos. | `[CONFIRMED SCOPE / NOT YET IN FIGMA]` |
| 14 | | **Process** | `/process` | The 12-Step ERUM Standard across 4 execution phases. | `[CONFIRMED SCOPE / NOT YET IN FIGMA]` |
| 15 | | **Contact** | `/contact` | Phone, WhatsApp, Beni Suef location, Google Map embed, and contact form. | `[CONFIRMED SCOPE / NOT YET IN FIGMA]` |
| 16 | **Tier 3 (Utility)** | **Search Results** | `/search` | Multi-entity search tabs (Projects, Articles, Videos, Services). | `[CONFIRMED SCOPE / NOT YET IN FIGMA]` |
| 17 | | **404 Not Found** | `/404` | Architectural error recovery layout. | `[CONFIRMED SCOPE / NOT YET IN FIGMA]` |
| 18 | | **Privacy Policy** | `/privacy` | Legal policy and data protection terms. | `[CONFIRMED SCOPE / NOT YET IN FIGMA]` |
| 19 | | **Terms & Conditions**| `/terms` | Intellectual property and digital estimate disclaimers. | `[CONFIRMED SCOPE / NOT YET IN FIGMA]` |

### Knowledge & Content Hub Architecture Distinction
To avoid design ambiguity across the content platform, designers must distinguish between the three distinct knowledge views:
- **Knowledge Hub (`/knowledge`):** The primary multimedia gateway combining multi-format discovery: featured editorial hero, predictive search, category pills, latest articles, and the "Engineer's Advice" video carousel.
- **Articles Listing (`/knowledge/articles`):** The dedicated written archive and magazine view focused purely on long-form guides, technical finishing breakdowns, and written advice, equipped with topic filters and pagination.
- **Article Details (`/knowledge/[slug]`):** The single article reader view optimized for distraction-free reading, inline architectural diagrams, author credentials, related project proof, and contextual lead generation.

---

## 9. Required Sections per Page (Figma Layout Blueprint)

```text
1. HOME [IN FIGMA]
   ├── Header (Global)
   ├── Hero Section (Cinematic project hero + dual CTAs)
   ├── Selected Projects (3 flagship cards)
   ├── The ERUM Triad (Design Studio + Execution + Project Management)
   ├── Design → Reality (Interactive split comparison widget)
   ├── Process Preview (4-phase condensed timeline)
   ├── Featured Knowledge & Video Hub (1 hero video + 2 articles)
   ├── Meet The Engineer (Portrait + Engineering philosophy quote)
   ├── Testimonials (Verified client quote cards [PENDING CLIENT CONFIRMATION])
   ├── Final CTA Banner (Midnight navy background)
   └── Footer (Global)

2. PROJECTS LISTING [PROVISIONAL DESIGN - IN FIGMA]
   ├── Header & Breadcrumbs
   ├── Title & Horizontal Filter Bar (Type, Scope, Render vs Reality toggle)
   ├── Project Grid (3-column desktop / 1-column mobile)
   ├── Pagination / Load More
   ├── Inquiries CTA Banner
   └── Footer

3. PROJECT DETAILS & CASE STUDY TEMPLATE [PROPOSED / NOT YET IN FIGMA] (Modular Case Study Template — Proposed Route: /projects/[slug])
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
   ├── Service Pillar Cards with Deliverable Chips (Core Disciplines [CONFIRMED]; Specific Packages [PROPOSED])
   ├── Quality & Supervision Standards Block [PROPOSED FRAMEWORK]
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

8. ARTICLES LISTING (Dedicated Article Archive)
   ├── Header & Breadcrumbs (Home > Knowledge Hub > Articles)
   ├── Archive Header & Descriptive Intro
   ├── Topic Filter Chips (All, Interior Design, Finishing, BOQ, Materials)
   ├── Featured Editorial Guide (Optional hero card)
   ├── Article Card Grid (3-col desktop / 1-col mobile)
   ├── Pagination / Load More Controls
   ├── Related Project Proof Banner
   ├── Contextual Lead Generation CTA
   └── Footer

9. ARTICLE DETAILS
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

10. VIDEO LIBRARY
    ├── Header & Breadcrumbs
    ├── Title & Format Toggle (All, 16:9 Landscape, 9:16 Vertical Reels)
    ├── Topic Filter Chips
    ├── Featured Video of the Month
    ├── Responsive Video Grid
    ├── Video Inquiry CTA
    └── Footer

11. VIDEO DETAILS
    ├── Header & Breadcrumbs
    ├── Video Player Container (Cinema 16:9 or Smartphone 9:16)
    ├── Video Meta Block (Title, Category, Date)
    ├── Description & Takeaways Summary
    ├── Collapsible Transcript Accordion
    ├── Related Project Showcase
    ├── Up Next Videos Carousel
    ├── Contextual Consultation CTA
    └── Footer

12. ABOUT ERUM
    ├── Header & Breadcrumbs
    ├── Studio Manifesto [PROPOSED COPY]
    ├── Founding Story & Engineering Philosophy [PENDING CONFIRMATION]
    ├── Core Value Pillars (Precision, Transparency, Material Quality)
    ├── Operational Reach & Areas Served (Beni Suef [CONFIRMED]; Greater Cairo [PENDING CONFIRMATION])
    ├── On-Site Craftsmanship Photo Gallery
    ├── Lead CTA
    └── Footer

13. MEET THE ENGINEER
    ├── Header & Breadcrumbs
    ├── Founder Hero (Portrait, Name, Official Title)
    ├── Engineering Philosophy
    ├── Verified Credentials & Experience Highlights [PENDING CONFIRMATION]
    ├── Curated Advice Videos
    ├── Selected Projects Directed
    ├── Social Channels Touch Grid
    ├── Direct Consultation CTA
    └── Footer

14. START YOUR PROJECT (Lead Onboarding)
    ├── Header & Breadcrumbs
    ├── Title & Reassurance Subhead ("Tell Us About Your Space")
    ├── Trust Badges (e.g., Direct Engineer Review, Privacy Assurance, Consultation Call) [PROPOSED EXAMPLES]
    ├── Step Progress Indicator (Step 1 of 3)
    ├── Step 1: The Space (Type, Location, Area m²)
    ├── Step 2: The Scope (Service, Current Status, Budget Tier)
    ├── Step 3: Contact & Plans (Name, Phone/WhatsApp, File Dropzone [Configurable limit])
    ├── What Happens Next? (3-step timeline)
    ├── Direct WhatsApp Alternative Action
    └── Footer

15. CONTACT
    ├── Header & Breadcrumbs
    ├── Title & Direct Contact Prompt
    ├── Direct Channel Cards (Phone, WhatsApp, Email)
    ├── Studio Location & Opening Hours (Beni Suef)
    ├── Interactive Google Map Embed Frame
    ├── General Inquiries Form
    └── Footer

16. SEARCH RESULTS
    ├── Header & Search Query Bar
    ├── Entity Filter Tabs (All, Projects, Articles, Videos, Services)
    ├── Results Card Matrix
    ├── Empty State Recovery Block
    └── Footer

17. 404 NOT FOUND
    ├── Header
    ├── Architectural Blueprint Visual
    ├── Clear Recovery Message & Helpful Links
    ├── Search Input
    └── Footer

18. PRIVACY POLICY
    ├── Header & Breadcrumbs
    ├── Legal Document Header & Last Updated Date
    ├── Data Collection, Usage, and Floorplan Confidentiality Terms
    └── Footer

19. TERMS AND CONDITIONS
    ├── Header & Breadcrumbs
    ├── Document Header & Last Updated Date
    ├── Intellectual Property Protection & Estimate Disclaimers
    └── Footer
```

### 9.1 Dedicated Blueprint: Articles Listing (`/knowledge/articles`)

* **Page Objective:** Provide an organized, searchable, and authoritative archive of all ERUM written finishing guides, material comparisons, space-planning principles, and engineering advice.
* **Target Visitor Intent:** Long-form reader, researcher, or prospective client looking for deep-dive technical guidance on finishing their property in Egypt (e.g., porcelain vs. marble, plumbing inspection checklists, gypsum board mistakes).
* **Section Breakdown & Content Hierarchy:**
  1. **Header & Breadcrumbs:** Global Header + Breadcrumb trail (`Home > Knowledge Hub > Articles`).
  2. **Page Title & Intro Block:**
     - Title: `H1` (*"Finishing & Architectural Guides"*).
     - Subhead: Editorial introduction framing ERUM's commitment to transparent engineering knowledge.
     - Integrated Search Bar: Live predictive search filtering articles by keyword.
  3. **Topic & Category Filters:**
     - Horizontal pill chips allowing instant filtering: *All Guides*, *Interior Design*, *Finishing & Utilities* (Plumbing, Electrical, Gypsum), *Project Management & BOQ*, *Materials & Sourcing*.
  4. **Featured Article Hero (Optional):**
     - Prominent large editorial card highlighting a timely or foundational guide (e.g., *"The Complete Turnkey Finishing Checklist for Residential Villas"*).
     - Displays cover photo (16:9), category pill, reading time (`6 min read`), full headline, excerpt, and "Read Guide →" button.
     - *Conditional Rule:* If no article is marked as featured, the standard card grid seamlessly occupies this space without empty gaps.
  5. **Article Card Grid:**
     - 3-column grid on desktop (1440px), 2-column on tablet (834px), single-column stack on mobile (390px).
     - Card Anatomy (`❖ Card / Article`):
       - Cover image: Aspect ratio `16:9`, `overflow: hidden`, `radius.md`.
       - Badges: Category pill (`brand.gold.100` background with `brand.gold.700` text) + reading time badge (`14px`, muted text).
       - Title: `font.size.h4` (`18px`), SemiBold, max 2-line clamp to enforce uniform row heights.
       - Excerpt: 2-line clamped summary paragraph.
       - Footer: Publication date (`font.size.body-sm`, muted) and subtle directional arrow.
  6. **Pagination / Load More Controls:**
     - Desktop: Accessible numbered pagination (`← Previous  1  2  3  Next →`) with active state (`brand.navy.700` fill).
     - Mobile: "Load More Articles" button to reduce tapping friction on touchscreens.
  7. **Related Projects & Proof Callout:**
     - Full-width callout strip connecting theory to practice: *"Every guide we write is based on real site execution. Explore our completed projects to see these standards in reality."* with direct link to Portfolio.
  8. **Contextual Lead Generation CTA Banner:**
     - Midnight navy surface (`#0E1B33`) prompting inquiries: *"Have a specific finishing or design question about your property? Speak directly with our engineering team."* with button to `/start-project`.
  9. **Footer:** Global Footer.
* **Desktop & Mobile Behavior:**
  - *Desktop (1440px):* 3-column card grid with `32px` gutters; category chips aligned horizontally with active indicator.
  - *Mobile (390px):* Single-column full-width cards; category chips pan horizontally with touch scrolling (`overflow-x: auto; scrollbar-width: none;`); search bar occupies full width.
* **Arabic (RTL) & English (LTR) Requirements:**
  - Directional symmetry preserved; category chips anchor to inline-start edge; reading time badge positions to the inline-end edge; card arrows flip direction (`←` in Arabic, `→` in English).
* **Accessibility Requirements:**
  - Semantic `<main>` landmark with internal `<article>` tags for each card; search input has clear `<label>` and ARIA search role; pagination controls implement `aria-current="page"` and `aria-label="Pagination"`.
* **Required Content & Assets:**
  - Initial launch inventory of approved article drafts, high-resolution 16:9 photography for covers, confirmed author attribution to Eng. Abdelrahman Abdelrazek.
* **Dynamic Content Requirements:**
  - Live query against CMS `articles` collection; URL parameters update dynamically upon category selection (e.g., `?category=finishing`) to allow direct bookmarking and SEO indexing.
* **Open Decisions:**
  - Final client confirmation on initial launch article count and decision between numbered pagination versus infinite scroll (tracked in `docs/05_open_questions.md`).

---

## 10. Reusable Component Inventory (Document Once)

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
- `❖ Dropzone / FileUpload`: Dashed border (`2px dashed #E5E7EB`), blueprint icon, drag-and-drop prompt, configurable max file size label (proposed initial limit: 25MB, pending technical and client decisions) `[PROPOSED CONFIGURATION]`.

### 5. Buttons & Controls
- `❖ Button / Primary (Navy)`: Background `#203D73`, text `#FFFFFF`, radius `6px`.
- `❖ Button / Accent (Gold CTA)`: Background `#F5A000`, text `#0E1B33`, radius `6px`.
- `❖ Button / Secondary (Outline)`: Transparent, border `1px solid #203D73`, text `#203D73`.
- `❖ Button / Ghost`: Transparent, text `#203D73`, subtle background on hover.
- `❖ Filter / Chip`: Rounded pill tag (`radius.full`), active variant with navy fill and white text.

---

## 11. Viewport & Breakpoint Specifications

Design frames must be constructed using Figma Auto-Layout at these exact dimensions:

| Viewport | Frame Width | Margin | Gutter | Columns | Notes |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **Desktop (Primary)** | `1440px` | `32px` | `32px` | 12 columns | Standard presentation canvas. |
| **Tablet (Responsive)** | `834px` | `24px` | `24px` | 8 columns | iPad / tablet portrait reference. |
| **Mobile (Primary)** | `390px` | `16px` | `16px` | 4 columns | iPhone 14/15/16 baseline. Single-column cards. |

---

## 12. Arabic RTL and English LTR Requirements

Every component and template must have a corresponding **Arabic RTL** variant in Figma:

1. **Horizontal Flipping:** Navigation order, card layouts, bullet points, and breadcrumbs mirror horizontally (`Start` ↔ `End`).
2. **Directional Iconography:** Directional arrows (`→` becomes `←`) flip direction; universal glyphs (play icon, search magnifying glass, social icons, checkmarks) do **not** flip.
3. **Telecommunications Formats:** Phone numbers, WhatsApp numbers, and country codes (`+20 1X...`) must remain strictly LTR in both languages.
4. **Typographic Proportions:** Set Arabic text using the Arabic typography styles defined in [Section 6](#6-typography-candidates--pending-decisions).

---

## 13. Accessibility Requirements for Figma Files

- **Contrast Ratios:** All text styles must pass WCAG 2.1 AA (4.5:1 for body copy; 3:1 for large display titles). Use `#B47100` or `#203D73` for text on white; reserve bright gold `#F5A000` for accents and dark navy backgrounds.
- **Focus Rings:** Every interactive button and form field must include a visible `:focus-visible` variant with a `2px solid #F5A000` ring offset by `2px`.
- **Text Layers:** No text may be baked directly into flat raster image files. All headings, captions, and badges must remain live, editable text layers.

---

## 14. Component Interaction States

Every interactive component must declare 5 states in Figma component sets:
1. **Default**
2. **Hover** (Desktop cursor)
3. **Focus-visible** (Keyboard navigation ring)
4. **Active / Pressed** (Click feedback)
5. **Disabled** (Muted `#E5E7EB` background, cursor not-allowed)

---

## 15. Asset Status & Verification Guardrails

The canonical asset status checklist and working 10-folder inventory are maintained centrally in [Asset Checklist](../04_asset_checklist.md). To avoid duplicating the inventory table across documents, key asset handling guardrails for Figma are:

1. **Source Archive Status:** 309 JPG images across 10 folders have been received and cataloged into working review aids (`erum_image_inventory.csv`, `erum_commercial_shortlist_v2_reviewed.csv`, and contact sheets). These are internal review aids, not approved content.
2. **Internal Candidate IDs:** Labels such as `RES-CAND-01` and `COM-CAND-01` are internal review tags, not confirmed project titles. Never invent project names or deduce project identities from folder names.
3. **Verification Before Publishing:** Before any asset is marked approved or used as a non-placeholder cover:
   - Confirm image-to-project grouping and official project name.
   - Confirm status: render, construction photo, completed-space photo, moodboard, or plan.
   - Confirm ERUM's exact scope (design, execution, project management).
   - Confirm client publication permission for photos, floor plans, and visible individuals.
   - Check full-resolution sharpness, crop, and logo placement.
4. **Watermarks & Logos:** Visible ERUM marks in some supplied photos are the client's logo (confirmed by maintainer). This does not by itself confirm publication rights or turnkey execution.
5. **No Blind Imports:** Do not import all 309 raw images into Figma. Use editable neutral placeholders until assets are selected, cleared, and web-optimized.

---

## 16. Temporary Content & Placeholder Guidelines

Until official client assets are delivered, Figma designers must observe these strict placeholder rules:

- **No Lorem Ipsum:** Use realistic architectural placeholder copy (e.g. *"Villa Al-Noor — Modern Residential Finishing in Beni Suef"* instead of *"Lorem ipsum dolor sit amet"*).
- **No Stock Mansions:** If real project photos are unavailable for secondary cards, use monochromatic architectural wireframe renders with a clear watermark: `[TEMPORARY PLACEHOLDER — ERUM PROJECT ASSET PENDING]`.
- **Do Not Invent Credentials:** State `[Degree / Certification Pending Client Confirmation]` rather than inventing universities or accolades.
- **Editable Labels:** Placeholders must be editable native layers labelled as provisional.

---

## 17. Client Decisions Required Before Final UI Approval

All unresolved client decisions are centrally registered and tracked in [Open Questions & Decisions](../05_open_questions.md). The key decisions impacting current and upcoming Figma design frames are:

| Decision ID | Item | Current Status | Impact on Figma Design | Canonical Tracker |
| :--- | :--- | :--- | :--- | :--- |
| **CD-01** | **Brand Color Confirmation** | `[PENDING CLIENT CONFIRMATION]` | Verification of navy and gold hex codes. | `docs/05_open_questions.md#brand` |
| **CD-02** | **Arabic Brand Name** | `[PENDING CLIENT CONFIRMATION]` | Exact Arabic spelling for header lockup ("إي روم" vs. "إرم"). | `docs/05_open_questions.md#brand` |
| **CD-03** | **Font Family Approval** | `[PROPOSED CANDIDATE]` | Sign-off on Plus Jakarta Sans + Alexandria. | `docs/05_open_questions.md#brand` |
| **CD-04** | **Lead Form Step Model** | `[PROPOSED: 3-STEP WIZARD]` | Single-page vs. multi-step form design. | `docs/05_open_questions.md#business` |
| **CD-05** | **Numeral Format in Arabic** | `[PENDING CLIENT CONFIRMATION]` | Western (1, 2, 3) vs. Eastern Arabic (١، ٢، ٣) numerals for areas/dimensions. | `docs/05_open_questions.md#content` |
| **CD-06** | **Trust Badges & Customer Promises** | `[PENDING CLIENT CONFIRMATION]` | Confirm specific promises displayed on lead form (e.g. Direct Engineer Review, Free Initial Call). | `docs/05_open_questions.md#business` |
| **CD-07** | **File Upload Limit & Supported Types** | `[PENDING TECHNICAL / CLIENT CONFIRMATION]`| Confirm max upload size (proposed 25MB) and whether CAD/DWG files are accepted alongside PDF/images. | `docs/05_open_questions.md#p2-needed-before-implementation-and-launch` |
| **CD-08** | **Final Service List & Scope** | `[PENDING CLIENT CONFIRMATION]` | Confirm whether Custom Furniture and Exterior Design are separate standalone pillars. | `docs/05_open_questions.md#business` |

---

## 18. Recommended Figma Design Sequence (Phase 3 Workflow)

Figma design follows this 11-step sequence aligned with current canvas progress:

```text
Step 01: Design Foundations [IN FIGMA] (Color variables, typography styles, spacing grid, elevation)
   ↓
Step 02: Shared Component Library [IN FIGMA] (Header, footer, cards, form inputs, buttons, widgets)
   ↓
Step 03: Homepage [IN FIGMA] (Desktop & Mobile EN/AR, establishing core brand atmosphere)
   ↓
Step 04: Projects Listing [IN FIGMA - PROVISIONAL] (4 responsive bilingual frames verified; see docs/design/05_projects_listing_handoff.md)
   ↓
Step 05: Project Details & Case Study Template [CURRENT NEXT STEP - PROPOSED / NOT YET IN FIGMA]
   ↓
Step 06: Services Listing & Service Details
   ↓
Step 07: Knowledge Hub, Article Details, Video Library & Video Details
   ↓
Step 08: Lead Generation ("Start Your Project") & Contact Page
   ↓
Step 09: Remaining Pages (About, Meet The Engineer, Process, Search, 404, Legal)
   ↓
Step 10: Responsive Layouts (Tablet 834px & Mobile 390px edge cases)
   ↓
Step 11: Full Arabic (RTL) Layout Review (Typography balance & alignment symmetry)
   ↓
Step 12: Final Design QA & Client Sign-off (Replacing placeholders with approved assets)
```

---

## 19. Handoff Requirements for Future Frontend Development

When the Figma designs are approved and ready for frontend implementation:
1. **Figma Dev Mode Annotations:** Every component must have explicit auto-layout constraints, padding tokens, and gap measurements.
2. **Variable Token Mapping:** Figma variables must map 1:1 to CSS Custom Properties (`--color-brand-primary`, `--spacing-4`, `--radius-md`).
3. **Asset Export Readiness:** All icons must be exported as clean, optimized SVGs with `currentColor` fills where applicable.
4. **Responsive Behavior Specs:** Breakpoint behavior (stacking order, font size clamping, hide/show rules) must be explicitly noted in Figma sticky notes.
