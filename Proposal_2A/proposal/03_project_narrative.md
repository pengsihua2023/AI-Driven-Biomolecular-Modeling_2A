# Project Narrative

**Project Title:** AI-Driven Biomolecular Modeling of H5N1 Antigenic Evolution, Immune Escape, and Cross-Species Adaptation  
**Topic / Focus Area:** Topic 2 – Scaling the Biotechnology Revolution; Focus Area A – Biomolecular Science (BER)  
**Project Period:** Phase I (9 months)  
**Project Type:** Fundamental research with AI-enabled scientific workflow development

## 1. Overview and Relevance to Focus Area 2A

We propose to build and validate an AI-driven biomolecular modeling workflow that connects H5N1 sequence variation to structural and functional consequences—specifically, antigenic evolution, immune escape, and cross-species adaptation of hemagglutinin (HA). The work directly addresses **Topic 2, Focus Area A: Biomolecular Science (BER)** and its emphasis on discovering principles that connect protein structure with function.

H5N1 is an ideal model system for this challenge. The phenotypes that determine human risk—antigenic drift, antibody escape, altered receptor preference, and mammalian host adaptation—arise from coupled changes in biomolecular structure. Yet current analysis pipelines fragment these phenomena: genomic surveillance tracks substitutions without structural context, structural biology resolves individual complexes but cannot cover mutational combinatorics at surveillance scale, and most machine-learning approaches ignore three-dimensional architecture, glycosylation context, and epistatic coupling. No existing framework integrates these modalities into a single, benchmarked predictive workflow.

**Central hypothesis.** Multimodal, structure-aware AI models that jointly encode sequence, three-dimensional residue context, glycoprotein features, mutational constraint, and host/antibody interaction data will improve prediction of H5N1 antigenic evolution, immune escape potential, and cross-species adaptation relative to sequence-only baselines, while producing interpretable residue- and epitope-level hypotheses suitable for experimental follow-up.

Phase I will deliver a sharply scoped, nine-month demonstration: a reproducible workflow judged by three measurable outcomes—improved predictive performance over rigorous baselines, stronger mechanistic interpretability, and better prioritization of experimentally relevant mutations and variant combinations.

## 2. Scientific Opportunity and the Case for AI Advantage

The core scientific gap is that no current method links H5N1 sequence variation to structural and functional consequence in a unified, scalable, benchmarked workflow. Sequence frequency does not predict whether a substitution will alter antigenicity. Physics-based structural modeling is informative but computationally expensive at surveillance scale. Most machine-learning approaches treat sequence, structure, and phenotype as separate prediction problems, forfeiting the mechanistic coupling that governs real viral evolution.

AI advantage in this project will arise from four specific capabilities that no single existing approach provides:

1. **Multimodal data fusion.** Joint encoding of sequence, three-dimensional structure, epitope annotations, receptor-binding context, and host metadata within a single representation.
2. **Structure-aware reasoning.** Modeling residue neighborhoods, surface topology, antigenic patches, and long-range epistatic coupling—information that sequence-only methods discard.
3. **Calibrated hypothesis prioritization.** Uncertainty-aware scoring of which emerging variants are most likely to alter immune recognition or host adaptation, ranked against explicit baselines.
4. **Mechanistic interpretability.** Residue-level and region-level attribution that identifies the structural and sequence features driving each prediction, producing testable hypotheses rather than opaque scores.

If successful, the project will yield two outcomes. First, new testable knowledge about the biomolecular determinants of H5N1 antigenic change and host adaptation. Second, a documented, reproducible AI workflow for structure-informed biomolecular reasoning that can be extended in Phase II to broader viral systems, larger datasets, and deeper experimental coupling.

## 3. Specific Aim and Phase I Objectives

### Specific Aim
Develop and validate a multimodal AI workflow that predicts and interprets H5N1 antigenic evolution, immune escape risk, and cross-species adaptation from linked biomolecular and surveillance data.

