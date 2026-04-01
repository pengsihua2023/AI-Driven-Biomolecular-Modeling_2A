# 06_milestones_9_months.md

## 9-Month Phase I Milestones and Go/No-Go Plan

**Project Title:** AI-Driven Biomolecular Modeling of H5N1 Antigenic Evolution, Immune Escape, and Cross-Species Adaptation  
**RFA:** DOE Genesis Mission, DE-FOA-0003612  
**Topic / Focus Area:** Topic 2 – Scaling the Biotechnology Revolution; Focus Area A – Biomolecular Science (BER)  
**Project Period:** 9 months (Phase I)

## Purpose of this milestone plan

This plan is designed for a **Phase I** Genesis Mission application, where the project must establish a **clear, tangible AI-enabled research workflow** and provide **concrete evaluation of AI advantage**. DOE states that Phase I success may include improved predictive power or scientific insight, tighter coupling of data and experiments, new models that accelerate discovery, scaling metrics, or faster workflows; the aim is a **quantitative analysis** showing that the project is on a trajectory toward a transformative scientific capability. fileciteturn18file2

The milestones below are therefore written to do four things at once:

1. Produce a credible biomolecular modeling workflow aligned with **2A Biomolecular Science**, which emphasizes connecting **protein structure and function** and integrating structural characterization with genomics and other omics for functional analysis. fileciteturn19file0turn19file3
2. Demonstrate measurable **AI advantage** using explicit baseline comparisons, calibration metrics, prospective tests, and workflow-speed metrics. fileciteturn18file2
3. Fit the practical constraints of a **9-month Phase I small-team project**. fileciteturn18file1
4. Generate a disciplined **Phase II transition package** if the Phase I evidence supports scale-up. DOE indicates that Phase II is intended to expand the most promising Phase I directions at roughly 3–5× the Phase I level of effort. fileciteturn18file2turn18file1

---

## Overall Phase I objectives

### Objective 1. Build an integrated H5N1 biomolecular AI workflow
Develop a reproducible workflow that integrates sequence variation, structural representations, antigenic annotations, receptor-binding context, and host-related metadata to model three linked biological questions:

- **Antigenic evolution** of H5N1 HA
- **Immune escape** from known or inferred antibody-sensitive regions
- **Cross-species adaptation**, especially biomolecular features associated with avian-to-mammalian host shift

### Objective 2. Demonstrate quantitative AI advantage
Show that the proposed AI workflow outperforms or complements non-AI and simpler ML baselines in one or more of the following DOE-relevant ways:

- better prediction accuracy or calibration,
- better ranking of candidate variants for experimental follow-up,
- faster hypothesis generation,
- improved structure-function interpretation,
- improved scaling with more data or compute. fileciteturn18file2

### Objective 3. Produce a Phase II-ready evidence package
Deliver a prioritized expansion plan for a larger multi-institution effort, including validated datasets, documented workflows, benchmark results, risk-retirement status, and clearly justified next-stage experimental and computational aims.

---

## Work package structure

### WP1. Data foundation and benchmark definition
Curate the Phase I modeling corpus, define benchmark tasks, establish inclusion/exclusion rules, and lock evaluation splits.

### WP2. Multi-modal model development
Build the AI stack for sequence, structure, and mechanism-aware prediction.

### WP3. Mechanistic interpretation and validation
Interrogate learned representations against known structure-function biology and evaluate whether the model provides biologically interpretable insight.

### WP4. Workflow demonstration and AI-advantage analysis
Demonstrate end-to-end performance on realistic use cases and quantify gains over baselines.

### WP5. Reproducibility, transition, and submission packaging
Prepare the documentation and artifacts needed for a strong Phase II case and downstream DOE integration logic.

---

## Month-by-month milestone plan

## Month 1: Project launch, data inventory, and scope lock

### Technical goals
- Finalize scientific scope around HA antigenic change, immune escape proxy labels, and host adaptation targets.
- Inventory all candidate data sources and classify them as:
  - sequence-only,
  - sequence + structure,
  - sequence + phenotype,
  - sequence + host/species metadata,
  - external validation / holdout-only.
- Define the minimum viable Phase I benchmark suite.
- Freeze naming conventions, data provenance rules, and versioning procedures.

