# Claude Code Workflow for DOE Genesis Mission Phase I Proposal

## Purpose

This file provides a practical execution workflow for using Claude Code to iteratively strengthen the proposal package for the DOE Genesis Mission Phase I application.

**Project Title:**  
AI-Driven Biomolecular Modeling of H5N1 Antigenic Evolution, Immune Escape, and Cross-Species Adaptation

**Target Context:**  
DOE Genesis Mission, Phase I, 9-month project, Topic 2 / Focus Area 2A

This workflow is designed to help Claude Code behave like a controlled proposal-writing system rather than a one-shot text generator.

---

## Core Operating Principles

1. **Read before writing.**  
   Claude must read `CLAUDE.md`, `AGENTS.md`, and all major proposal files before revising anything.

2. **Narrative-first revision.**  
   `proposal/03_project_narrative.md` is the central file. Other files must align to it.

3. **No unsupported invention.**  
   Claude must not invent:
   - partner institution names,
   - signatures,
   - facility access,
   - approvals,
   - citations,
   - budget numbers,
   - data-access permissions.

4. **DOE style over hype.**  
   The writing should be reviewer-friendly, concise, concrete, disciplined, and defensible.

5. **Phase I discipline.**  
   The project must remain tightly scoped to a 9-month effort focused on:
   - a clear and tangible AI-enabled research workflow,
   - measurable AI advantage,
   - realistic milestones,
   - credible transition logic for Phase II.

6. **Consistency matters.**  
   The proposal package should tell one coherent story across narrative, plans, milestones, appendices, and letters.

---

## Recommended Execution Order

Use the following prompts in sequence.  
Do **not** start by asking Claude to write the entire proposal from scratch in one pass.

---

## Step 0 — Read the workspace only

Use this first:

```text
Please read the project scaffold before writing anything.

Tasks:
1. Read CLAUDE.md and AGENTS.md carefully.
2. Read all files under proposal/, docs/, templates/, and proposal/appendices/ if present.
3. Build an internal understanding of:
   - the DOE Genesis Mission Phase I context,
   - Topic 2 / Focus Area 2A alignment,
   - the proposed project title,
   - the expected 9-month Phase I scope,
   - the current state of the draft narrative and appendices.
4. Do not rewrite files yet.
5. Return only:
   - a concise map of the project structure,
   - the 10 most important missing factual inputs,
   - the 10 most important writing risks,
   - the 5 highest-priority files to revise first.

Important constraints:
- Treat this as a DOE proposal-writing environment.
- Be conservative, specific, and evidence-driven.
- Do not invent institutional facts.
- Do not claim external partners or facilities unless explicitly present in the project files.
```

### Goal of Step 0
Make Claude understand the workspace before editing anything.

---

## Step 1 — Revise the main narrative

```text
Now revise the main narrative.

Primary target file:
- proposal/03_project_narrative.md

Tasks:
1. Rewrite the file into a stronger DOE Phase I 5-page-style project narrative.
2. Preserve the project title and core scientific direction:
   AI-Driven Biomolecular Modeling of H5N1 Antigenic Evolution, Immune Escape, and Cross-Species Adaptation
3. Strengthen alignment with:
   - Topic 2 / Focus Area 2A
   - Phase I expectations for a clear and tangible AI-enabled research workflow
   - explicit and quantitative AI advantage
4. Make the narrative read like a real proposal, not a concept note.
5. Improve:
   - scientific/technical merit and impact
   - technical approach and feasibility
   - management realism
   - Phase I scope discipline
   - Phase II transition logic
6. Do not add unsupported claims.
7. Keep a formal DOE style: concise, credible, non-hyped, reviewer-friendly.

Output requirements:
- Overwrite proposal/03_project_narrative.md
- Then provide:
  1. a section-by-section revision summary
  2. a list of remaining placeholders that still need real information
  3. a list of any statements that may need citations or documentary support
```

### Goal of Step 1
Turn the main narrative into a stronger submission-style draft.

---

## Step 2 — Harmonize the strategy files

```text
Now harmonize the supporting strategy files with the revised narrative.

Target files:
- proposal/04_teaming_plan.md
- proposal/05_management_plan.md
- proposal/06_milestones_9_months.md
- proposal/09_review_criteria_response.md

Tasks:
1. Make these files fully consistent with proposal/03_project_narrative.md.
2. Ensure the same story is told across all files:
   - same project scope
   - same team logic
   - same milestones
   - same evaluation strategy
   - same Phase II transition logic
3. Remove redundancy and contradictions.
4. Make sure the 9-month schedule is realistic and appropriately bounded for Phase I.
5. In the review-criteria file, directly support likely DOE reviewer concerns.

Output requirements:
- Update all four files in place.
- Then provide:
  1. a consistency report
  2. a list of mismatches fixed
  3. a list of unresolved factual placeholders
```

### Goal of Step 2
Make the supporting files match the main narrative and each other.

---

## Step 3 — Review appendix consistency