### Phase I Objectives

**Objective 1. Curate a locked benchmark linking H5N1 sequence, structure, and phenotype.**  
Assemble a harmonized dataset of HA sequences, experimental and predicted HA structures, antigenic-site annotations, receptor-binding features, host species labels, and literature-derived functional annotations. Define train/validation/test partitions with lineage-aware and temporal splits to prevent information leakage.

**Objective 2. Build structure-aware multimodal AI models for three coupled prediction tasks.**  
Develop models that integrate protein language model embeddings, structure-informed graph or geometric features, residue-level functional annotations, and host/evolutionary metadata. Train and evaluate on three tasks: (i) antigenic impact classification, (ii) immune escape likelihood estimation, and (iii) cross-species adaptation scoring.

**Objective 3. Quantify AI advantage against rigorous baselines.**  
Compare multimodal models against sequence-only protein language model baselines, conventional feature-engineered classifiers, and ablated variants lacking structure or functional-site inputs. Report gains in discrimination, calibration, prioritization yield, and interpretability.

**Objective 4. Deliver interpretable hypotheses and a Phase II-ready workflow package.**  
Produce ranked candidate mutations, residue patches, and variant clusters for experimental follow-up. Deliver a documented, reproducible workflow with benchmark specification, evaluation suite, and Phase II expansion plan.

## 4. Technical Approach

### Task 1. Data assembly, harmonization, and benchmark locking
The benchmark centers on H5N1 HA, with optional neuraminidase or polymerase context included only where directly relevant to host adaptation interpretation. Five data layers will be integrated: (i) viral sequences with aligned residue coordinates; (ii) experimental and predicted HA structures (monomers and trimers); (iii) annotations for receptor-binding residues, major antigenic regions, glycosylation motifs, cleavage features, and solvent-exposed surfaces; (iv) host species, clade, and geographic metadata; and (v) curated evidence for antigenic change, antibody escape, altered receptor engagement, or mammalian adaptation from published literature and public databases.

**Benchmark discipline** is a defining feature of the Phase I design. Before any model optimization, we will lock train/validation/test partitions using lineage-aware and temporal splits that prevent information leakage across closely related variants. Surveillance-style generalization—predicting forward in time and across clades—is more informative than random-split accuracy and will be the primary evaluation paradigm.

### Task 2. Multimodal representation of H5N1 biomolecular variation
Each viral variant will be encoded through four complementary modalities:

- **Sequence:** protein language model embeddings (e.g., ESM-family) with mutation-aware tokenization capturing substitution identity and positional context.
- **Structure:** residue-level graphs encoding contact neighborhoods, solvent-accessible surface area, geometric features, and site-specific structural context derived from experimental or predicted HA coordinates.
- **Functional sites:** domain-informed annotations for receptor-binding residues, antigenic patches, glycosylation motifs, and other biologically defined site labels.
- **Evolutionary / host context:** clade assignments, host species, and related metadata, incorporated with care to improve generalization without introducing trivial label leakage.

This multimodal design reflects the biology: immune escape and host adaptation depend not merely on whether a residue changes, but on where in three-dimensional space the change occurs, whether it remodels an exposed epitope or receptor-contact surface, whether it disrupts glycan shielding, and whether combinations of substitutions interact non-additively. To quantify the marginal contribution of each information layer, we will train and compare sequence-only, sequence+structure, and full multimodal model variants in a controlled ablation framework.

### Task 3. Prediction tasks
Three tightly coupled prediction tasks target the major biomolecular dimensions of H5N1 risk:

**Task 3A: Antigenic impact.** Classify whether observed or candidate substitutions produce meaningful antigenic change, with residue- and variant-level ranking of predicted effect size.

**Task 3B: Immune escape.** Estimate the probability that substitutions or substitution combinations reduce recognition by known neutralizing antibodies or defined antibody classes, using published escape maps, epitope annotations, and structural context as supervision signals.

