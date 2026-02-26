# Resume Page Content Design

Date: 2026-02-26
Status: Approved
Scope: Update `src/pages/resume.astro` using content from `docs/resumes/Base Resume.pdf`

## Goals

- Replace the placeholder resume snapshot with full, web-native resume content.
- Keep the page easy to scan in under 90 seconds while preserving concrete impact details.
- Align with portfolio tone and visual system already used across the site.

## Chosen Direction

Use a structured resume page (not raw PDF rendering) with clear sectioning and concise, metric-rich bullets.
This provides better readability and recruiter scan speed than embedding or mirroring the PDF verbatim.

## Content Decisions

- Title shown on page: **Senior Product Manager**
- Header should not include a Contact/email field.
- Header should include:
  - Name
  - Title
  - Location
  - LinkedIn

## Information Architecture

1. Resume hero header (name/title/location/link)
2. Executive summary
3. Core impact highlights
4. Work experience (reverse chronological)
5. Education
6. Skills
7. Footer CTA row (Back to Portfolio, GitHub, LinkedIn)

## Content Mapping from Base Resume

### Header

- Name: Sijae Brown
- Title: Senior Product Manager
- Location: Boulder, Colorado
- LinkedIn: `https://www.linkedin.com/in/sijae-brown-54331489/`

### Executive Summary

Use the existing profile narrative from `Base Resume.pdf`, lightly edited for web readability while preserving meaning.

### Work Experience

Preserve reverse chronological order and key outcomes:

- Float Health (11/2022-Present), Senior Product Manager
- Upstream Tech (11/2021-11/2022), Machine Learning Engineer
- Lockheed Martin Space (11/2019-09/2021), Research Scientist - Machine Learning and Artificial Intelligence
- Lockheed Martin Aeronautics (06/2017-11/2019), AI Software Engineer

Keep core quantifiable proof points intact where available, including:

- 100% of visits powered by eChart
- 85%+ visit volume automated in revenue flow
- 75%+ billing operations time reduction
- PHI-sharing time reduced from 8 minutes to seconds

### Education

- University of Missouri-Columbia (2012-2017)

### Skills

Convert PDF skills into web-scannable format (compact bullet groups or tags), keeping wording faithful to resume.

## UX and Layout Notes

- Keep current design language (Space Grotesk + Manrope, teal accents, card surfaces).
- Use section cards with clear headings and short spacing between bullets.
- Optimize for desktop and mobile readability without introducing new interaction complexity.

## Verification Checklist

- `npm run build` succeeds.
- Resume page renders all sections and maintains responsive layout.
- Header does not include Contact/email.
- LinkedIn URL matches `https://www.linkedin.com/in/sijae-brown-54331489/`.
- Existing homepage and resume links remain valid.

## Out of Scope

- PDF embed/viewer implementation
- CMS-driven resume content
- Download tracking analytics