```text
Now review the appendix package for consistency with the proposal narrative.

Target files include:
- proposal/appendices/appendix_02_facilities_resources.md
- proposal/appendices/appendix_03_equipment.md
- proposal/appendices/appendix_06_transparency_foreign_connections.md
- proposal/appendices/appendix_07_other_attachments.md
- proposal/appendices/letters/*.md

Tasks:
1. Check consistency between the appendices and the main narrative.
2. Ensure institutional names, resource descriptions, and project roles are aligned.
3. Ensure no appendix introduces technical claims that contradict the narrative.
4. Ensure letters read as commitment/access letters, not recommendation letters.
5. Flag any appendix language that sounds too promotional, too vague, or noncompliant.
6. Do not invent names or signatures.

Output requirements:
- Revise files only where needed.
- Then provide:
  1. an appendix compliance checklist
  2. a list of remaining placeholders by file
  3. a list of items that must be completed by humans before submission
```

### Goal of Step 3
Make the appendices compliant and aligned with the narrative.

---

## Step 4 — Red-team review in DOE reviewer mode

```text
Now switch into DOE reviewer mode.

Read the current proposal package as if you are a skeptical but fair Phase I reviewer.

Tasks:
1. Critique the package under the following lenses:
   - scientific/technical merit and impact
   - technical feasibility
   - clarity of AI advantage
   - Topic 2A fit
   - credibility of the 9-month scope
   - team and resource sufficiency
   - weakness of evidence
   - vagueness or overclaiming
2. Identify the top 15 reviewer objections.
3. For each objection, provide:
   - why a reviewer may raise it
   - how serious it is
   - exactly which file and section it affects
   - the best fix

Output requirements:
- Do not revise files yet.
- Return only the red-team review in a structured format.
```

### Goal of Step 4
Expose likely reviewer objections before final polishing.

---

## Step 5 — Fix the most serious weaknesses

```text
Now address the red-team review.

Tasks:
1. Revise the proposal package to fix the most serious reviewer objections.
2. Prioritize:
   - unsupported claims
   - weak Topic 2A alignment
   - vague AI advantage
   - unrealistic milestones
   - unclear team roles
3. Make only justified revisions.
4. Preserve formal DOE proposal style.
5. Do not fabricate partner details, citations, or institutional approvals.

Output requirements:
- Revise relevant files in place.
- Then provide:
  1. a change log
  2. a list of objections fully addressed
  3. a list of objections still dependent on missing real-world information
```

### Goal of Step 5
Strengthen the package without introducing fabricated content.

---

## Step 6 — Final consistency and readiness audit

```text
Run a final proposal consistency and submission-readiness audit.

Tasks:
1. Review the entire package for:
   - internal consistency
   - naming consistency
   - institutional consistency
   - timeline consistency
   - appendix consistency
   - tone consistency
2. Find:
   - duplicated text
   - contradictory statements
   - undefined acronyms
   - missing cross-file alignment
   - weak transitions
   - placeholders still unresolved
3. Produce a final readiness report.

Output requirements:
Return:
1. Submission readiness score (0-100)
2. Top 20 remaining issues
3. Which issues are critical vs non-critical
4. A final ordered to-do list for the human PI/team
Do not revise files in this step unless absolutely necessary.
```

### Goal of Step 6
Produce a final human-facing list of what remains before submission.

---

## Optional Master Control Prompt

Use this once at the beginning if you want Claude Code to adopt the right working mode.

```text
You are operating inside a DOE Genesis Mission Phase I proposal-writing workspace.

Your job is not to brainstorm loosely. Your job is to help produce a credible, compliant, reviewer-friendly proposal package for a 9-month Phase I project under Topic 2 / Focus Area 2A.

Project title:
AI-Driven Biomolecular Modeling of H5N1 Antigenic Evolution, Immune Escape, and Cross-Species Adaptation

Global instructions:
- Read CLAUDE.md and AGENTS.md first and treat them as controlling project guidance.
- Treat proposal/03_project_narrative.md as the central scientific narrative unless revised.
- Keep all other files aligned to the narrative.
- Write in a formal DOE proposal style: precise, compact, non-hyped, defensible.
- Do not invent institutional facts, partner names, approvals, or data access.
- Distinguish clearly between what is already supported in project files and what still needs human confirmation.
- Prefer conservative claims over ambitious but weakly supported claims.
- Keep Phase I tightly scoped to a 9-month demonstration effort with quantitative AI-advantage evaluation.
- Preserve strong alignment with biomolecular structure-function modeling and H5N1 biological relevance.
- When revising files, also report what remains unresolved.
```

---

## Recommended Three-Round Usage Pattern

### Round 1
- Master Control Prompt
- Step 0
- Step 1
- Step 2

### Round 2
- Step 3
- Step 4

### Round 3
- Step 5
- Step 6

This staged workflow is safer and usually produces better results than a one-shot request.

---

## What Not to Ask Claude to Do Automatically

Avoid asking Claude Code to do the following unless you provide the exact facts:

- invent industry partner names
- invent National Lab or user facility names
- invent signatures or institutional titles
- invent data-access approvals
- invent facility-access approvals
- invent bibliography entries
- invent budget numbers
- invent cost share arrangements

These are human-controlled submission items.

---

## Human Inputs That Still Matter Most

Before final submission, the human team should confirm:

1. Lead PI name, appointment, and unit
2. Final participating institutions
3. Industry partner identity
4. National Lab or user facility identity
5. Real project data sources
6. Real benchmark or validation datasets
7. Real access conditions for data/models/software
8. Authorized signatories for letters
9. Final appendix package contents
10. Final budget and institutional approvals

---

## Suggested File Placement

Save this file at:

```text
docs/claude_code_workflow.md
```

This keeps the workflow inside the project and makes it easy to reuse during iterative proposal development.