### Deliverables
- `data_inventory_v1.csv`
- `benchmark_definition_v1.md`
- `assumptions_and_exclusions.md`
- `reproducibility_manifest_v1.md`

### Success criteria
- At least **three benchmark tasks** are defined and accepted by the team.
- Every planned dataset has recorded provenance, schema, and intended use.
- External holdout set policy is documented before any model training begins.

### Go/No-Go checkpoint A
**Go** if the team can define a coherent benchmark suite with enough data diversity to support at least one robust predictive task and one interpretation task.  
**No-Go / re-scope** if the available data are too sparse or too inconsistent to support defensible Phase I evaluation.

---

## Month 2: Curation, harmonization, and baseline setup

### Technical goals
- Clean and harmonize sequence, structural, and metadata fields.
- Resolve deduplication, clade naming, host-species harmonization, and missingness handling.
- Build transparent baseline models:
  - rule-based or literature-derived baselines,
  - classical ML baselines on engineered features,
  - simpler deep learning baselines on sequence alone.
- Define primary metrics and confidence reporting.

### Deliverables
- `curated_dataset_v1/`
- `data_dictionary_v1.md`
- `baseline_models_spec.md`
- `evaluation_metrics_plan.md`

### Success criteria
- Train/validation/test split is locked.
- At least **two non-AI or low-complexity baselines** and **one sequence-only ML baseline** are runnable.
- Missing-data policy and leakage-prevention checks are documented.

### AI-advantage measurements initiated
- Accuracy / AUROC / AUPRC / correlation as applicable
- calibration error
- top-k retrieval / ranking utility
- compute and turnaround time per experiment round

---

## Month 3: Structure-aware representation pipeline

### Technical goals
- Construct the biomolecular representation layer linking sequence variation to structure-function context.
- Generate residue-level and region-level features for:
  - antigenically relevant HA sites,
  - receptor-binding regions,
  - glycosylation-related context,
  - mutation neighborhood / contact context,
  - optional partner proteins or adaptation markers where data permit.
- Build the first structure-aware multimodal model.

### Deliverables
- `feature_pipeline_v1/`
- `structure_mapping_qc_report.md`
- `multimodal_model_v1_spec.md`
- `training_run_log_m3.md`

### Success criteria
- Structure-aware features are generated reproducibly for the majority of benchmarked variants.
- Multimodal model training runs complete successfully.
- First-pass comparison against sequence-only baseline is available.

### Go/No-Go checkpoint B
**Go** if structure-aware modeling shows either measurable performance gain or improved mechanistic interpretability over sequence-only baselines.  
**Fallback** if no gain appears: simplify to a focused structure-informed rescoring or ranking workflow rather than a full multimodal predictor.

---

## Month 4: Immune escape modeling and uncertainty calibration

### Technical goals
- Build the immune-escape scoring component.
- Add uncertainty-aware prediction and confidence calibration.
- Evaluate whether the model can prioritize variants with higher likelihood of antigenic shift or escape-related change.
- Begin ablation studies to isolate the value of structure, metadata, and mechanistic priors.

### Deliverables
- `immune_escape_model_v1/`
- `uncertainty_and_calibration_report.md`
- `ablation_plan_v1.md`
- `midpoint_results_deck.md`

### Success criteria
- Calibrated ranking output is available for candidate H5N1 variants.
- At least one ablation study is complete.
- Uncertainty estimates are usable for decision support, not just raw scores.

### Quantitative targets
Target values will be finalized once the benchmark is locked, but Phase I should aim to demonstrate at least one of the following versus the strongest baseline:

- **≥10% relative improvement** in a primary prediction metric,
- **≥20% improvement** in top-k prioritization yield,
- **≥2× improvement** in candidate triage speed,
- materially improved calibration or error concentration in biologically critical regions.

These are internal project targets rather than FOA-mandated thresholds.

---

## Month 5: Cross-species adaptation modeling

### Technical goals
- Build the cross-species adaptation component centered on biomolecular determinants of host shift.
- Integrate host metadata and receptor-binding relevant features into the model stack.
- Evaluate whether the workflow can distinguish or rank variants by adaptation-relevant signatures.
- Assess transferability across clades or time windows.

