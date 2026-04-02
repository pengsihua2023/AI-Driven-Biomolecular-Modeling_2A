# Runbook for Operating Claude Code on the DOE Genesis Mission Phase I Proposal

## Purpose

This runbook is the operator-facing companion to `docs/claude_code_workflow.md`.

If `claude_code_workflow.md` tells Claude Code **what to do**, this runbook tells the human operator **how to run the process well**, **what outputs to inspect**, **how to judge quality**, and **when to stop, accept, or send Claude back for revision**.

**Project Title:**  
AI-Driven Biomolecular Modeling of H5N1 Antigenic Evolution, Immune Escape, and Cross-Species Adaptation

**Proposal Context:**  
DOE Genesis Mission, Phase I, 9-month project, Topic 2 / Focus Area 2A

---

## 1. What This Runbook Is For

Use this runbook when you want to turn Claude Code into a controlled writing assistant for a DOE proposal rather than a free-form brainstorming tool.

This runbook helps you:
- operate Claude Code in stages;
- avoid common proposal-writing failure modes;
- spot weak outputs early;
- prevent factual drift across files;
- decide when a draft is strong enough to keep;
- decide when Claude should revise again;
- keep humans in control of institutional facts, partner details, and submission-critical content.

---

## 2. Ground Rules Before You Start

Before you run any workflow steps, confirm the following:

### 2.1 Project files exist
You should already have:
- `CLAUDE.md`
- `AGENTS.md`
- `proposal/03_project_narrative.md`
- `proposal/04_teaming_plan.md`
- `proposal/05_management_plan.md`
- `proposal/06_milestones_9_months.md`
- `proposal/09_review_criteria_response.md`
- `proposal/appendices/...`
- `docs/claude_code_workflow.md`

### 2.2 Claude is not the source of truth for institutional facts
Claude may reorganize and improve prose, but it must not be trusted to invent:
- partner names,
- signatories,
- access approvals,
- National Lab relationships,
- budget details,
- cost share,
- data rights,
- institutional authorizations.

### 2.3 Narrative-first rule
The main scientific story should live in:
- `proposal/03_project_narrative.md`

Other files should support that file, not compete with it.

### 2.4 Phase I discipline rule
Every file should remain consistent with a:
- **9-month Phase I scope**
- **clear and tangible AI-enabled research workflow**
- **quantitative AI advantage**
- **credible, bounded deliverables**

If a file starts sounding like a 3-year center proposal, it needs revision.

---

## 3. Recommended Operating Sequence

Run Claude Code in the following order:

### Round 1
1. Master control prompt
2. Step 0 — Read the workspace
3. Step 1 — Revise the narrative
4. Step 2 — Harmonize support files

### Round 2
5. Step 3 — Review appendices
6. Step 4 — DOE reviewer-mode red team

### Round 3
7. Step 5 — Fix serious weaknesses
8. Step 6 — Final readiness audit

Do not skip directly to the final audit before the narrative and support files are stabilized.

---

## 4. How to Judge Each Step

---

## Step 0 — Read the Workspace Only

### What you ask Claude to do
Claude reads the workspace and returns:
- project structure map
- missing factual inputs
- writing risks
- highest-priority files

### What a good output looks like
A strong Step 0 output should:
- correctly identify the central proposal files;
- recognize the DOE Phase I context;
- understand Topic 2A alignment;
- list real missing information rather than generic filler;
- flag actual risks such as overclaiming, vague AI advantage, or placeholder partner roles.

### What a weak output looks like
Reject or rerun if Claude:
- summarizes only superficially;
- misses obvious files;
- gives generic academic-writing advice instead of proposal-specific risks;
- fails to identify missing factual inputs;
- starts revising files even though it was told not to.

### Acceptance criteria
Accept Step 0 only if:
- the file map is mostly correct;
- the missing inputs are specific and useful;
- the identified risks would genuinely matter to a DOE reviewer.

### Operator action after Step 0
Save the output somewhere useful, such as:
- `internal/step0_workspace_assessment.md`

This becomes a diagnostic baseline.

---

## Step 1 — Revise the Main Narrative

### What you ask Claude to do
Claude rewrites:
- `proposal/03_project_narrative.md`

### What a good output looks like
A strong narrative revision should:
- sound like a real proposal rather than a concept memo;
- make the science problem clear early;
- explain why H5N1 biomolecular modeling matters;
- connect strongly to Topic 2A;
- define the AI-enabled workflow clearly;
- explain AI advantage in measurable terms;
- keep the project scoped to a realistic 9-month Phase I;
- avoid hype and vague claims;
- make the transition to Phase II plausible but not overblown.

