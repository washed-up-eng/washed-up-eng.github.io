# Simple Personal Homepage Design

Date: 2026-03-04
Status: Approved
Direction: Quiet Personal Landing

## Goals

- Keep the homepage simple and personal.
- Use one main photo and a short greeting instead of resume-style content.
- Add an `Info` section with personal photos (you and your animals).
- Move all CTAs below the `Info` section.

## Chosen Direction

Use a minimal structure with three clear blocks:

1. Hero (single main photo + greeting)
2. `Info` photo section (4 photos)
3. CTA row (all actions below `Info`)

This keeps the page clean, expressive, and easy to scan.

## Content Structure

### Hero

- One main image of you.
- Short greeting line.
- No resume-like overview or dense professional copy.

### Info

- Section title: `Info`
- Optional one-line intro sentence.
- Four photos in a responsive grid (you + animals).

### CTA Block (below Info)

- Primary: `Request Resume` (links to LinkedIn)
- Secondary: `LinkedIn`
- Tertiary: `GitHub`
- Microcopy: `Resume available upon request.`

## Visual Notes

- Keep whitespace generous and layout calm.
- Tone should feel soft/feminine while still strong and intentional.
- Avoid resume-card patterns and heavy section density.
- Use subtle motion only (small fade/rise).

## Implementation Constraints

- Keep `src/pages/index.astro` as the composition layer.
- Replace old homepage sections with lightweight personal components.
- Keep content static via frontmatter arrays/objects.
- Store photo assets in `public/images/`.
- Keep CTA links real URLs (no placeholders).

## Verification Checklist

- `npm run build` succeeds.
- Main hero image renders and scales correctly.
- `Info` section renders 4 images responsively.
- CTA block appears below `Info` and includes approved microcopy.
- `Request Resume` points to LinkedIn.

## Out of Scope

- Password-protected resume flows
- Dynamic gallery or CMS
- Multi-page redesign outside homepage