### Deliverables
- `cross_species_model_v1/`
- `host_metadata_harmonization.md`
- `temporal_generalization_report.md`
- `adaptation_case_studies_v1.md`

### Success criteria
- Model generates biologically plausible host-shift rankings or classifications.
- Temporal or clade holdout performance is reported.
- Failure modes are categorized rather than hidden.

### Go/No-Go checkpoint C
**Go** if at least one adaptation-focused use case shows reproducible value on strict holdout evaluation.  
**Re-scope** if adaptation labels are too weak, by repositioning this task as mechanistic prioritization rather than definitive prediction.

---

## Month 6: End-to-end workflow demonstration

### Technical goals
- Integrate the three modules into a single demonstrator workflow:
  1. ingest candidate variants,
  2. compute structure-aware representations,
  3. estimate antigenic evolution / escape / adaptation scores,
  4. generate uncertainty and rationale summaries,
  5. produce ranked outputs for expert review.
- Measure end-to-end runtime, reproducibility, and operator effort.

### Deliverables
- `workflow_demo_v1/`
- `end_to_end_runtime_benchmark.md`
- `user_story_examples.md`
- `workflow_qc_checklist.md`

### Success criteria
- A new input panel of variants can be processed from raw inputs to ranked report without ad hoc manual intervention.
- Runtime and reproducibility are documented.
- Demonstrator is stable enough for partner feedback.

### AI-advantage focus
This milestone is where the project directly addresses the FOA’s emphasis on a **clear, tangible research workflow** and not just a collection of disconnected models. fileciteturn18file2

---

## Month 7: External validation and partner-facing review

### Technical goals
- Evaluate the workflow on strict external or temporally separated holdout data.
- Conduct partner review sessions with academic, national-lab, and/or industry collaborators.
- Identify which outputs are credible enough for Phase II expansion.

### Deliverables
- `external_validation_report.md`
- `partner_feedback_summary.md`
- `error_analysis_v1.md`
- `phase2_gap_analysis.md`

### Success criteria
- External validation is completed and honestly reported.
- Error categories are tied to next-step fixes.
- At least one partner confirms the workflow is scientifically useful for follow-up prioritization.

### Go/No-Go checkpoint D
**Go to Phase II planning** if the workflow demonstrates value on external data and the team can clearly state what larger-scale effort would buy.  
**Do not escalate** if performance collapses on external validation without a credible explanation or remediation path.

---

## Month 8: Consolidation, reproducibility hardening, and transition package

### Technical goals
- Harden documentation, code packaging, and reproducibility records.
- Finalize benchmark tables, ablation results, calibration plots, and case studies.
- Prepare the scientific narrative for why the approach is on a trajectory toward transformative capability.

### Deliverables
- `reproducibility_package_v1/`
- `benchmark_tables_final.csv`
- `figures_for_phase2_package/`
- `phase2_concept_v1.md`

### Success criteria
- All primary results can be regenerated from versioned inputs.
- The project can state, with evidence, what AI contributed beyond conventional approaches.
- Transition artifacts are ready for insertion into a Phase II concept package.

---

## Month 9: Final analysis, decision memo, and submission-ready closeout

### Technical goals
- Produce the final Phase I synthesis.
- Explicitly map results to DOE Phase I success logic.
- Write a go/no-go memo for Phase II, including scale-up priorities, team expansion logic, and infrastructure requirements.

### Deliverables
- `phase1_final_technical_report.md`
- `ai_advantage_quantification_memo.md`
- `phase2_go_no_go_decision_memo.md`
- `final_milestone_completion_matrix.md`

### Success criteria
- Final report includes quantitative comparison to baselines and explicit lessons learned.
- Phase II rationale is supported by data, not aspiration.
- Remaining risks are clearly identified with mitigation plans.

---

## Milestone completion matrix

