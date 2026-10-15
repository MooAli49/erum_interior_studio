# ERUM Interior Studio — Figma Design Handoff & UI Specification

> **Document Status:** Provisional Figma UI Design & Handoff — client validation and asset approval pending.  
> **Figma file:** [ERUM Interior Studio — Phase 1 Design Foundations](https://www.figma.com/design/wcFiQnpI3crusgQPKJgPDB/ERUM-Interior-Studio-%E2%80%94-Phase-1-Design-Foundations?node-id=2013-1568)  
> **Repo:** https://github.com/MooAli49/erum_interior_studio

## Purpose
This file defines the working design system and handoff expectations. It is a specification source of truth for design intent, not proof that every documented page/frame has already been created in Figma. The live Figma file is the source of truth for the current canvas; this spec records what should be there and what remains provisional.

## Status labels
- `[CONFIRMED]`: explicitly confirmed requirement or verified supplied asset.
- `[PROPOSED]`: suggested direction that can be designed provisionally.
- `[PENDING CLIENT CONFIRMATION]`: must not be represented as final.
- `[IN FIGMA]`: verified in the live file only when checked.
- `[NOT YET IN FIGMA]`: specification exists, but a native editable frame has not been built.

## Existing Figma pages verified
- `01 — Foundations` `[IN FIGMA]`
- `02 — Components` `[IN FIGMA]`
- `03 — Homepage` `[IN FIGMA]`

The Homepage currently includes:
- `Home / EN / Desktop`
- `Home / EN / Mobile`
- `Home / AR / Desktop`
- `Home / AR / Mobile`
- `Homepage / Handoff & approvals`

Do not tell stakeholders that another page exists unless it is visible in the live file. The next intended page is `04 — Projects Listing (Provisional)` `[NOT YET IN FIGMA]`.

## Brand/design guardrails
- Primary visual direction: architectural, editorial, restrained luxury, image-first.
- Provisional colors: Navy `#203D73`, Midnight `#0E1B33`, Gold `#F5A000`, accessible gold `#B47100`, white/off-white. (Full token definitions in [Design System Specification](02_design_system.md)).
- Provisional typefaces: Plus Jakarta Sans for English and Alexandria for Arabic.
- Final logo lockup, palette, fonts and Arabic brand spelling remain pending.
- Reuse existing native component definitions. Do not create redundant component systems or visually divergent patterns.
- Arabic is intentional RTL composition; it is not simply a mirrored English frame.
- Small text on white must use a contrast-safe color. Bright gold is an accent, not default body text.

## Existing asset state
The supplied archive contained 309 JPGs over 10 folders. A working inventory (`erum_image_inventory.csv`), commercial shortlist (`erum_commercial_shortlist_v2_reviewed.csv`), and residential review package were generated as working review documents. They are not client-approved content.

Before publishing any image, confirm:
1. Correct group/project mapping and official project name.
2. Render vs photo vs construction/moodboard/plan status.
3. ERUM's role and exact scope.
4. Publication rights, including floor plans and any identifiable people.
5. Original-resolution quality, cropping and chosen cover/gallery order.

Never infer a project identity from its source-folder name. Visible ERUM marks in some supplied images were confirmed as the client's logo, but publishing permission still requires separate confirmation.

## Reusable Component Inventory & Layout Standards
Components built on `02 — Components` in Figma follow the specifications in [Design System Specification](02_design_system.md):
- **Header & Navigation:** 5 core links (Projects, Services, About, Knowledge, Contact), language toggle (`AR` | `EN`), CTA button. Mobile sticky 64px header with WhatsApp quick trigger and drawer.
- **Card Patterns:** `❖ Card / Project` (4:3 aspect ratio, category chip, metadata line), `❖ Card / Service`, `❖ Card / Article` (16:9), `❖ Card / Video` (16:9 / 9:16).
- **Interactive Widgets:** Render vs Reality split slider, Before/After slider, Video player modal.
- **Form Controls:** Text/tel inputs, select dropdowns, textareas, segmented pills, file dropzone.
- **Buttons:** Primary Navy, Accent Gold, Secondary Outline, Ghost.
- **Viewports:** Desktop 1440px (12 cols), Tablet 834px (8 cols), Mobile 390px (4 cols).

## Intended next design: Projects Listing
**Status: `[PROPOSED]` / `[NOT YET IN FIGMA]` until verified.**  
Detailed handoff spec: [05_projects_listing_handoff.md](05_projects_listing_handoff.md).

Create four editable, responsive frames on page `04 — Projects Listing (Provisional)`:
- `Projects Listing / EN / Desktop` — 1440px
- `Projects Listing / AR / Desktop` — 1440px, native RTL
- `Projects Listing / EN / Mobile` — 390px
- `Projects Listing / AR / Mobile` — 390px, native RTL

Recommended structure:
1. Existing global header / language switch / primary CTA.
2. Temporary internal review banner: `Provisional design — content and imagery awaiting client approval` / `تصميم مبدئي — المحتوى والصور بانتظار اعتماد العميل`.
3. Breadcrumb, eyebrow and `Selected Projects` / `مشاريع مختارة` heading.
4. Short intro with wording explicitly described as draft.
5. Filter chips: All projects, Residential, Commercial (Arabic equivalents). Do not show project counts until final inventory is approved.
6. Responsive project grid: three columns desktop, one column mobile. Use neutral image placeholders rather than unapproved assets.
7. Each card: provisional category, title pending confirmation, location/scope pending confirmation, View project link.
8. Contact CTA reusing existing CTA components.
9. Existing footer; all contact details remain unfilled until confirmed.

Use existing card, button, header and footer components wherever feasible. Design filters and navigation as prototypes only until interaction behavior is confirmed. Pagination vs Load More remains open. Do not imply that the number of placeholders is the final project count.

## Design QA before handoff
- Desktop/mobile and Arabic/English visual review.
- No horizontal overflow at 390px.
- Minimum 44px mobile touch targets.
- Visible focus states and clear keyboard order.
- Check Arabic line heights and text wrapping manually.
- Check text contrast.
- Ensure placeholders are editable and labelled as provisional.
- Do not use fabricated/stock imagery as if it were client work.
- Remove internal approval banners before final client-facing presentation, or replace with approved copy.

## Current dependencies & client hold points
All open client decisions are tracked in the canonical register: [Open Questions & Decisions](../05_open_questions.md). Key dependencies include:
- Official logo and brand guidelines.
- Confirmed photo/project mapping and publication permission.
- Approved project metadata and initial project list.
- Final services/service areas.
- Contact channels and CTA destination.
- Approved Arabic/English copy.