**Task 3C: Cross-species adaptation.** Identify biomolecular signatures associated with mammalian host adaptation, focusing on HA receptor-binding features and structurally interpretable adaptation proxies. This task will not claim to predict transmission outcomes; it will identify structural and sequence patterns statistically associated with increased adaptation concern.

Where beneficial, multi-task learning will share representations across tasks to improve data efficiency and enforce mechanistic consistency among related endpoints.

### Task 4. Interpretability and hypothesis generation
Predictive performance alone is insufficient; Phase I must also demonstrate biological utility. We will implement four levels of interpretability analysis:

1. **Residue attribution.** Per-residue importance scores identifying which positions most strongly influence each prediction, computed via gradient-based or perturbation-based methods.
2. **Epitope-patch importance.** Aggregated attribution over structurally defined antigenic regions, receptor-binding domains, and glycosylation neighborhoods.
3. **Mutational interaction analysis.** Detection of non-additive (epistatic) effects among substitution pairs or small combinations, scored against single-mutation baselines.
4. **Counterfactual variant scoring.** In silico mutagenesis to estimate the predicted functional impact of unobserved substitutions at key positions.

These analyses will generate ranked, testable hypotheses: which substitutions most strongly remodel specific antigenic regions, which residue combinations may drive escape through epistatic coupling, and which emerging lineages warrant closer scrutiny because of joint antigenic and host-adaptation signatures.

## 5. Evaluation Plan and Quantitative Definition of AI Advantage

AI advantage is defined operationally. The proposed workflow must demonstrate measurable improvement over appropriate baselines in one or more of four dimensions:

1. **Predictive power.** Higher discrimination (AUROC, AUPRC) or ranking quality on held-out benchmark tasks under lineage-aware and temporal splits.
2. **Surveillance-style generalization.** Sustained performance across clades, time windows, or host contexts not seen during training.
3. **Biological insight.** Enrichment of known functional sites among top-attributed residues; stronger prioritization of expert-credible hypotheses versus baseline rankings.
4. **Workflow efficiency.** Reduced candidate search space for follow-up structural or experimental analysis, measured by top-k enrichment and triage throughput.

### Baselines
Four baseline classes will anchor all comparisons:

- sequence-only protein language model predictions (e.g., ESM-family zero-shot or fine-tuned),
- conventional feature-engineered classifiers using hand-crafted sequence and physicochemical descriptors,
- ablated multimodal models with structure or functional-site inputs removed,
- simple statistical rankings derived from substitution frequency, conservation score, or literature-derived concern lists.

### Success criteria for Phase I
Phase I succeeds if the workflow demonstrates:

- reproducible improvement over the strongest sequence-only baseline on at least two of the three prediction tasks,
- interpretable residue- or region-level outputs that recover known structure-function biology in case-study analyses,
- a prioritized list of candidate variants or mutations for downstream experimental follow-up, and
- a documented, reproducible workflow technically ready for Phase II expansion.

Gains will be evaluated under stringent partitioning strategies relevant to real-world surveillance conditions, not random splits.

## 6. Feasibility, Teaming, and Resources

This Phase I effort is designed as the first rigorous benchmark-and-demonstration step rather than as a claim of prior completed predictive success. The proposal does not rely on unpublished pilot results. Instead, feasibility rests on the availability of mature public data streams, established structural modeling resources, existing protein modeling toolchains, and institutional computing capacity sufficient to execute a tightly bounded workflow within nine months. The Phase I objective is to convert those ingredients into a locked benchmark, reproducible modeling pipeline, and quantitative evaluation framework that can support stronger downstream experimental coupling in Phase II.

