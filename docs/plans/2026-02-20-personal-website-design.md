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
This balances recruiter speed with hiring manager depth. Use the resume called "Base Resume.pdf" in the 
/resumes folder to find the correct content for the website.

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
- Value statement: In short, I turn ambiguity into execution, tribal knowledge into systems, and ambitious ideas into infrastructure that scales.
- CTA row: View Resume, Contact, GitHub

### Impact Snapshots

Three compact proof cards:

- Automation at scale: 85%+ visit volume automated after leading invoicing and payout automation; billing operations reduced by over 75%.
- Clinical platform ownership: zero-to-one eChart development now supports 100% of patient visits over the last 3 years.
- Execution speed + compliance: HIPAA-compliant workflow modernization reduced PHI sharing time from 8 minutes to seconds.

### Featured Case Studies

Two to three concise stories in this structure:

- Challenge
- Actions
- Result

Each case study includes one concrete artifact signal (roadmap, launch plan, decision memo, or dashboard).

Case study candidates sourced from the base resume:

- Automated Nurse Selector (Float)
  - Challenge: high-variance, manually curated staffing process.
  - Actions: translated tacit operational knowledge into a zero-touch matching workflow using nurse skill, acuity, and care complexity.
  - Result: scalable nurse-to-patient matching and improved marketplace reliability.
  - Artifact signal: decision framework and matching rules.
- Document Management v2 (Float)
  - Challenge: fragmented clinical documentation workflows and slow PHI sharing.
  - Actions: led migration from fragmented Google Drive workflows to secure in-app HIPAA-compliant document management.
  - Result: PHI sharing time reduced from 8 minutes to seconds.
  - Artifact signal: launch plan and risk register.
- Invoicing and Payout Automation (Float)
  - Challenge: manual billing and payout operations constrained scale.
  - Actions: integrated Stripe-triggered payouts and pharmacy invoicing tied to eChart submission.
  - Result: over 75% reduction in billing operations time and automation across 85%+ visit volume.
  - Artifact signal: automation dashboard.

### Working Style

Four principles:

- Align quickly, document clearly
- De-risk early with milestones
- Keep decision logs visible
- Balance speed with reliability

### Final CTA Band

Closing prompt line plus CTA buttons:

- Prompt: If you need a TPM who can operationalize complex programs and ship reliably across engineering, product, design, and operations, let's talk.

- View Resume
- Contact
- GitHub

## Visual System

- Mood: creative hybrid, professional with personality.
- Typography: Space Grotesk for display, Manrope for body.
- Color: dark teal (#00555A hex value) accent system, no orange background tones, but may use orange as an accent. 
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
- CTA links validated (resume, linkedin, GitHub).
- Accessibility and contrast quick pass.

## Out of Scope (for now)

- Dynamic CMS integration
- Multi-language support
- Complex animation systems
