# Personality-First Homepage Redesign

Date: 2026-03-03
Status: Approved
Direction: Open Terrain (free, feminine, strong)

## Goals

- Redesign the homepage to feel personal, expressive, and human rather than resume-like.
- Show lifestyle and personality through imagery and concise copy.
- Keep a clear but lightweight professional signal.
- Route resume requests through LinkedIn with intentional friction.

## Core Decisions

- Homepage should be stripped down and not read like a resume.
- Add personal photos (you and/or your animals) in a visual-forward layout.
- Keep a nod to professional work without dense case-study formatting.
- Primary CTA should be `Request Resume`.
- Resume access behavior on homepage should include microcopy: `Resume available upon request.`
- Resume requests should go through LinkedIn.

## Experience Direction

The page should feel open-air and grounded with a feminine edge while remaining strong and direct.
Voice should be concise and confident, with short statements instead of long professional sections.

Lifestyle themes to reflect:

- Horses
- Mountain sports
- Trail running
- Ocean swimming

## Homepage Architecture

`src/pages/index.astro` remains composition-only and renders five focused sections:

1. `PersonalHero`
   - Name
   - One-line identity
   - Primary CTA: `Request Resume` (LinkedIn)
   - Microcopy: `Resume available upon request.`
2. `PhotoMosaic`
   - 2-4 personal images
   - Asymmetric responsive layout
3. `InMotion`
   - Short personal lines about horses, mountain sports, trail running, ocean swimming
4. `ProfessionalNod`
   - 2-3 compact proof lines about technical/product leadership
5. `SimpleFooterLinks`
   - LinkedIn
   - GitHub

## Content Strategy

- Keep all homepage content static in frontmatter arrays/objects for now.
- Avoid resume-style section headers like "Work Experience" or long role timelines on homepage.
- Favor short copy blocks that read like a personal introduction.
- Keep `src/pages/resume.astro` available in repository, but de-emphasize it from homepage flow.

## Visual System Notes

- Keep existing quality bar for typography and responsive behavior.
- Shift visual tone away from corporate-heavy treatment and toward editorial personal storytelling.
- Use spacing and image rhythm to create a sense of freedom and motion.
- Maintain strong contrast and legibility.

## CTA Rules

- Primary homepage action: `Request Resume` -> LinkedIn profile
- Display text near CTA: `Resume available upon request.`
- Keep LinkedIn and GitHub links available in footer-level actions.

## Verification Checklist

- `npm run build` succeeds.
- Homepage layout works on desktop and mobile.
- `Request Resume` points to LinkedIn.
- Microcopy appears exactly as approved.
- No placeholder links (`#`).
- Images load correctly and crop gracefully across breakpoints.

## Out of Scope

- CMS integration
- Dynamic galleries
- Authentication or password protection for resume