### Warning signs
Reject or revise if the narrative:
- sounds like marketing copy;
- overuses words like transformative, revolutionary, paradigm-shifting without evidence;
- drifts away from biomolecular structure-function logic;
- treats Phase I like a full deployment project;
- introduces unsupported partner capabilities;
- becomes too long, repetitive, or diffuse;
- mentions milestones or data sources that are not reflected elsewhere.

### Acceptance criteria
Accept Step 1 only if:
- the opening problem statement is sharp;
- the scientific objective is understandable;
- the workflow is concrete;
- AI advantage is framed as something that can be tested quantitatively;
- the tone feels reviewer-oriented rather than promotional.

### Operator action after Step 1
Read the file manually and ask:
1. Could a reviewer explain this project after one read?
2. Is the central workflow concrete?
3. Does this still look like a 9-month project?
4. Would I be embarrassed defending any sentence as unsupported?

If the answer to 3 or 4 is problematic, send Claude back.

---

## Step 2 — Harmonize the Support Files

### What you ask Claude to do
Claude revises:
- `proposal/04_teaming_plan.md`
- `proposal/05_management_plan.md`
- `proposal/06_milestones_9_months.md`
- `proposal/09_review_criteria_response.md`

### What a good output looks like
The files should:
- tell the same story as the narrative;
- use the same project scope and logic;
- align team roles with actual project tasks;
- keep milestones realistic;
- make review-criteria responses feel grounded in the actual proposal.

### Common failure modes
Reject or revise if:
- milestones do not match the narrative;
- the team plan implies partners the narrative does not mention;
- the management plan introduces committees, workflows, or governance structures that feel too large for Phase I;
- the review-criteria document sounds generic and disconnected from the actual project.

### Acceptance criteria
Accept only if:
- the files are visibly consistent;
- you no longer see conflicting timelines;
- the support files make the main narrative stronger, not more confusing.

### Operator action after Step 2
Create a quick consistency check:
- project objective
- team composition
- AI advantage
- milestones
- deliverables
- Phase II transition

If these six items read differently across files, the package is not ready for Round 2.

---

## Step 3 — Review Appendix Consistency

### What you ask Claude to do
Claude checks the appendix package and letter templates.

### What a good output looks like
A strong appendix review should:
- align institutional names and resource descriptions;
- keep appendix claims modest and factual;
- ensure letters read as commitment/access letters, not endorsements;
- identify placeholders clearly;
- keep appendices from making unsupported technical claims.

### Common failure modes
Reject or revise if:
- appendices contain stronger claims than the main narrative;
- letters sound like praise letters;
- letters promise resources or support that are not confirmed;
- appendix text introduces new science claims that should have stayed in the narrative.

### Acceptance criteria
Accept only if:
- appendices are factual and restrained;
- letters are one-page style and functional;
- placeholders are clearly visible and not hidden inside polished prose.

### Operator action after Step 3
Highlight all remaining placeholders in a separate list:
- names
- titles
- institution names
- access conditions
- signatories
- partner roles

This is your human-closeout list.

---

## Step 4 — DOE Reviewer-Mode Red Team

### What you ask Claude to do
Claude critiques the proposal package instead of revising it.

### What a good output looks like
The red-team output should:
- identify real reviewer objections;
- prioritize serious weaknesses;
- point to exact files and sections;
- explain why the issue matters;
- suggest fixes that are actually doable.

### What a weak output looks like
Reject or rerun if Claude:
- gives only mild praise with generic comments;
- fails to identify hard objections;
- does not distinguish major vs minor weaknesses;
- proposes fixes that require invented facts.

### Acceptance criteria
Accept only if:
- the objections feel plausible;
- at least several are uncomfortable but true;
- the list gives you a real basis for improvement.

### Operator action after Step 4
Do not get defensive.  
This is one of the highest-value steps in the workflow.

Take the top 5 objections and ask:
- Would a DOE reviewer really think this?
- Do we already have the information needed to fix it?
- Is the problem wording, evidence, scope, or logic?

---

## Step 5 — Fix the Most Serious Weaknesses

### What you ask Claude to do
Claude revises the package based on the red-team review.

### What a good output looks like
A strong Step 5 revision should:
- fix high-severity issues first;
- reduce overclaiming;
- make AI advantage more concrete;
- tighten Topic 2A fit;
- make milestones more credible;
- improve role clarity without inventing facts.

### Common failure modes
Reject or revise if:
- Claude “fixes” issues by fabricating information;
- the proposal becomes dull and loses scientific sharpness;
- the red-team objections are ignored;
- the revised files no longer align.

### Acceptance criteria
Accept only if:
- the worst issues are visibly improved;
- the proposal is stronger and more credible than before;
- no new unsupported content has been introduced.

### Operator action after Step 5
Compare before and after versions of:
- narrative opening
- AI advantage section
- milestones
- team roles
- Topic 2A framing

