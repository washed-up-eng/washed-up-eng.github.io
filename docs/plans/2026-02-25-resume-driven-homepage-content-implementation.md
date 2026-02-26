# NEW CASE STUDIES 
I want to update the plan under the heading "Resme-Driven Homepage Content Implementation Plan" to include the following information.  
I want to update each of the case studies to use the following format : Problem, Insight, System Built, Business Shift, Artifact. 

**Clinical Staffing Engine**
The first case study should be called, "Clinical Staffing Engine". Here is the copy for each of the headings.
-  Problem : "Staffing decisions relied on tacit operational knowledge and informal coordination, introducing bias, variability and scale constraints under growth pressure."
- Insight : "Inconsistency wasn’t a people problem — it was a systems problem. Critical matching logic lived in undocumented heuristics, with regulatory constraints and acuity signals applied unevenly across operators."
- System Built : "Encoded nurse skillsets, regulatory constraints and patient acuity into a production-grade matching engine — converting tribal knowledge into structured, enforceable decision logic."
- Business Shift : "Transformed a high-variance, manually curated workflow into scalable infrastructure — unlocking growth without proportional scheduling headcount, standardizing decision quality and reducing operational entropy."
- Artifact : "Matching logic architecture + deployment instrumentation"

**Revenue Orchestration System**
The second case study should be called, "Revenue Orchestration System". Here is the copy for each of the headings.
-  Problem : "Billing and nurse payouts relied on repetitive manual coordination across clinical, finance, and operations — creating latency, human error risk and scaling constraints as visit volume grew."
- Insight : "Sustainable scale required treating revenue flow as a system — not a series of handoffs."
- System Built : "Designed and deployed an automated visit-to-revenue pipeline integrating clinical documentation, invoicing logic and Stripe-based payout scheduling — transforming manual handoffs into event-driven financial infrastructure."
- Business Shift : "Shifted 85%+ of visits to automated processing, reduced billing time by 75%+ and transformed finance operations from reactive task execution to scalable infrastructure."
- Artifact : "Revenue automation dashboard + payout trigger instrumentation"

**PHI Governance & Workflow Modernization**
The third case study should be called, "PHI Governance & Workflow Modernization". Here is the copy for each of the headings.
-  Problem : "Clinical document exchange depended on fragmented systems, exposing the organization to HIPAA risk and operational inefficiency."
- Insight : "Sustainable scale required embedding compliance into infrastructure — not relying on process discipline alone."
- System Built : "Architected and led migration to a centralized, HIPAA-compliant document management system with role-based access, audit trails and controlled PHI lifecycle management."
- Business Shift : "Collapsed PHI exchange time from minutes to seconds while materially reducing compliance exposure and enabling scalable, secure clinical operations."
- Artifact : "Launch sequencing plan + enterprise risk mitigation register".m


# Resume-Driven Homepage Content Implementation Plan

> **For Claude:** REQUIRED SUB-SKILL: Use superpowers:executing-plans to implement this plan task-by-task.

**Goal:** Update the homepage and resume pages with resume-accurate TPM-first content, including the approved hero value statement and quantified impact proof.

**Architecture:** Keep `src/pages/index.astro` as the composition layer with static frontmatter arrays feeding presentational components. Update only content and small style tokens where needed to preserve the approved visual system. Keep CTA destinations real and consistent across homepage and resume page.

**Tech Stack:** Astro, component-scoped CSS, static content in frontmatter arrays, npm build verification

---

### Task 1: Update Hero content with approved value statement

**Files:**
- Modify: `src/pages/index.astro`

**Step 1: Write the content assertion checks (failing-first)**

Run:

```bash
rg "I turn ambiguity into shipped outcomes" src/pages/index.astro
```

Expected: 1 match (old value statement still present).

**Step 2: Replace hero value statement with approved copy**

Set `valueStatement` to:

```text
In short, I turn ambiguity into execution, tribal knowledge into systems, and ambitious ideas into infrastructure that scales.
```

**Step 3: Verify replacement**

Run:

```bash
rg "In short, I turn ambiguity into execution" src/pages/index.astro
```

Expected: 1 match.

**Step 4: Commit**

```bash
git add src/pages/index.astro
git commit -m "Update hero value statement to approved TPM positioning"
```

### Task 2: Replace impact cards with resume-backed metrics

**Files:**
- Modify: `src/pages/index.astro`

**Step 1: Write failing content checks**

Run:

```bash
rg "12 launches|4 core functions|91% on-time" src/pages/index.astro
```

Expected: 3 matches (placeholder metrics).

**Step 2: Replace `impactCards` array values**

Use these cards exactly:

