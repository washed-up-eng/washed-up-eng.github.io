# Resume Page Content Refresh Implementation Plan

> **For Claude:** REQUIRED SUB-SKILL: Use superpowers:executing-plans to implement this plan task-by-task.

**Goal:** Replace the placeholder `/resume` page with structured, resume-accurate sections sourced from `docs/resumes/Base Resume.pdf`, with title set to Senior Product Manager.

**Architecture:** Keep implementation in `src/pages/resume.astro` using static frontmatter content arrays/objects and semantic section blocks. Preserve existing site visual language by reusing current layout tokens and minimal scoped style updates for sectioned resume content. Maintain existing CTA/link behavior while ensuring LinkedIn uses the approved URL.

**Tech Stack:** Astro, component-scoped CSS, static frontmatter content, npm build verification

---

### Task 1: Create resume content structure in frontmatter

**Files:**
- Modify: `src/pages/resume.astro`

**Step 1: Write failing content check for current placeholder sentence**

Run:

```bash
grep -n "quick resume snapshot while a downloadable PDF is being finalized" src/pages/resume.astro
```

Expected: 1 match.

**Step 2: Add structured content objects/arrays in frontmatter**

Add frontmatter constants for:

- Header metadata (name, title, location, linkedin)
- Summary paragraph(s)
- Impact highlights list
- Experience list (role, company, date range, location, bullets)
- Education list
- Skills list
- Footer CTA links

Keep content faithful to `docs/resumes/Base Resume.pdf`.

**Step 3: Verify placeholder sentence remains until layout replacement task**

Run:

```bash
grep -n "quick resume snapshot while a downloadable PDF is being finalized" src/pages/resume.astro
```

Expected: 1 match.

**Step 4: Commit**

```bash
git add src/pages/resume.astro
git commit -m "Add structured frontmatter model for resume page content"
```

### Task 2: Replace resume header and summary blocks

**Files:**
- Modify: `src/pages/resume.astro`

**Step 1: Write failing checks for current title and header copy**

Run:

```bash
grep -n "Technical Program Manager for startup execution\|Contact on LinkedIn" src/pages/resume.astro
```

Expected: current title line and legacy CTA copy match.

**Step 2: Implement new header and summary rendering**

Render:

- Name: Sijae Brown
- Title: Senior Product Manager
- Location: Boulder, Colorado
- LinkedIn URL only in header metadata row (no Contact/email field)
- Executive summary text from the base resume

**Step 3: Verify updated header content**

Run:

```bash
grep -n "Senior Product Manager\|Boulder, Colorado\|linkedin.com/in/sijae-brown-54331489" src/pages/resume.astro
```

Expected: 3+ matches.

**Step 4: Commit**

```bash
git add src/pages/resume.astro
git commit -m "Replace resume header and summary with resume-sourced copy"
```

### Task 3: Add impact highlights and full work experience sections

**Files:**
- Modify: `src/pages/resume.astro`

**Step 1: Write failing checks for key metric phrases**

Run:

```bash
grep -n "85%\+\|100% of patient visits\|8 minutes to seconds\|75%" src/pages/resume.astro
```

Expected: missing or incomplete matches before full experience rendering.

**Step 2: Render Core Impact Highlights section**

Include metric-forward bullets derived from resume:

- 100% patient visits powered by eChart
- 85%+ of visits automated in billing flow
- 75%+ billing operations reduction
- PHI exchange reduced from 8 minutes to seconds

**Step 3: Render Work Experience section (reverse chronological)**

Render roles and bullets for:

- Float Health (Senior Product Manager)
- Upstream Tech (Machine Learning Engineer)
- Lockheed Martin Space (Research Scientist - ML/AI)
- Lockheed Martin Aeronautics (AI Software Engineer)

Keep bullets concise but faithful to resume wording.

**Step 4: Verify key entities and metrics appear**

Run:

```bash
grep -n "Float Health\|Upstream Tech\|Lockheed Martin Space\|Lockheed Martin Aeronautics\|85%\+\|100%\|8 minutes to seconds\|75%" src/pages/resume.astro
```

Expected: all company names and metric tokens found.

**Step 5: Commit**

```bash
git add src/pages/resume.astro
git commit -m "Add impact highlights and full work experience to resume page"
```

### Task 4: Add education, skills, and footer CTA row

**Files:**
- Modify: `src/pages/resume.astro`

**Step 1: Write failing checks for missing education/skills content**

Run:

```bash
grep -n "University of Missouri-Columbia\|Skills\|Rules Engines & Automation" src/pages/resume.astro
```

Expected: one or more patterns missing before section implementation.

**Step 2: Render Education section**

Include university and date range from resume.

**Step 3: Render Skills section**

Render skills from resume in readable web format (tag grid or grouped bullets).

**Step 4: Update footer CTA row**

Keep:

- Back to Portfolio
- GitHub (`https://github.com/washed-up-eng`)
- LinkedIn (`https://www.linkedin.com/in/sijae-brown-54331489/`)

Ensure no "Contact" label requirement in header.

**Step 5: Verify section keywords and links**

Run:

```bash
grep -n "University of Missouri-Columbia\|Skills\|github.com/washed-up-eng\|linkedin.com/in/sijae-brown-54331489" src/pages/resume.astro
```

Expected: all patterns found.

**Step 6: Commit**

```bash
git add src/pages/resume.astro
git commit -m "Add education skills and footer links to resume page"
```

### Task 5: Visual polish and responsive cleanup for sectioned resume

**Files:**
- Modify: `src/pages/resume.astro`

**Step 1: Write failing check for old single-panel layout class usage**

Run:

```bash
grep -n "class=\"panel\"" src/pages/resume.astro
```

Expected: legacy single-panel usage still present.

**Step 2: Apply scoped style updates for multi-section readability**

Add/update CSS for:

- section cards and spacing rhythm
- role headers and date/location metadata
- bullet readability
- skills tag/bullet presentation
- mobile stacking behavior

Stay within existing site visual identity.

**Step 3: Verify style anchors exist**

Run:

```bash
grep -n "\.section\|\.role\|\.skills\|@media" src/pages/resume.astro
```

Expected: all selectors present.

**Step 4: Commit**

```bash
git add src/pages/resume.astro
git commit -m "Polish resume page layout for scannable sectioned content"
```

### Task 6: End-to-end verification

**Files:**
- Verify: `src/pages/resume.astro`
- Verify: `src/pages/index.astro`

**Step 1: Run build**

Run:

```bash
npm run build
```

Expected: build succeeds and outputs `/resume/index.html` and `/index.html`.

**Step 2: Validate no placeholder links**

Run:

```bash
grep -R "href=\"#\"" src
```

Expected: no matches.

**Step 3: Validate resume route and social links exist**

Run:

```bash
grep -n "/resume\|linkedin.com/in/sijae-brown-54331489\|github.com/washed-up-eng" src/pages/index.astro src/pages/resume.astro
```

Expected: all patterns found.

**Step 4: Final commit for any residual edits**

```bash
git add src/pages/resume.astro src/pages/index.astro
git commit -m "Finalize resume page refresh from base resume content"
```
