# ERUM Interior Studio — Projects Listing Figma Handoff (Provisional)

**Status:** Provisional Figma UI Design & Handoff — client validation and asset approval pending.  
**Figma Canvas Status:** `[PROPOSED]` / `[NOT YET IN FIGMA]`  
**Scope:** Projects Listing page, desktop + mobile, Arabic RTL + English LTR.  
**Important:** The Projects Listing page is NOT yet present on the live Figma canvas. This document serves as the handoff specification to construct page `04 — Projects Listing (Provisional)` in Figma. Keep unconfirmed elements visibly provisional.

## Existing Figma file
- File: `ERUM Interior Studio — Phase 1 Design Foundations`
- File key: `wcFiQnpI3crusgQPKJgPDB`
- Existing actual pages: `01 — Foundations` `[IN FIGMA]`, `02 — Components` `[IN FIGMA]`, `03 — Homepage` `[IN FIGMA]`
- Add an actual page named `04 — Projects Listing (Provisional)` when write access is available.
- Reuse the existing components and visual language; do not create a second design system.

## Temporary tokens (pending approval)
- Navy `#203D73`; Midnight `#0E1B33`; Gold `#F5A000`; accessible gold `#B47100`
- White `#FFFFFF`; text `#181F2B`; muted `#626C7B`; border `#E2E6EC`; soft `#F6F7F9`
- English font candidate: Plus Jakarta Sans; Arabic font candidate: Alexandria
- Use existing variables/components when possible. Final logo, brand colors, fonts, and Arabic naming are unconfirmed.

## Frames
1. `Projects Listing / EN / Desktop` — 1440px
2. `Projects Listing / AR / Desktop` — 1440px, intentional RTL
3. `Projects Listing / EN / Mobile` — 390px
4. `Projects Listing / AR / Mobile` — 390px, intentional RTL

Use editable text, components, and Auto Layout; never use a flattened full-page screenshot as the deliverable.

## Page structure
1. Existing global header component; provisional wordmark; language switch; CTA `Start a project` / `ابدأ مشروعك`.
2. A temporary pale-gold status strip:
   - EN: `Provisional design — content and imagery awaiting client approval`
   - AR: `تصميم مبدئي — المحتوى والصور بانتظار اعتماد العميل`
3. Breadcrumb: `Home / Projects` / `الرئيسية / المشاريع`.
4. Eyebrow: `THE PORTFOLIO` / `معرض الأعمال`.
5. Heading: `Selected Projects` / `مشاريع مختارة`.
6. Intro:
   - EN: `Explore a collection of ERUM project work. Final project titles, imagery, locations and service scope will be added after client review.`
   - AR: `استكشف مجموعة من أعمال ERUM. ستُضاف أسماء المشاريع والصور والمواقع ونطاق العمل بعد مراجعة العميل.`
7. Filters using existing chips/buttons: All projects / كل المشاريع; Residential / سكني; Commercial / تجاري. Don't show counts until the project list is confirmed.
8. Responsive project grid:
   - Desktop: 3 columns, generous spacing, consistent 4:3 or 3:2 image frames.
   - Mobile: 1 column, no horizontal overflow.
   - Show 6 editable placeholder cards on desktop and 4 on mobile; this is a layout sample, not the final project count.
9. Each card: neutral image placeholder labelled pending approval; provisional category; `Project title pending client confirmation` / `اسم المشروع بعد تأكيد العميل`; metadata placeholder for location/scope; `View project` / `عرض التفاصيل`.
10. Contact CTA: `Planning a project? Let’s talk.` / `بتخطط لمشروع؟ خلينا نتكلم.` and `Start a project` / `ابدأ مشروعك`.
11. Existing footer component. Do not invent phone/email/address/hours/social links.

## Asset status
The supplied archive contains 309 images across 10 folders (canonical working inventory documented in [Asset Checklist](../04_asset_checklist.md)). The visible ERUM logo is the client's company logo (confirmed by maintainer). Do not treat folder names as proof of project identity. Keep temporary internal candidate IDs like `RES-CAND-01` and `COM-CAND-01` until official names are confirmed. Do not claim completed execution or use “Render vs Reality” unless confirmed. Keep image type `Unknown` until verified. Use neutral placeholders until image groups, quality, permission, render/photo status, and ERUM's scope are confirmed.

## Accessibility / QA
- Minimum mobile target: 44px; visible focus state; keyboard order.
- Use `#B47100` or navy for small text on white; reserve bright gold for accents/large fills.
- RTL must be composed intentionally, not just mirrored.
- Verify card title wrapping at 390px and no horizontal overflow.
- Keep image aspect ratios reserved to prevent layout shift.
- Reuse existing header, footer, card, chip, button, and typography patterns where possible.

## Client hold points
All open decisions are tracked in the canonical register: [Open Questions & Decisions](../05_open_questions.md):
- Official brand name, Arabic spelling, logo, colors, fonts.
- Image-to-project grouping and official project names/locations.
- Render vs completed photography.
- ERUM role per project: design, execution, project management, or other.
- Permission to publish images/floor plans and any images containing people.
- Final service list, service areas, CTA destination, contacts.
- Top 3 homepage projects, initial portfolio count, filter taxonomy, pagination/load-more behavior.

## Ready-for-review criteria
- Four editable bilingual/responsive frames.
- Existing components reused where possible.
- No unverified names, locations, completion claims, contact details, testimonials, guarantees, or promises presented as facts.
- All temporary elements marked provisional.
- Desktop/mobile and RTL/LTR visually checked.
