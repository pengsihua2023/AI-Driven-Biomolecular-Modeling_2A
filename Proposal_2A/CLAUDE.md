# CLAUDE.md

## Mission
This repository exists to produce a **DOE Genesis Mission FY26 Phase I proposal** for **Focus Area 2A – Biomolecular Science (BER)** under RFA **DE-FOA-0003612**.

Working title:
**AI-Driven Biomolecular Modeling of H5N1 Antigenic Evolution, Immune Escape, and Cross-Species Adaptation**

The primary objective is to create a compliant, persuasive, reviewer-oriented proposal package for a **9-month Phase I project** that demonstrates a clear research workflow, a credible path to **AI advantage**, and a strong rationale for Phase II expansion.

## Ground Truth and Compliance Priority
When there is any conflict between repository notes and sponsor requirements, follow the sponsor requirements.

The controlling source is the uploaded FOA:
- `DE-FOA-0003612.pdf`

Key constraints already confirmed from the FOA:
- Phase I project period: **9 months**.
- Phase I expected award size: **$500,000–$750,000**.
- **Multi-institutional teams are required** for responsive submissions.
- In Phase I, the team must include partner institutions from at least **two** of these categories:
  1. DOE/NNSA National Laboratory or Scientific User Facility
  2. Industry
  3. IHE / Non-profit / Other
- Topic 2 is **Scaling the Biotechnology Revolution**.
- Focus Area 2A is **Biomolecular Science (BER)** and centers on determining principles connecting **protein structure and function**.

## Operating Mode
Work in **document-first mode**.

That means:
1. First produce sponsor-aligned planning and writing documents.
2. Then produce polished proposal text.
3. Only generate code, figures, or tables when they directly support the proposal narrative or a required appendix.
4. Do not wander into side explorations unless they materially strengthen the application.

## Primary Writing Goal
The final writing should read like a strong DOE science proposal:
- technically serious
- concise
- specific
- evidence-based
- modest in claims
- clear about deliverables and evaluation
- explicit about risks and fallback plans

Avoid inflated startup language, vague futurism, and generic AI hype.

## Proposal Framing for This Repository
This proposal should frame H5N1 as a **high-consequence biomolecular modeling problem** relevant to biotechnology, biosecurity, and predictive biology.

The central scientific frame is:
- H5N1 evolution alters **HA antigenicity**, **immune recognition**, and **host adaptation**.
- Existing approaches often treat sequence, structure, antigenic escape, and host adaptation as separate tasks.
- The proposed work builds an AI-driven biomolecular workflow that links:
  - viral sequence variation
  - structural representation of HA and related biomolecular interfaces
  - antigenic evolution and immune escape prediction
  - cross-species adaptation signals
  - quantitative evaluation of AI advantage

## What Counts as Success in Phase I
Phase I is not a full-scale translational program. It must show a **clear, tangible research workflow** with quantitative evidence that the approach is on a trajectory toward transformative capability.

For this repository, successful Phase I writing should therefore emphasize:
- a tightly scoped but credible 9-month plan
- curated benchmark datasets and clearly defined tasks
- measurable scientific and modeling improvements
- concrete AI advantage metrics
- reproducible workflows and FAIR-minded outputs
- a realistic Phase II transition plan

## Non-Negotiable Writing Rules
- Always align language to **DOE / BER / Genesis Mission** priorities.
- Always connect the proposed work to **AI-enabled scientific discovery**, not just routine ML model building.
- Always state what the model will predict, on what data, and how success will be measured.
- Always distinguish:
  - observation vs interpretation
  - model performance vs scientific insight
  - Phase I demonstration vs Phase II scale-up
- Always include risks, limitations, and fallback options.
- Never imply validated public-health deployment unless the proposal truly includes that scope.
- Never overclaim “real-time surveillance,” “pandemic prevention,” or “clinical utility” without a directly supported work package.
- Never present speculative biology as established fact.
- Never promise unavailable data, compute, personnel, or partnerships.

## Preferred Scientific Vocabulary
Prefer:
- biomolecular modeling
- protein structure–function relationships
- antigenic evolution
- immune escape
- cross-species adaptation
- host range–relevant mutations
- structure-informed representation learning
- benchmarked predictive workflow
- quantitative evaluation
- AI advantage
- reproducible scientific workflow
- uncertainty-aware prediction
- interpretable latent representation

Use carefully:
- foundation model
- agentic AI
- digital twin
- autonomous discovery
- transformative
- platform

Avoid unless justified:
- revolutionary
- game-changing
- world-leading
- unprecedented
- cure
- prevent pandemics
- real-time operational deployment

## Expected Repository Outputs
The repository should eventually contain:
- FOA alignment memo
- one-page concept
- outline
- Project Narrative draft
- management/teaming plan
- milestone table
- risk register
- Phase II transition memo
- reviewer-criteria crosswalk
- templates for letters and appendices
- Claude rules and skills for consistent drafting and review

## File Priorities
High priority files:
- `proposal/00_foa_alignment.md`
- `proposal/01_one_page_concept.md`
- `proposal/02_outline.md`
- `proposal/03_project_narrative.md`
- `proposal/06_milestones_9_months.md`
- `proposal/09_review_criteria_response.md`
- `docs/sponsor/doe_phase1_rules.md`
- `docs/sponsor/compliance_checklist.md`
- `docs/science/ai_advantage_definition.md`
- `docs/science/validation_strategy.md`
- `.claude/rules/proposal_writing.md`
- `.claude/rules/doe_compliance.md`

## Review Heuristics
Every substantial draft should be checked against these questions:
1. Is the proposal obviously responsive to Focus Area 2A?
2. Is the project narrow enough for 9 months?
3. Does the work show a tangible workflow rather than a vague vision?
4. Are the data, models, and tasks explicitly defined?
5. Is AI advantage operationalized with metrics rather than slogans?
6. Are team roles and partnerships necessary and credible?
7. Does the narrative explain why DOE should fund this rather than another agency?
8. Is the Phase II path visible but not overbuilt into Phase I?
9. Are claims calibrated to available evidence?
10. Would a skeptical reviewer understand exactly what is delivered at month 9?

## How to Draft
When drafting, usually follow this sequence:
1. Re-read `proposal/00_foa_alignment.md`.
2. Re-read `docs/sponsor/doe_phase1_rules.md` and `docs/sponsor/compliance_checklist.md`.
3. Re-read the science framing files in `docs/science/`.
4. Draft in outline-first form.
5. Convert outline bullets into prose.
6. Run a compliance pass.
7. Run a reviewer-style red-team pass.
8. Tighten wording for concision and specificity.

## When Asked to Revise Text
Unless the user says otherwise, revise toward:
- greater sponsor alignment
- greater clarity
- tighter scope
- more measurable deliverables
- more explicit evaluation
- less hype
- stronger Phase I realism

## Do Not Do These Things
- Do not silently change the project title without flagging it.
- Do not invent partner institutions or named personnel.
- Do not fabricate preliminary data.
- Do not cite literature that has not been verified.
- Do not convert the proposal into an NIH-style disease-mechanism grant.
- Do not turn the proposal into a generic AI-for-biology application disconnected from BER Focus Area 2A.
- Do not assume the page limit unless the FOA section has been checked.

## Default Output Style
Use polished scientific prose in Markdown.
When helpful, provide:
- short headings
- compact bullet lists
- milestone tables
- reviewer-oriented checklists

## Final Reminder
This repository is for **winning a DOE Phase I proposal**, not for writing a review article, not for building a production software system, and not for speculative science fiction. Favor sponsor-fit, scientific precision, and executable planning over breadth.
