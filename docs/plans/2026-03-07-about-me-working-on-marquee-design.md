# About Me + Working On Homepage Design

Date: 2026-03-07
Status: Approved
Direction: Approach A (Hero -> About Me -> Photo Marquee -> Things I'm Working On -> CTAs)

## Goals

- Split the current `Info` section into two sections:
  - `About Me`
  - `Things I'm Working On`
- Add more photos and present them in a continuously scrolling row.
- Keep the page simple and personal while preserving readability and responsiveness.

## Approved Structure

Homepage section order:

1. `SimpleHero`
2. `AboutMeSection`
3. `PhotoMarquee`
4. `WorkingOnSection`
5. `BottomCtas`

## Hero Requirement

- Keep an image in the hero section.
- Use the existing hero photo: `/images/me.jpg`.
- Keep current greeting copy.

## Content Model

In `src/pages/index.astro`, use static frontmatter content for:

- `heroImage` (existing `me.jpg`)
- `greeting` (existing approved text)
- `aboutMe` object (`title`, `body`)
- `marqueePhotos` array (`src`, `alt`, optional position)
- `workingOn` array (3 concise items)
- `ctaLinks` and `microcopy`

## Component Plan

- Keep: `src/components/SimpleHero.astro`
- Add: `src/components/AboutMeSection.astro`
- Add: `src/components/PhotoMarquee.astro`
- Add: `src/components/WorkingOnSection.astro`
- Keep: `src/components/BottomCtas.astro`

## Marquee Interaction Design

- Single continuously scrolling horizontal photo ribbon.
- CSS-only animation using `@keyframes` translateX.
- Duplicate track content once for seamless infinite looping.
- Moderate constant speed.
- Rounded image tiles with consistent height and `object-fit: cover`.

Accessibility and fallback:

- Respect `prefers-reduced-motion` by disabling animation and showing static content.

## Styling Direction

- Preserve the minimal personal visual direction.
- Maintain generous spacing and a clear hierarchy.
- Keep contrast and readability strong.
- Ensure responsive layout behavior on desktop and mobile.

## Verification

- `npm run build` succeeds.
- New section order appears in `src/pages/index.astro`.
- No placeholder links (`href="#"`) in `src`.
- Marquee reduced-motion fallback behaves correctly.