| Milestone | Month | Primary output | Evidence of completion |
|---|---:|---|---|
| M1 Scope and benchmark lock | 1 | Benchmark suite | Approved benchmark definition and data inventory |
| M2 Curated dataset + baselines | 2 | Curated corpus and baseline models | Frozen splits, reproducible baseline runs |
| M3 Structure-aware model v1 | 3 | Multimodal model | First-pass comparison vs sequence-only baseline |
| M4 Escape model + calibration | 4 | Ranked immune-escape outputs | Calibration report and ablation results |
| M5 Adaptation model | 5 | Host-shift prediction/prioritization | Holdout performance and case studies |
| M6 End-to-end workflow demo | 6 | Integrated pipeline | Reproducible variant-to-report workflow |
| M7 External validation | 7 | Strict holdout evaluation | External validation and error analysis |
| M8 Reproducibility hardening | 8 | Transition package | Regenerable benchmark tables and documented workflow |
| M9 Phase I synthesis | 9 | Final technical and go/no-go package | Final report and Phase II decision memo |

---

## Primary quantitative evaluation framework

Because DOE explicitly asks whether Phase I projects can provide **quantitative analysis** of trajectory toward transformative capability, the project will report metrics in five categories. fileciteturn18file2

### 1. Predictive performance
- AUROC / AUPRC / F1 / correlation, as appropriate to each benchmark
- top-k enrichment for candidate prioritization
- performance on temporally or phylogenetically separated holdouts

### 2. Calibration and trustworthiness
- expected calibration error
- confidence-stratified error rate
- uncertainty-aware abstention utility

### 3. Mechanistic utility
- consistency of highlighted residues or regions with known structure-function biology
- enrichment of biologically plausible sites among top-ranked drivers
- interpretability review by domain experts

### 4. Workflow acceleration
- wall-clock time from variant intake to ranked output
- reduction in manual triage burden
- number of candidate variants that can be screened per cycle

### 5. Scaling behavior
- performance as a function of data volume
- performance as a function of compute budget
- marginal value of adding structure and omics-derived context

---

## Risk register tied to milestones

### Risk 1: Label sparsity or weak phenotypic supervision
**Impact:** limits robust supervised learning.  
**Mitigation:** use ranking tasks, weak supervision, transfer learning, and strict uncertainty reporting.  
**Affected milestones:** M2–M5.

### Risk 2: Structure coverage is incomplete or inconsistent
**Impact:** weakens multimodal modeling.  
**Mitigation:** allow hierarchical fallback from full structure-aware modeling to region-aware or feature-engineered structural context.  
**Affected milestones:** M3–M4.

### Risk 3: External validation underperforms
**Impact:** weak Phase II case.  
**Mitigation:** use temporally separated holdouts early, track domain shift, and present failure analysis honestly.  
**Affected milestones:** M5–M7.

### Risk 4: Workflow is accurate but not operationally useful
**Impact:** limited demonstration of AI advantage.  
**Mitigation:** measure runtime, triage efficiency, and end-to-end usability from M6 onward.  
**Affected milestones:** M6–M9.

### Risk 5: Project becomes too broad for 9 months
**Impact:** fragmented outputs.  
**Mitigation:** retain a core benchmark and demote secondary tasks if needed at Go/No-Go checkpoints B or C.  
**Affected milestones:** all months.

---

## Phase II transition logic

DOE’s Phase II vision is to expand the most promising Phase I directions after quantitative evidence is established. fileciteturn18file2turn18file1 The project will recommend Phase II only if the following conditions are met:

1. **Technical evidence:** at least one major benchmark shows clear advantage over the strongest baseline.
2. **Mechanistic value:** outputs improve understanding of structure-function relationships relevant to H5N1 antigenic evolution, escape, or adaptation.
3. **Workflow value:** the integrated system reduces discovery-cycle friction, not merely prediction error.
4. **External credibility:** at least one external validation or partner review supports usefulness.
5. **Scale-up logic:** the team can articulate what additional data, partners, compute, or experimental coupling would enable in a larger effort.

If these conditions are met, Phase II would expand from proof-of-concept modeling to a broader, better-instrumented program involving larger datasets, deeper experimental coupling, more rigorous prospective validation, and stronger integration with DOE-scale AI and data infrastructure.

---

## Notes for integration into the proposal package

- This file is intentionally more detailed than what will appear in the 5-page Project Narrative.
- The main narrative should summarize this plan in a compact milestone table plus one short paragraph on go/no-go logic.
- The detailed logic here is best used by Claude Code as working context for drafting the narrative, management plan, and review-criteria response.