If these are not clearly better, do another revision pass.

---

## Step 6 — Final Readiness Audit

### What you ask Claude to do
Claude runs a final consistency and readiness audit.

### What a good output looks like
A strong audit should:
- identify remaining critical issues cleanly;
- distinguish critical vs non-critical;
- give a realistic readiness score;
- produce a human to-do list that is concrete and ordered.

### What a weak output looks like
Reject or rerun if:
- the audit says everything is basically ready when obvious placeholders remain;
- the readiness score is inflated;
- the to-do list is vague;
- file-specific problems are not named.

### Acceptance criteria
Accept only if:
- the final issues list is practical;
- it clearly separates writing issues from human-administrative issues;
- the readiness score feels honest.

### Operator action after Step 6
Use the audit to build the final human submission checklist.

Do not ask Claude for yet another rewrite unless the remaining issues are actually text problems rather than missing real-world inputs.

---

## 5. The Fast Human Evaluation Checklist

Use this short checklist after any major Claude revision.

### Science and fit
- Is the biological problem clear?
- Is the Topic 2A fit explicit?
- Is the structure-function connection visible?
- Is H5N1 relevance scientifically credible?

### AI logic
- Is the AI workflow concrete?
- Is AI advantage measurable?
- Are baselines implied or stated?
- Is evaluation plausible in 9 months?

### Proposal discipline
- Does the scope fit Phase I?
- Are deliverables bounded?
- Is Phase II mentioned without overselling?

### Team and resources
- Are the institutional roles believable?
- Do the resources support the claims?
- Are partner roles substantive rather than decorative?

### Tone and writing
- Is the prose precise?
- Is the document readable by a busy reviewer?
- Are there obvious unsupported claims?
- Does anything sound like hype?

If multiple answers are “no,” do not move to the next round yet.

---

## 6. Common Failure Patterns and What to Do

### Failure pattern 1: Claude gets generic
**Symptom:** The writing sounds like a general academic summary.  
**Fix:** Re-prompt with emphasis on DOE reviewer expectations, Phase I discipline, and quantitative AI advantage.

### Failure pattern 2: Claude becomes too promotional
**Symptom:** Too many grand claims, not enough concrete demonstration logic.  
**Fix:** Ask Claude to cut hype, reduce adjectives, and state claims in testable terms.

### Failure pattern 3: Claude invents details
**Symptom:** New partner names, approvals, access conditions, or data claims appear.  
**Fix:** Revert and explicitly instruct Claude to use placeholders instead of invention.

### Failure pattern 4: Files drift apart
**Symptom:** Narrative, milestones, and team plan no longer match.  
**Fix:** Re-run the harmonization step before any further polishing.

### Failure pattern 5: Phase I becomes too big
**Symptom:** The project reads like a center-scale or Phase II project.  
**Fix:** Reduce scope, shorten deliverables, reframe outcomes as demonstration rather than full realization.

### Failure pattern 6: Red team is too soft
**Symptom:** The critique is polite but not useful.  
**Fix:** Ask again and explicitly request skeptical reviewer objections with severity ranking.

---

## 7. When to Stop Revising

You should usually stop asking Claude for more writing revisions when:
- the remaining issues are mostly human-administrative;
- the remaining placeholders require real institutional decisions;
- further editing only changes wording without improving credibility;
- the proposal already reads as coherent, scoped, and defensible.

Over-editing can flatten a proposal and create new inconsistencies.

---

## 8. What Humans Must Still Own

Even after Claude has done excellent work, humans still need to finalize:

- lead PI identity
- appointment and eligibility
- final institutions
- partner commitments
- National Lab or user facility participation
- signatories
- data-access conditions
- budget and cost share
- final appendix contents
- compliance review
- submission formatting

Claude can support these processes, but it should not control them.

---

## 9. Recommended Folder for Internal Outputs

It is useful to save Claude’s diagnostic outputs in a non-submission folder such as:

```text
internal/
  step0_workspace_assessment.md
  redteam_review_round1.md
  change_log_round2.md
  final_readiness_audit.md
```

This keeps your thinking organized and makes it easier to track what changed.

---

## 10. Suggested Operating Habit

A good working habit is:

1. Run one workflow step
2. Read Claude’s output yourself
3. Decide whether it passes
4. Save the result
5. Only then move to the next step

Do not chain too many revisions without reading them.  
The human operator is the quality-control layer.

---

## 11. Final Advice

The goal is not to make Claude sound smart.  
The goal is to produce a proposal package that a DOE reviewer can trust.

That means:
- concrete claims,
- realistic scope,
- consistent story,
- restrained tone,
- strong internal alignment,
- and clear separation between what is known and what still requires human confirmation.

Save this file at:

```text
docs/runbook.md
```