The project is further grounded by the lead institution’s existing computational environment. The **University of Georgia (UGA)** provides the project’s primary execution base, with project-relevant computing support available through the **Institute for Artificial Intelligence (IAI)** and the **Georgia Advanced Computing Resource Center (GACRC)**. According to the IAI computing-resources document, UGA faculty and researchers have access to **Sapelo2**, UGA’s shared high-performance computing cluster operated by GACRC, including large CPU capacity and GPU partitions with **H100**, **A100**, and **L4** nodes. For IAI-affiliated faculty, additional priority access is available to dedicated GPU-enabled systems, including **NVIDIA B200**, **L40S**, and **AMD MI210** resources. These existing resources reduce startup risk and support the benchmark construction, multimodal model training, ablation studies, and reproducible evaluation required for Phase I. fileciteturn30file0

The multi-institutional team combines three complementary capabilities. The lead institution provides project leadership, biomolecular AI model development, benchmark design, and evaluation. A DOE/NNSA National Laboratory or Scientific User Facility partner contributes scalable computing infrastructure, workflow reproducibility engineering, and alignment with Genesis Mission platform requirements. An industry partner contributes applied AI engineering practice, model lifecycle management, and external relevance testing. Each partner owns a defined technical scope and deliverable set; none serves a nominal role.

## 7. Risks and Mitigation

| Risk | Mitigation |
|------|-----------|
| **Sparse or heterogeneous phenotype labels** limit supervised learning | Ranking-based task formulations, weak supervision, transfer learning from related influenza subtypes, and explicit uncertainty reporting |
| **Structural uncertainty** for variants lacking experimental coordinates | Propagate structure-prediction confidence scores; compare experimental vs. predicted structures where both exist; evaluate whether structure-informed gains survive uncertainty-aware filtering |
| **Lineage leakage** inflates apparent performance | Lineage-aware deduplication, temporal test splits, phylogenetically stratified holdouts, and ablation studies that isolate clade signal from mechanistic signal |
| **Overclaimed biological interpretation** | Distinguish prediction from proof in all outputs; anchor interpretations to published virology; frame all model-derived candidates as prioritized hypotheses for experimental follow-up |

## 8. Expected Outcomes

At the end of Phase I, the project will deliver five concrete products:

1. A curated, locked H5N1 biomolecular benchmark with defined tasks, evaluation splits, and provenance documentation.
2. A tested multimodal modeling workflow for antigenic evolution, immune escape, and host-adaptation prediction.
3. A quantitative AI-advantage assessment comparing multimodal, sequence-only, and ablated baselines under stringent evaluation.
4. Ranked, interpretable mutation- and epitope-level hypotheses with residue-resolution attribution for downstream experimental follow-up.
5. A Phase II transition package: trained models, reproducible workflow code, benchmark specification, and expansion roadmap.

These outputs advance the Genesis Mission objective by demonstrating that structure-informed AI can extract biomolecular insight from heterogeneous viral data at a level that simpler approaches cannot match—connecting sequence variation to structural and functional consequence in a reproducible, benchmarked scientific workflow.

## 9. Phase II Vision

Phase II will expand the validated Phase I workflow along three axes: (i) **data scale**—integration of larger surveillance streams, additional influenza subtypes, and automated ingestion pipelines; (ii) **biomolecular depth**—expanded antibody classes, higher-order variant combinatorics, and selected non-HA adaptation markers (e.g., PB2 mammalian-adaptation residues); and (iii) **experimental coupling**—direct partnership with structural biology and virology laboratories for prospective validation of Phase I–generated hypotheses. The Phase II goal is to transition from a well-validated research workflow to a broader, experimentally grounded capability for AI-driven biomolecular reasoning over viral evolution.

**Summary.** This project uses H5N1 as a scientifically demanding model system to develop and validate an AI-driven biomolecular modeling workflow aligned with DOE Genesis Mission Topic 2A. The work is feasible within nine months, anchored to quantitative AI-advantage evaluation against rigorous baselines, and designed to produce both high-value biomolecular science and a strong evidentiary basis for Phase II.