1) `Automation at scale` / `85%+ visit volume automated` / `Led invoicing and payout automation at Float, cutting billing operations time by over 75%.`

2) `Clinical platform ownership` / `100% of visits supported` / `Spearheaded zero-to-one eChart development powering all patient visits for the last 3 years.`

3) `Execution speed + compliance` / `8 minutes to seconds` / `Led HIPAA-compliant document workflow modernization, dramatically reducing PHI sharing time.`

**Step 3: Verify updated metrics exist**

Run:

```bash
rg "85%\+ visit volume automated|100% of visits supported|8 minutes to seconds" src/pages/index.astro
```

Expected: 3 matches.

**Step 4: Commit**

```bash
git add src/pages/index.astro
git commit -m "Replace impact snapshots with resume-validated metrics"
```

### Task 3: Replace case studies with resume-derived Float stories

**Files:**
- Modify: `src/pages/index.astro`

**Step 1: Write failing content checks**

Run:

```bash
rg "Enterprise Onboarding Program|Reliability Recovery Initiative|Usage Analytics Rollout" src/pages/index.astro
```

Expected: 3 matches (synthetic case studies still present).

**Step 2: Replace `caseStudies` with resume-backed stories**

Create three case studies:

- `Automated Nurse Selector (Float)` with challenge/actions/result and artifact `Decision framework and matching rules`.
- `Document Management v2 (Float)` with challenge/actions/result and artifact `Launch plan and risk register`.
- `Invoicing and Payout Automation (Float)` with challenge/actions/result and artifact `Automation dashboard`.

Keep structure compatible with `CaseStudyList.astro` props.

**Step 3: Verify new case study titles appear**

Run:

```bash
rg "Automated Nurse Selector \(Float\)|Document Management v2 \(Float\)|Invoicing and Payout Automation \(Float\)" src/pages/index.astro
```

Expected: 3 matches.

**Step 4: Commit**

```bash
git add src/pages/index.astro
git commit -m "Use resume-based Float case studies on homepage"
```

### Task 4: Update final CTA prompt for TPM hiring message

**Files:**
- Modify: `src/pages/index.astro`

**Step 1: Write failing check for old CTA prompt**

Run:

```bash
rg "If you are hiring a TPM to make high-ambiguity work shippable" src/pages/index.astro
```

Expected: 1 match.

**Step 2: Replace prompt text**

Set CTA prompt to:

```text
If you need a TPM who can operationalize complex programs and ship reliably across engineering, product, design, and operations, let's talk.
```

**Step 3: Verify replacement**

Run:

```bash
rg "operationalize complex programs and ship reliably" src/pages/index.astro
```

Expected: 1 match.

**Step 4: Commit**

```bash
git add src/pages/index.astro
git commit -m "Align final CTA message with TPM-first positioning"
```

### Task 5: Align resume page summary to same narrative

**Files:**
- Modify: `src/pages/resume.astro`

**Step 1: Write failing check for temporary placeholder sentence**

Run:

```bash
rg "quick resume snapshot while a downloadable PDF is being finalized" src/pages/resume.astro
```

Expected: 1 match.

**Step 2: Replace intro and bullets with resume-backed language**

Update the summary paragraph and bullets to include:

- Senior TPM profile (applied AI, systems automation, zero-to-one delivery).
- Cross-functional execution across healthcare, defense, and climate domains.
- Measured outcomes (75%+ billing ops reduction, 100% visit support via eChart, PHI sharing reduced from 8 minutes to seconds).

**Step 3: Verify outcome phrases present**

Run:

```bash
rg "75%|100%|8 minutes to seconds" src/pages/resume.astro
```

Expected: at least 3 matches.

**Step 4: Commit**

```bash
git add src/pages/resume.astro
git commit -m "Refresh resume page with quantified TPM outcomes"
```

### Task 6: End-to-end verification and link checks

**Files:**
- Verify: `src/pages/index.astro`
- Verify: `src/pages/resume.astro`

**Step 1: Build site**

Run:

```bash
npm run build
```

Expected: Astro build completes and outputs `/index.html` and `/resume/index.html`.

**Step 2: Validate no placeholder links**

Run:

```bash
rg "href=\"#\"|example.com" src
```

Expected: no matches.

**Step 3: Validate CTA destinations are consistent**

Run:

```bash
rg "linkedin.com/in/sijae-brown|github.com/washed-up-eng|/resume" src/pages/index.astro src/pages/resume.astro
```

Expected: all three destination patterns found.

**Step 4: Final commit for any remaining polish**

```bash
git add src/pages/index.astro src/pages/resume.astro
git commit -m "Finalize resume-driven homepage content updates"
```
