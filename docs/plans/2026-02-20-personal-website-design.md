# Personal Website Design - Sijae Brown

Date: 2026-02-20
Status: Approved
Approach: Narrative portfolio with impact snapshots

## Goals

- Primary outcome: get hired for a Technical Program Manager role at startup companies.
- Voice: balanced (confident and approachable).
- Proof priorities: launches shipped, cross-functional leadership, and execution metrics.

## Chosen Direction

We will use a narrative portfolio structure that combines quick-scan proof with concise storytelling.
This balances recruiter speed with hiring manager depth.

## Site Architecture

Single-page homepage optimized for 60-90 second scans:

1. Hero
2. Impact snapshots (3 cards)
3. Featured case studies (2-3)
4. Working style / TPM principles
5. Final CTA band

CTAs:

- Primary: View Resume
- Secondary: Contact Sijae
- Tertiary: GitHub

## Content Blueprint

### Hero

- Headline: Sijae Brown
- Subhead: Technical Program Manager for startup execution
- Value statement: turns ambiguity into shipped outcomes
- CTA row: View Resume, Contact, GitHub

### Impact Snapshots

Three compact proof cards:

- Launches shipped (0 to 1 programs/features)
- Cross-functional leadership (engineering/product/design/ops)
- Execution metrics (delivery reliability, cycle-time, or adoption)

### Featured Case Studies

Two to three concise stories in this structure:

- Challenge
- Actions
- Result

Each case study includes one concrete artifact signal (roadmap, launch plan, decision memo, or dashboard).

### Working Style

Four principles:

- Align quickly, document clearly
- De-risk early with milestones
- Keep decision logs visible
- Balance speed with reliability

### Final CTA Band

Closing prompt line plus CTA buttons:

- View Resume
- Contact
- GitHub

## Visual System

- Mood: creative hybrid, professional with personality.
- Typography: Space Grotesk for display, Manrope for body.
- Color: dark teal accent system, no orange background tones.
- Layout: max-width content rail with responsive card grids.
- Motion: subtle rise/fade and card stagger; no heavy parallax.

## Implementation Constraints

- Keep `src/pages/index.astro` as composition layer.
- Add focused presentational components in `src/components/`:
  - `Hero`
  - `ImpactCards`
  - `CaseStudyList`
  - `CTAFooter`
- Keep content static via frontmatter arrays first; optionally migrate to content collections later.
- Ensure production links are real URLs (no placeholder `#`).

## Verification Checklist

- `npm run build` succeeds.
- Desktop and mobile layout checks pass.
- CTA links validated (resume, contact, GitHub).
- Accessibility and contrast quick pass.

## Out of Scope (for now)

- Dynamic CMS integration
- Multi-language support
- Complex animation systems
