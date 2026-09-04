# **A shared cytoskeletal–guidance architecture links persistent psychedelic-associated enhancers to schizophrenia TWAS, with a minority tail in a clozapine-enriched proxy**

## **Abstract**

**Background.** Schizophrenia is highly polygenic, but translating genetic associations into experimentally tractable targets remains difficult. Treatment-resistant schizophrenia affects approximately one-third of patients and is clinically associated with clozapine exposure, chronicity, and heterogeneous ascertainment. Psychedelic-associated enhancer programmes have been linked to synaptic and developmental genes, but their relationship to schizophrenia liability and treatment-resistance-associated profiles has not been resolved at gene level.

**Methods.** Persistent H3K27ac enhancers identified after a single DOI exposure in mouse frontal-cortex neuronal material were linked to genes using an activity-by-contact scoring framework. Mouse targets were mapped to human orthologues and used to construct GO biological-process gene sets. These sets were tested against S-PrediXcan-derived schizophrenia statistics from the 2026 European-ancestry schizophrenia analysis and the 2018 CLOZUK clozapine-enriched proxy. Conservative enrichment filters, gene-level convergence and divergence, leave-k testing, driver ablation, and concordance analyses were applied.

**Results.** Regulation of cell motility and positive regulation of serine/threonine kinase activity were the only non-metabolic GO-level findings that passed the conservative confidence-interval and permutation criteria in both cohorts. Gene-level analysis resolved them into a ten-gene negative cytoskeletal/guidance block: TNR, CCDC25, RHOA, NEXN, TENM2, ERBB4, ADRA2A, SPATA13, PLEKHG3, and LDB2. The block survived leave-two-out and driver-ablation tests. Convergent-down and convergent-up genes remained balanced at conventional Z-score thresholds, with 53 and 54 genes, respectively. Cross-cohort correlation was 0.81 and increased to 0.91 after removal of a 16% divergent tail. The treatment-resistance-associated adhesion and neurite deviation concentrated in five genes rather than a module-wide effect.

**Conclusions.** Persistent-enhancer-associated genes resolve to a shared, bidirectional schizophrenia architecture whose most robust object is a compact cytoskeletal/guidance block. The clozapine-enriched proxy retains this architecture and adds a minority divergent tail. These results support gene-level experimental follow-up and argue against treating overlapping GO terms as independent mechanisms or treatment resistance as a separate molecular disease map.

## **Introduction**

### **The translational stall in schizophrenia**

Schizophrenia is a highly heritable, polygenic disorder in which risk is distributed across many common and rare variants. Large genetic studies have shown that common risk is concentrated in genes expressed in the brain, particularly in neuronal and synaptic systems, and that schizophrenia-associated alleles are enriched in mutation-intolerant genomic contexts \[1-4\]. Rare disruptive variants have provided complementary evidence for synaptic, postsynaptic, and neurodevelopmental involvement \[5\]. These findings have established a strong biological foundation, but they have not yet produced a broad new class of first-line treatments.

One reason is that the field often has more pathway labels than experimentally manageable targets. Most schizophrenia-associated variants are noncoding, and linking them to genes requires integration across linkage disequilibrium, chromatin state, enhancer activity, gene expression, and cell type. TWAS can prioritize genes, but its results depend on prediction models, linkage disequilibrium, tissue choice, and the distinction between genetically predicted expression and measured expression \[6-9\]. Gene-set analysis adds biological context but can generate apparently separate signals from overlapping gene membership. The problem addressed here is therefore practical as well as statistical: there are many plausible processes, but relatively few gene-level objects that a laboratory or translational programme can test directly.

### **Treatment resistance as a clinical, not molecular, category**

Treatment-resistant schizophrenia is a clinically important category associated with disability, service use, and limited therapeutic options. Clozapine remains the established evidence-based treatment for treatment resistance and, in relevant jurisdictions, the only antipsychotic specifically licensed for that indication \[10,11\]. However, treatment-resistance definitions have historically varied across studies. The Treatment Response and Resistance in Psychosis Working Group was established in part because treatment-resistant and treatment-responsive samples were not consistently defined or clinically comparable \[11\]. Reviews have also emphasized the contribution of pseudo-resistance, illness duration, medication exposure, smoking, metabolic factors, and other sources of clinical heterogeneity \[12-15\].

The CLOZUK-derived schizophrenia analysis is therefore a useful but imperfect proxy for treatment resistance. It is enriched for individuals exposed to clozapine, but it is not a clean treatment-resistant-versus-responsive case–control study. This distinction matters for target discovery. If a clozapine-enriched sample represents a second molecular disease map, it may warrant a distinct discovery strategy. If it largely retains the schizophrenia map and differs at a minority of loci, then the translational priority becomes stratification rather than wholesale replacement of the schizophrenia target landscape.

### **Why a psychedelic enhancer map is a usable prior, not a treatment claim**

A single DOI exposure in mice has been reported to produce enduring changes in frontal-cortex dendritic structure, synaptic plasticity, and chromatin organization. In particular, H3K27ac changes at enhancer regions associated with synaptic assembly persisted beyond the acute exposure period, and the affected regulatory regions overlapped loci associated with schizophrenia, depression, and attention-deficit/hyperactivity disorder \[16\].

Enhancers are a reasonable starting point for studying common psychiatric risk because common disease variants are frequently located in regulatory DNA and active chromatin regions. However, enhancer activity does not by itself establish the regulated gene, the relevant cell type, or the direction of expression change. Activity-by-contact models provide a principled way to prioritize enhancer–gene connections, but they remain predictions that require experimental validation \[17,18\].

The present analysis therefore treats the 091IvA enhancer experiment and the 091IvC gene-set construction as an independently derived regulatory prior. It does not assume that DOI is therapeutic in schizophrenia, that persistent enhancer activity reverses schizophrenia-associated expression, or that a mouse enhancer has the same function in human patient tissue. The question is narrower: do genes tagged by this persistent enhancer programme organize into a coherent schizophrenia TWAS architecture, and is that architecture shared with a clozapine-enriched proxy?

### **Hypothesis and design**

We hypothesized that the enhancer-derived genes would not resolve into many independent schizophrenia pathways. Instead, we expected a compact, bidirectional gene architecture shared by a liability-oriented schizophrenia TWAS and a clozapine-enriched proxy, with a minority of genes showing larger proxy-specific deviations. The analysis proceeded from persistent DOI-associated enhancers to activity-by-contact target genes, human orthologue mapping, GO biological-process sets, S-PrediXcan statistics in the two schizophrenia datasets, conservative set-level filtering, gene-level convergence and divergence, and robustness stress testing.

### **Scope**

This is an association and architecture study. A negative TWAS Z-score is not equivalent to measured downregulation in patient cortex. Mouse neuronal H3K27ac is not human patient expression or chromatin. The clozapine-enriched dataset is a proxy rather than a definitive molecular definition of treatment resistance. These limitations are part of the design and determine the level at which the results are interpreted.

## **Methods**

### **Enhancer source and gene-set construction**

The enhancer prior was derived from GSE161626, a mouse experiment examining the effects of a single DOI exposure on frontal-cortex neuronal material. H3K27ac signal was assessed at vehicle, 24-hour, 48-hour, and 7-day time points. The 091IvA pipeline constructed a consensus peak set from high-signal genomic bins, quantified H3K27ac signal per peak and sample, and compared the 7-day condition with vehicle. Peaks were retained using false-discovery-rate and effect-size criteria, after which time-course profiles were standardized and clustered. Persistent up and down clusters were defined as those remaining displaced from vehicle at 24 hours, 48 hours, and 7 days.

Persistent enhancers were linked to protein-coding mouse genes using an activity-by-contact scoring implementation. Mean 7-day enhancer activity was combined with a distance-dependent contact function over a five-megabase window. Enhancer–gene pairs with ABC scores greater than 0.02 were retained. Mouse genes were mapped to human orthologues using HomoloGene-style mappings and symbol-based fallback where a one-to-one mapping was unavailable. The mapping procedure recorded direct matches, orthologue-resolved matches, fallback symbols, and unmapped genes.

The resulting human genes were used to construct associated pathway sets. GO biological-process and KEGG libraries were queried using hypergeometric enrichment. The lead-set filters used a Benjamini–Hochberg false-discovery-rate threshold of 0.10, a minimum of five overlapping query genes, and a maximum pathway size of 500 genes. No minimum fold-enrichment threshold was imposed. KEGG was retained primarily as an orientation resource. The inferential objects in 091IvD were the associated human GO biological-process sets, not the complete raw ABC target list.

The source experiment and its persistent chromatin findings are described by \[16\]. The use of an activity-by-contact framework follows the logic of \[17,18\], while the enhancer and chromatin interpretation was informed by regulatory-genomics resources including the Roadmap Epigenomics and PsychENCODE projects \[19-22\].

### **TWAS cohorts and gene-level scores**

Two schizophrenia datasets were analyzed. The first was the European-ancestry schizophrenia component of Bigdeli et al \[23\], hereafter SCZ-EUR. The second was the schizophrenia dataset from Pardiñas et al \[3\], derived from the clozapine-enriched CLOZUK sample and treated throughout as a TRS-proxy rather than a definitive treatment-resistant schizophrenia phenotype. The Bigdeli study emphasizes the broad sharing of schizophrenia genetic architecture across populations while also demonstrating the importance of ancestral diversity for discovery and prediction \[23,24\]. The present analysis used the EUR slice and therefore does not constitute an ancestry-diverse replication.

S-PrediXcan results were loaded from tissue-level files, with gene symbols and Ensembl identifiers harmonized when available. For each gene and cohort, tissue-level Z-scores were combined using a Stouffer calculation. Six brain tissues contributed to the tissue-level analyses: amygdala, anterior cingulate cortex, caudate, frontal cortex area BA9, hippocampus, and nucleus accumbens. Cross-tissue correlations and shared expression models were not assumed to be independent.

### **Set-level statistics**

For each gene set and cohort, the analysis calculated the number of genes found, coverage, Stouffer Z, mean Z, median Z, mean absolute Z, a trimmed mean, Wilcoxon signed-rank testing against zero, and a competitive permutation p-value. Ten thousand random gene-set permutations were used where applicable. Bootstrap percentile confidence intervals were generated from 2,000 resamples of the observed gene members. Robust analyses used winsorized values for selected statistics.

Cross-cohort comparisons included unpaired and paired tests, Pearson correlation, Spearman correlation, Lin’s concordance correlation coefficient, Kendall’s tau, sign-concordance rate, and sign-concordance testing. Gene-level leave-one-out influence was assessed by recomputing Stouffer Z after removal of each gene. A gene was flagged as influential if its removal changed the absolute Stouffer statistic by more than 20% or caused a sign flip. Family-wise false-discovery rates were calculated by pooling the p-values produced within the run across enrichment, differential, proximity, and pairwise tests.

The conservative reporting gate required a set to have a confidence interval excluding zero, a permutation p-value below 0.05, and an influence-robust Stouffer statistic with absolute value at least 1.96. The gate was applied to distinguish set-level findings from concordance, proximity, or driver-level observations.

### **Gene-level architecture**

The 091IvD gene-detail files were stacked into a matrix containing 702 unique genes. Genes were classified using the two cohort-level median Z-scores. A gene was designated converge-down if it had the same sign in both cohorts and both absolute Z-scores exceeded 1.96. Converge-up required the same positive-sign criterion. Diverge-sign required opposite signs and a minimum absolute Z-score greater than 1.0. Diverge-shift required an absolute TRS-proxy minus SCZ-EUR Z-score difference greater than 2.0. All remaining genes were classified as weak.

GO sets were mapped to six descriptive modules—migration and cytoskeleton, neurite development, adhesion and synapse, signaling and plasticity, excitability, and metabolism—solely for orientation. These modules were not treated as independent pathways. The ten-gene cytoskeletal/guidance core, the four prespecified driver genes CD40, GIGYF1, GCH1, and CACNB3, and the seven prespecified TRS-proxy candidates AMIGO1, CNTN1, CDH10, ST8SIA2, ITM2B, KCNQ2, and GLI2 were defined before the Stage 4 stress tests.

### **Robustness battery and reproducibility**

The robustness battery included Z-score threshold grids from 1.00 to 3.00, divergent-tail thresholds from 1.00 to 3.00, leave-one- and leave-two-out tests for the ten-gene core, kinase residual analysis after CD40 removal, driver ablation, concordance after removal of hubs and divergent-tail genes, candidate-gene ablation of the adhesion and neurite shift, bootstrap correlation within the ten-gene core, and reannotation of motility genes after stripping kinase-overlapping genes.

The principal failure rule for the motility claim was prespecified: if the motility-only set lost its negative signal after removal of kinase-overlapping genes, motility and kinase would not be reported as independent pathways. The analysis used no new wet-lab data and did not rerun upstream TWAS models. Input provenance and file hashes were recorded by the pipeline. A post-hoc Stage 3 report-generation step attempting to sort a mechanistic roster failed because a mean\_Z column was unavailable. This affected the roster export only; the gene-by-cohort matrix, convergence classes, anchor tables, and Stage 4 stress tests were generated separately and form the basis of the present manuscript.

## **Results**

### **1\. Conservative set screening yields two reproducible negative annotations**

The complete significant-results summary contained 92 raw enrichment findings and 107 family-wise false-discovery-rate-significant entries. However, most of the family-wise entries belonged to proximity or concordance tests rather than enrichment tests. The conservative enrichment leaderboard contained 66 meta-level rows. Nine had confidence intervals excluding zero, and five survived the additional permutation criterion. Of these, two non-metabolic GO terms were reproducible in both cohorts: regulation of cell motility and positive regulation of serine/threonine kinase activity.

Regulation of cell motility was negative in SCZ-EUR, with Stouffer Z equal to \-8.12, a 95% confidence interval from \-13.30 to \-3.06, permutation p equal to 0.0085, and Wilcoxon p equal to 0.0044. The corresponding TRS-proxy result was also negative, with Stouffer Z equal to \-7.11, a confidence interval from \-12.57 to \-1.87, permutation p equal to 0.0153, and Wilcoxon p equal to 0.0230. Positive regulation of serine/threonine kinase activity showed the same direction: SCZ-EUR Stouffer Z was \-7.78, with confidence interval \-13.53 to \-2.40 and permutation p equal to 0.0105; the TRS-proxy Stouffer Z was \-7.04, with confidence interval \-12.03 to \-2.52 and permutation p equal to 0.0162.

A pteridine-containing compound metabolic-process set also passed the numerical confidence-interval and permutation criteria in SCZ-EUR. It contained only five genes and was dominated by GCH1. We therefore treated it as a GCH1-class observation rather than a stable metabolic pathway finding. The Stage 4 influence analysis supported this distinction: the motility Stouffer result required removal of no influential genes, whereas the kinase result required removal of one major driver, CD40, but remained strongly negative after that removal. The focus sets showed complete sign consistency across the six brain tissues used for tissue-level analysis. The numerical basis for these classifications is summarized in Table 1\.

#### **Table 1\. Conservative set-level enrichment findings**

| Gene set | Cohort | n | Stouffer Z | 95% CI | Permutation p | Interpretation |
| ----- | ----- | ----- | ----- | ----- | ----- | ----- |
| Regulation of cell motility | SCZ-EUR | 32 | \-8.117 | \-13.300 to \-3.064 | 0.0085 | Conservative survivor |
| Regulation of cell motility | TRS-proxy | 33 | \-7.109 | \-12.573 to \-1.873 | 0.0153 | Conservative survivor |
| Positive regulation of serine/threonine kinase activity | SCZ-EUR | 27 | \-7.781 | \-13.533 to \-2.401 | 0.0105 | Conservative survivor |
| Positive regulation of serine/threonine kinase activity | TRS-proxy | 27 | \-7.036 | \-12.033 to \-2.518 | 0.0162 | Conservative survivor |
| Pteridine-containing compound metabolic process | SCZ-EUR | 5 | \-6.794 | \-14.878 to \-1.102 | 0.0267 | GCH1-dominated observation |

Other synapse, adhesion, projection, and developmental gene sets frequently showed strong cross-cohort correlations, generally in the range of 0.76 to 0.90, but did not pass the conservative set-level enrichment gate. This distinction is central to interpreting the analysis. Gene-level ordering can be shared while the set mean remains weak or unstable, particularly when a pathway label contains genes with opposing directions. This is consistent with known limitations of gene-set analysis in the presence of overlapping membership and non-independent gene-level statistics \[25\].

### **2\. The ten-gene cytoskeletal/guidance block is the principal object**

The most stable result was not the full regulation-of-cell-motility GO term. It was a compact ten-gene block comprising TNR, CCDC25, RHOA, NEXN, TENM2, ERBB4, ADRA2A, SPATA13, PLEKHG3, and LDB2. All ten genes were negative in both GWAS-derived TWAS cohorts. Their SCZ-EUR and TRS-proxy Z-score pairs were, respectively: TNR, \-8.07 and \-7.58; CCDC25, \-5.82 and \-7.02; RHOA, \-5.87 and \-4.78; NEXN, \-4.26 and \-4.73; TENM2, \-3.42 and \-6.21; ERBB4, \-3.96 and \-5.39; ADRA2A, \-3.84 and \-4.11; SPATA13, \-2.21 and \-3.10; PLEKHG3, \-2.92 and \-2.35; and LDB2, \-2.06 and \-2.20. The gene-level scores are shown in Table 2\.

#### **Table 2\. Ten-gene cytoskeletal/guidance core**

| Gene | Z, SCZ-EUR | Z, TRS-proxy | ΔZ, TRS−SCZ | Orientation module |
| ----- | ----- | ----- | ----- | ----- |
| TNR | \-8.070 | \-7.584 | 0.487 | Migration/cytoskeleton; neurite development |
| CCDC25 | \-5.815 | \-7.016 | \-1.201 | Migration/cytoskeleton |
| RHOA | \-5.874 | \-4.776 | 1.098 | Adhesion/synapse; migration/cytoskeleton; signaling/plasticity |
| NEXN | \-4.258 | \-4.734 | \-0.476 | Adhesion/synapse; migration/cytoskeleton; neurite development |
| TENM2 | \-3.416 | \-6.212 | \-2.796 | Adhesion/synapse; migration/cytoskeleton |
| ERBB4 | \-3.957 | \-5.388 | \-1.431 | Migration/cytoskeleton; neurite development; signaling/plasticity |
| ADRA2A | \-3.844 | \-4.107 | \-0.263 | Migration/cytoskeleton; signaling/plasticity |
| SPATA13 | \-2.210 | \-3.102 | \-0.892 | Migration/cytoskeleton |
| PLEKHG3 | \-2.920 | \-2.348 | 0.572 | Migration/cytoskeleton |
| LDB2 | \-2.061 | \-2.204 | \-0.143 | Migration/cytoskeleton |

The block-level Stouffer statistics were \-13.4 in SCZ-EUR and \-15.0 in the TRS-proxy. The result remained negative after every leave-two-out combination: at least eight genes remained double-significant below \-1.96, and the block-level Stouffer statistic remained below \-1.96 in both cohorts. All ten genes retained the same sign across cohorts, and the weakest absolute Z-score in either cohort was 2.06 for LDB2. The within-core bootstrap correlation had a median of 0.83, with a 95% interval from 0.46 to 0.96. Thus, the core showed evidence of a shared ranking, although the interval was not sufficiently tight to justify describing the internal hierarchy as invariant.

Driver ablation produced the same conclusion. Removing CD40, GIGYF1, GCH1, CACNB3, or all four drivers left all ten core genes classified as converge-down. The block therefore did not borrow its existence from the kinase driver, the largest positive gene, the pteridine-associated GCH1 result, or the synaptic CACNB3 signal.

The biology attached to this block is coherent but should remain descriptive. TNR encodes tenascin-R, an extracellular-matrix protein associated with perineuronal-net organization, nodes of Ranvier, and inhibitory-synapse environments \[26\]. TENM2 is a teneurin-family adhesion molecule involved in cell recognition and partner matching. NEXN is associated with actin-linked mechanical coupling, whereas RHOA is a canonical small GTPase regulating actin organization, growth-cone behavior, and neuronal morphology \[27,28\]. ERBB4 is a receptor for neuregulin signaling and has established relevance to interneuron development, cortical circuitry, and schizophrenia biology \[29-31\]. ADRA2A is a Gi-coupled receptor that can influence intracellular signaling and cytoskeletal remodeling in addition to its role in catecholaminergic physiology. The presence of CCDC25, SPATA13, PLEKHG3, and LDB2 is empirical rather than rhetorical: they remained in the block after leave-two-out testing and are part of the object even though the most familiar biological narrative centers on TNR, RHOA, and ERBB4.

The required qualification emerged from set-composition control. The motility and kinase annotations contained 46 overlapping genes. Four of those—ADRA2A, ERBB4, PIK3R1, and RHOA—were converge-down genes, and three were members of the ten-gene core. When kinase-overlapping genes were removed, the motility-only Stouffer statistic was \-0.24 in SCZ-EUR and \-2.22 in the TRS-proxy. Thus, the parent motility GO term was not an independent pathway in SCZ-EUR. The TRS-proxy retained a modest secondary motility-only signal, but this does not rescue a claim of two independent GO pathways.

The kinase annotation nonetheless remained informative after CD40 removal. Forty-seven genes remained after excluding CD40, with residual Stouffer statistics of \-5.58 in SCZ-EUR and \-4.98 in the TRS-proxy; seven genes still met the converge-down criterion. The supplied summary reports the count but does not enumerate those seven residual genes, so no identities are assigned here. The appropriate conclusion is that the kinase-annotated set remained negative after removal of a major driver, not that CD40 defines a kinase mechanism or that the kinase set represents a second independent disease pathway.

Ten cytoskeletal/guidance genes formed a double-cohort negative block that survived leave-two-out testing, same-sign checks, and removal of CD40, GIGYF1, GCH1, and CACNB3. Because RHOA, ERBB4, and ADRA2A also belong to the kinase annotation, we treat this as one gene-level block, not two pathways.

### **3\. The architecture is bidirectional rather than uniformly downregulated**

Across the 702 unique genes, 53 were classified as converge-down, 54 as converge-up, 97 as divergent, and 498 as weak. The balance between the two convergent classes was not dependent on a single threshold. At an absolute Z-score cutoff of 1.00, there were 101 down and 109 up genes. At 1.64, the counts were 65 and 65\. At 1.96, they were 53 and 54\. At 2.58, they were 36 and 37\. Only at the more extreme cutoff of 3.00 did the balance become clearly more negative, with 32 down and 22 up genes. The complete gene-class distribution is shown in Table 3\.

#### **Table 3\. Gene-level convergence and divergence classes**

| Class | Definition | n | Percentage |
| ----- | ----- | ----- | ----- |
| Converge-down | Same sign in both cohorts; both absolute Z-scores \>1.96; negative direction | 53 | 7.5 |
| Converge-up | Same sign in both cohorts; both absolute Z-scores \>1.96; positive direction | 54 | 7.7 |
| Diverge-sign | Opposite signs; minimum absolute Z-score \>1.0 | 37 | 5.3 |
| Diverge-shift | Absolute TRS-proxy minus SCZ-EUR Z-score difference \>2.0 | 60 | 8.5 |
| Weak | Does not meet another classification rule | 498 | 70.9 |
| **Total** |  | **702** | **100.0** |

The working range from 1.64 to 2.58 therefore supports an approximately balanced bidirectional architecture. The negative tail was more extreme, containing genes such as TNR, KCNN3, LIMK1, CD40, and GCH1, but the positive class was not a single-locus artefact. The largest positive signal came from GIGYF1, with Z-scores of 13.59 in SCZ-EUR and 12.04 in the TRS-proxy. Other positive genes included PLEKHG4, LY6H, ZIC1, KIF20B, UNC119B, FUT9, LRP4, GPM6A, GABRA5, ABCC8, FAM110C, MMP9, SH2B2, and CXADR.

Removing GIGYF1 reduced the converge-up class from 54 to 53 genes. The positive class therefore did not collapse when its largest member was removed. Likewise, removing CD40 reduced the converge-down class from 53 to 52\. These ablations show that neither class was created by one extreme locus. The threshold grid is shown in Table 4\.

#### **Table 4\. Threshold sensitivity of the bidirectional convergent split**

| Absolute Z-score cutoff | Converge-down genes | Converge-up genes | Down/up ratio | Motility-core genes retained |
| ----- | ----- | ----- | ----- | ----- |
| 1.00 | 101 | 109 | 0.93 | 10 |
| 1.64 | 65 | 65 | 1.00 | 10 |
| 1.96 | 53 | 54 | 0.98 | 10 |
| 2.58 | 36 | 37 | 0.97 | 7 |
| 3.00 | 32 | 22 | 1.46 | 7 |

This architecture explains why different statistical summaries tell apparently different stories. Pearson correlation, Lin’s concordance correlation, Kendall’s tau, and sign concordance can be high when genes retain a similar rank order across cohorts. Stouffer, Wilcoxon, and permutation statistics can be weak or strongly negative depending on which direction dominates the mean within a particular annotation. Motility and kinase labels appear negative because their negative members carry the set mean. Projection, synapse, and adhesion labels often appear concordant without passing the enrichment gate because both positive and negative classes are represented within the same annotation.

The enhancer experiment therefore did not identify a uniformly schizophrenia-downregulated programme or a uniformly plasticity-upregulated programme. It identified a regulatory neighbourhood in which schizophrenia-associated TWAS signals point in both directions. The correct summary is that the down and up classes remained approximately balanced across the prespecified threshold range, and that disagreement between concordance and enrichment reflects opposing architecture rather than an unstable cutoff.

### **4\. The TRS-proxy retains the map and adds a minority divergent tail**

The two cohorts shared a broad gene-level map. Among 512 genes mapped in both datasets, Pearson correlation was 0.808 across all mapped genes. Removing cross-layer hubs changed the correlation only slightly, to 0.804. In contrast, removing the divergent tail increased the correlation to 0.906, and removing both hubs and the tail produced a correlation of 0.905. Sign concordance showed the same pattern, increasing from 0.793 for all mapped genes to 0.850 after tail removal and 0.847 after removal of both hubs and tail.

At the planned absolute Delta-Z threshold of 2.0, 110 of 702 genes, or approximately 16%, formed the divergent tail. The sensitivity grid showed that the tail remained a minority at every threshold: 247 genes at a threshold of 1.0, 171 at 1.5, 110 at 2.0, 78 at 2.5, and 58 at 3.0. All seven prespecified candidates—AMIGO1, CDH10, CNTN1, GLI2, ITM2B, KCNQ2, and ST8SIA2—were retained from the lowest through the highest tail thresholds. The gene-level classification contained 97 divergent genes because its sign-divergence and shift rules were applied sequentially; the tail-sensitivity analysis used the broader union of sign and absolute-shift criteria. The concordance and tail-sensitivity results are summarized in Table 5\.

#### **Table 5\. Cross-cohort concordance and divergent-tail sensitivity**

| Analysis | n | Pearson r | Sign concordance | Tail size | Tail fraction | TRS candidates retained |
| ----- | ----- | ----- | ----- | ----- | ----- | ----- |
| All mapped genes | 512 | 0.808 | 0.793 | — | — | — |
| No cross-layer hubs | 494 | 0.804 | 0.789 | — | — | — |
| No divergent tail | 434 | 0.906 | 0.850 | — | — | — |
| No hubs and no tail | 418 | 0.905 | 0.847 | — | — | — |
| Delta-Z cutoff 1.00 | — | — | — | 247 | 0.352 | 7 |
| Delta-Z cutoff 1.50 | — | — | — | 171 | 0.244 | 7 |
| Delta-Z cutoff 2.00 | — | — | — | 110 | 0.157 | 7 |
| Delta-Z cutoff 2.50 | — | — | — | 78 | 0.111 | 7 |
| Delta-Z cutoff 3.00 | — | — | — | 58 | 0.083 | 7 |

The improvement in concordance after removing the tail is informative. Hubs were not manufacturing the shared map, whereas the genes selected as potentially TRS-proxy-specific were suppressing the overall correlation. At the module level, the same pattern was observed after tail removal: adhesion and synapse genes had a correlation of 0.91, neurite-development genes 0.93, motility and cytoskeletal genes 0.89, signaling and plasticity genes 0.90, and excitability genes 0.95. The shared architecture was therefore distributed across modules rather than confined to one highly connected group.

The adhesion and neurite deviation was concentrated in five genes: AMIGO1, CNTN1, CDH10, ST8SIA2, and ITM2B. Their mean Delta-Z was \-4.09, compared with \-0.25 among the other 325 genes in the combined adhesion and neurite module. AMIGO1 showed the largest individual negative shift, from 0.92 in SCZ-EUR to \-4.85 in the TRS-proxy. CNTN1, CDH10, and ST8SIA2 also showed pronounced deviations, while ITM2B remained on the list because it met the prespecified shift rule rather than because it completed a preferred biological narrative. These results support a candidate list, not a module-wide TRS-proxy adhesion defect.

KCNQ2 was distinct. Its Delta-Z was \+5.10, whereas the remaining excitability-related genes had a mean shift of approximately \-0.35. KCNQ2 therefore represented a separate single-gene excitability hypothesis rather than a sixth member of the adhesion and neurite list. Its positive TRS-proxy direction contrasted with the negative convergence of KCNN3 and HCN3 in both cohorts and with the positive convergence of GABRA5 and ABCC8. The pattern is consistent with a split excitability hypothesis, but the evidence is insufficient for a potassium-transport pathway claim.

Clinically, these findings do not identify a molecular mechanism of treatment resistance. The CLOZUK dataset is enriched for clozapine exposure and may also capture chronicity, smoking, metabolic load, ancestry composition, ascertainment, and other correlated features. The most defensible statement is geometric: the TRS-proxy is mostly the same schizophrenia map with a locally divergent minority tail.

### **Findings that Stage 4 did not promote**

Several attractive interpretations remained unsupported. The enhancer-to-motility-to-synapse-to-excitability cascade cannot be inferred because enhancer–gene order, cell type, and causality are absent from the CSV results. Internal robustness for this claim remained approximately 32\. A psychedelic reversal of schizophrenia TWAS direction was not supported because there were no post-drug human expression data and no direct sign comparison between DOI-dependent expression and schizophrenia-associated TWAS. That claim remained at approximately 15\. A TRS molecular mechanism remained unsupported because the comparator was a clozapine-enriched proxy with chronicity, cumulative drug exposure, and ascertainment confounding; its internal robustness remained approximately 18\.

The pteridine or BH4 interpretation remained a GCH1-driven observation, with internal robustness approximately 39\. The potassium-ion-transport annotation remained internally split among KCNN3 and HCN3, GABRA5 and ABCC8, and KCNQ2, with internal robustness approximately 41\. Projection morphogenesis did not pass the earlier confidence-interval and permutation gate and was not revived by Stage 4\. The principal stress-test outcomes are summarized in Table 6\.

#### **Table 6\. Principal robustness stress-test outcomes**

| Test or claim | Result | Key evidence |
| ----- | ----- | ----- |
| Motility core, leave-two-out | PASS | At least 8 of 10 genes remained double-significant; Stouffer remained below \-1.96 |
| Kinase set after CD40 removal | PASS | Residual Stouffer Z \= \-5.575 in SCZ-EUR and \-4.977 in TRS-proxy; 7 converge-down genes |
| Driver ablation | PASS | All 10 motility-core genes remained converge-down after removal of CD40, GIGYF1, GCH1, CACNB3, or all four |
| Shared architecture after hub/tail removal | PASS | Pearson r increased from 0.808 to 0.905 after removing hubs and the divergent tail |
| Motility versus kinase independence | FAIL | Motility-only Stouffer Z \= \-0.236 in SCZ-EUR and \-2.224 in the TRS-proxy after removing kinase-overlapping genes |
| Motility-core ranking stability | PASS | Bootstrap r, 95% interval 0.460 to 0.964; median 0.828 |
| Adhesion/neurite TRS-proxy shift | PASS as candidate list | Candidate mean Delta-Z \= \-4.090 versus \-0.248 in the remaining module genes |
| KCNQ2/KCNN3 split | Not applicable | Single-gene hypothesis; not promoted to a pathway claim |
| GCH1/pteridine interpretation | Not applicable | Metabolism class expected to vanish without GCH1 |

The legal association-level statement is therefore:

Genes tagged by a persistent-enhancer experiment converge, at the TWAS level, on a shared cytoskeletal and plasticity-related neighbourhood implicated in schizophrenia. The data show overlap and association. They do not show which enhancer regulates which gene, in which cell, in which direction relative to the drug, or whether that direction would be therapeutic.

The required figures would follow the claim hierarchy. Figure 1 would show the Z-score cutoff grid with the ten-gene block marked. Figure 2 would show SCZ-EUR against the TRS-proxy, with the divergent tail in a separate colour and the all-gene and no-tail correlations annotated. Figure 3 would show leave-two-out and driver-ablation results for the core. The 46-gene motility–kinase overlap would be placed in the supplement as a clarification of the core finding, not as an additional discovery.

## **Discussion**

### **A usable target class**

The principal contribution of this analysis is not another broad schizophrenia pathway label. It is the identification of a small gene-level object that survives multiple stress tests in two GWAS-derived TWAS cohorts. The ten-gene block spans extracellular matrix, cell adhesion, actin-linked structure, Rho-family signaling, and growth-factor-receptor biology. This is consistent with the broader schizophrenia literature, in which common and rare variation converge on neuronal development, synaptic organization, and plasticity-related systems \[2,4,5,32\].

The result should not be described as evidence for a single biochemical pathway. Rather, it identifies a compact interface at which neurite structure, guidance, cell contact, and intracellular signaling meet. That distinction makes the finding more experimentally useful. A reasonable first-stage programme would test TNR, RHOA, ERBB4, NEXN, and TENM2 in human induced pluripotent stem-cell-derived cortical neurons and interneurons. CRISPR or CRISPR interference could be used to perturb each gene, with readouts including neurite length, branch number, growth-cone collapse, spine morphology, and gephyrin or PSD-95 puncta. These phenotypes are relevant to the known roles of actin and Rho-family signaling in growth-cone behavior and synaptic structure \[27,28,26,33\].

A second stage would ask whether schizophrenia-risk donor lines already differ on the same morphological measures. Only after such effects were established would it be reasonable to test pharmacological perturbations, including 5-HT2A-related compounds, non-hallucinogenic psychedelic-related analogues \[34\], or tools directed at ERBB4 and Rho signaling. The key translational point is that this programme does not require administering DOI to patients with psychosis. The assay can test whether a cellular phenotype lies in a regulatory neighbourhood shared by a psychedelic-associated enhancer experiment and schizophrenia genetic risk.

### **Shared substrate, three models, no winner**

The enhancer study provides an experimentally derived regulatory prior, while the schizophrenia TWAS provides a human genetic association map. Their overlap is biologically interesting because it connects persistent psychedelic-associated chromatin changes with genes implicated by schizophrenia genetics. However, three explanations remain open.

The first is therapeutic recruitment: a psychedelic-associated regulatory programme may engage a plasticity-related system that is impaired in a subset of schizophrenia-relevant neurons. The second is shared vulnerability: the same constrained neuronal genes may be sensitive to both psychedelic-induced remodeling and schizophrenia liability, with direction depending on cell type, developmental stage, or cellular state. The third is generic constrained-gene overlap: persistent enhancer-associated genes may be enriched for genes that are broadly important in neuronal development and therefore more likely to appear in schizophrenia studies.

The present data do not discriminate among these models. ABC links are predictions, not direct human enhancer–promoter contacts. The direction of an enhancer-associated signal does not establish the direction of gene expression in human cortex. Nor does a negative TWAS Z-score demonstrate that the corresponding gene is transcriptionally reduced in patients. Chromosome-conformation, cell-type-specific regulatory maps, perturbation experiments, and direct expression measurements are required before the shared substrate can be assigned a causal or therapeutic meaning \[17,18,22\].

The legally supportable sentence is therefore that persistent enhancer-tagged genes and schizophrenia TWAS converge on a cytoskeletal, guidance, and plasticity-related neighbourhood. The analysis does not demonstrate psychedelic reversal, therapeutic direction, or a causal enhancer-to-synapse cascade.

### **TRS trials should stop assuming a second map**

The most consequential clinical implication is negative. The clozapine-enriched proxy did not show a wholesale reorganization of the schizophrenia gene map. Cross-cohort correlation was approximately 0.81 across all mapped genes and rose to approximately 0.91 after removal of the divergent tail. This pattern is inconsistent with the simple idea that treatment-resistant schizophrenia represents an entirely separate molecular disease architecture. It is compatible with a shared schizophrenia substrate plus locally different biology.

This does not mean that treatment resistance is biologically unimportant. It means that the most efficient discovery strategy may be stratification within a shared target space. The ten-gene block can serve as a starting point for experiments relevant to schizophrenia generally and for examining whether specific cellular phenotypes are enriched in treatment-resistant samples. The five-gene adhesion and neurite list—AMIGO1, CNTN1, CDH10, ST8SIA2, and ITM2B—and the separate KCNQ2 hypothesis could then be evaluated in treatment-resistant cohorts defined using TRRIP criteria.

A replication study should prespecify whether the ten-gene block remains negative, whether cross-cohort correlation remains near 0.8, and whether the named tail genes remain off-diagonal after adjustment for illness duration, smoking, cumulative antipsychotic exposure, clozapine concentration, ancestry, and ascertainment. The relevant comparison should distinguish treatment resistance from clozapine exposure and pseudo-resistance wherever possible. The TRRIP framework is especially important because inconsistent clinical definitions can make a molecularly heterogeneous sample appear more distinct than it is \[11-13\].

The same caution applies to individual genes such as CD40 and ZAP70. Their prominence in an annotated kinase or immune-related set may reflect exposure, cell composition, or sample characteristics rather than a specific treatment-resistance mechanism. They should remain candidate biomarkers or covariates until tested in treatment-naive and treatment-characterized samples. Clozapine remains the evidence-based treatment for treatment resistance; these genetic results do not justify delaying or withholding it \[10\].

### **Why GO-led translation fails and what to report instead**

The 46-gene overlap between motility and kinase annotations is a concrete example of why GO labels cannot be treated as independent discoveries. The same genes can be annotated to cytoskeletal, receptor, kinase, adhesion, and plasticity processes. When those labels are tested separately, they may produce several significant terms that describe one underlying gene-level structure. The problem is not that the annotations are incorrect. The problem is that the annotations are not independent units of evidence.

The appropriate reporting unit in this study is therefore one block, one candidate list, and one divergent tail. The ten-gene block should be presented as the principal negative object. The kinase set minus CD40 should be retained as supporting annotation, not as a second mechanism. GCH1 should be described as a one-gene pteridine or BH4 hypothesis. GIGYF1 should be described as an influential positive locus within a broader up core, not as evidence for an RTK pathway. The five adhesion and neurite genes should be reported as a list, not as a module-wide TRS defect.

This approach also protects against a common interpretive error: allowing a pathway cartoon to determine which genes count as evidence. In the present analysis, genes remained in the core because they survived the empirical stress tests, not because they fit a preferred mechanistic narrative.

### **Excitability as a secondary, testable split**

The excitability results are more modest but potentially useful. KCNN3 and HCN3 were negative in both cohorts, whereas GABRA5 and ABCC8 were positive in both. KCNQ2 was positive in the TRS-proxy but not in SCZ-EUR, producing a large proxy-specific shift. These observations do not establish a potassium-transport pathway. They suggest a split physiological hypothesis involving intrinsic excitability, afterhyperpolarization, and the relationship between channel composition and synaptic input.

A suitable experimental test would use patch-clamp recordings in patient-derived cortical neurons or interneurons. The relevant readouts would include resting membrane potential, action-potential threshold, spike-frequency adaptation, afterhyperpolarization, and synaptic-event frequency. KCNN3, HCN3, GABRA5, ABCC8, and KCNQ2 should be treated as separate hypotheses rather than collapsed into one channel pathway. The broader physiological interpretation is circuit computation—connectivity and intrinsic gain—rather than a new diagnostic channelopathy \[35-37\].

### **Limits that protect translation**

The analysis has several limitations that should remain visible. First, the SCZ-EUR results represent one ancestry slice of a broader schizophrenia GWAS. The Bigdeli study demonstrates that schizophrenia genetic effects are broadly shared across populations but also shows that discovery and prediction are affected by ancestral representation. The present findings should therefore be replicated in non-European datasets rather than treated as globally generalizable \[24,23\].

Second, the TWAS results are based on genetically predicted expression and should not be equated with measured bulk RNA expression in dorsolateral prefrontal cortex or any other patient tissue. Stouffer aggregation assumes a level of independence that is unlikely to hold fully in the presence of linkage disequilibrium, shared eQTLs, and correlated tissue models. Bootstrap intervals quantify resampling uncertainty in the gene members; they do not capture uncertainty in the upstream TWAS prediction models.

Third, the enhancer prior was derived from mouse frontal-cortex neuronal material after a single DOI exposure. It does not establish a human cell type, human enhancer–promoter contact, or patient-specific regulatory direction. The 091IvA pipeline used predicted activity-by-contact links and a five-megabase scoring window, not direct perturbation of each enhancer in human brain cells. No post-drug human expression dataset was available for a reversal analysis, and no comparison was made between DOI-induced expression direction and schizophrenia TWAS direction.

Fourth, the TRS comparison uses a clozapine-enriched proxy. Chronicity, cumulative drug exposure, smoking, metabolic burden, ancestry, ascertainment, and treatment history cannot be separated completely by the present analysis. The divergent tail may contain genuine resistance biology, but it may also contain biology associated with long-term illness or medication exposure. The current data cannot distinguish these possibilities.

Finally, this manuscript does not include a third schizophrenia GWAS, MAGMA analyses with gene-size or constraint covariates, human Hi-C or promoter-capture maps, single-cell causal attribution, or wet-lab validation. Those analyses constitute the next stage rather than results of the present study.

### **What would change practice**

Two developments would materially strengthen the translational case. First, an independent European-ancestry TWAS and at least one non-European replication should test whether the ten-gene block retains its sign and whether the shared-map correlation remains high. If so, a funded human-neuron perturbation panel would be justified.

Second, a TRRIP-defined treatment-resistant and treatment-responsive cohort should test whether AMIGO1, CNTN1, CDH10, ST8SIA2, ITM2B, and KCNQ2 remain off-diagonal after adjustment for smoking, illness duration, clozapine exposure, and related clinical variables. Persistence of the tail under those controls would support its use in treatment-stratification studies. Neither result is established here. Both are direct consequences of stating the architecture at the level supported by the data.

## **Conclusion**

Persistent DOI-associated enhancer genes tested against two schizophrenia TWAS datasets resolve to a bidirectional architecture whose most robust negative object is a ten-gene cytoskeletal/guidance block, not a collection of independent GO pathways.

The clozapine-enriched proxy retains this shared architecture and adds a minority divergent tail, including an adhesion and neurite candidate list and a separate KCNQ2 excitability hypothesis. This pattern supports shared-target discovery with stratified follow-up rather than a second molecular map for treatment resistance.

The next translational step is experimental: morphology and excitability assays in human neurons, together with TRRIP-compliant replication of the divergent candidates. Until enhancer–gene contacts, cell type, and treatment-naive resistance contrasts are established, the correct claim is association with a shared plasticity-related regulatory neighbourhood.

## **References**

1. International Schizophrenia Consortium. Common polygenic variation contributes to risk of schizophrenia and bipolar disorder. *Nature*. 2009;460(7256):748-752. doi:10.1038/nature08185

2. Schizophrenia Working Group of the Psychiatric Genomics Consortium. Biological insights from 108 schizophrenia-associated genetic loci. *Nature*. 2014;511(7510):421-427. doi:10.1038/nature13595

3. Pardiñas AF, Holmans P, Pocklington AJ, et al. Common schizophrenia alleles are enriched in mutation-intolerant genes and in regions under strong background selection. *Nat Genet*. 2018;50(3):381-389. doi:10.1038/s41588-018-0059-2

4. Trubetskoy V, Pardiñas AF, Qi T, et al. Mapping genomic loci implicates genes and synaptic biology in schizophrenia. *Nature*. 2022;604(7906):502-508. doi:10.1038/s41586-022-04434-5

5. Fromer M, Pocklington AJ, Kavanagh DH, et al. De novo mutations in schizophrenia implicate synaptic networks. *Nature*. 2014;506(7487):179-184. doi:10.1038/nature12929

6. Gamazon ER, Wheeler HE, Shah KP, et al. A gene-based association method for mapping traits using reference transcriptome data. *Nat Genet*. 2015;47(9):1091-1098. doi:10.1038/ng.3367

7. Gusev A, Ko A, Shi H, et al. Integrative approaches for large-scale transcriptome-wide association studies. *Nat Genet*. 2016;48(3):245-252. doi:10.1038/ng.3506

8. Wainberg M, Sinnott-Armstrong N, Mancuso N, et al. Opportunities and challenges for transcriptome-wide association studies. *Nat Genet*. 2019;51(4):592-599. doi:10.1038/s41588-019-0385-z

9. Barbeira AN, Dickinson SP, Bonazzola R, et al. Exploring the phenotypic consequences of tissue specific gene expression variation inferred from GWAS summary statistics. *Nat Commun*. 2018;9:1825. doi:10.1038/s41467-018-03621-1

10. Kane J, Honigfeld G, Singer J, Meltzer H. Clozapine for the treatment-resistant schizophrenic: a double-blind comparison with chlorpromazine. *Arch Gen Psychiatry*. 1988;45(9):789-796. doi:10.1001/archpsyc.1988.01800330013001

11. Howes OD, McCutcheon R, Agid O, et al. Treatment-resistant schizophrenia: Treatment Response and Resistance in Psychosis (TRRIP) Working Group consensus guidelines on diagnosis and terminology. *Am J Psychiatry*. 2017;174(3):216-229. doi:10.1176/appi.ajp.2016.16050503

12. Gillespie AL, Samanaite R, Mill J, Egerton A, MacCabe JH. Is treatment-resistant schizophrenia categorically distinct from treatment-responsive schizophrenia? A systematic review. *BMC Psychiatry*. 2017;17:12. doi:10.1186/s12888-016-1177-y

13. Samanaite R, Gillespie A, Sendt KV, et al. Biological predictors of clozapine response: a systematic review. *Front Psychiatry*. 2018;9:327. doi:10.3389/fpsyt.2018.00327

14. Lally J, Gaughran F, Timms P, Curran SR. Treatment-resistant schizophrenia: current insights on the pharmacogenomics of antipsychotics. *Pharmacogenomics Pers Med*. 2016;9:117-129. doi:10.2147/PGPM.S115741

15. Potkin SG, Kane JM, Correll CU, et al. The neurobiology of treatment-resistant schizophrenia: paths to antipsychotic resistance and a roadmap for future research. *NPJ Schizophr*. 2020;6:1. doi:10.1038/s41537-019-0090-z

16. de la Fuente Revenga M, Zhu B, Guevara CA, et al. Prolonged epigenomic and synaptic plasticity alterations following single exposure to a psychedelic in mice. *Cell Rep*. 2021;37(3):109836. doi:10.1016/j.celrep.2021.109836

17. Fulco CP, Nasser J, Jones TR, et al. Activity-by-contact model of enhancer-promoter regulation from thousands of CRISPR perturbations. *Nat Genet*. 2019;51(12):1664-1669. doi:10.1038/s41588-019-0538-0

18. Nasser J, Bergman DT, Fulco CP, et al. Genome-wide enhancer maps link risk variants to disease genes. *Nature*. 2021;593(7858):238-243. doi:10.1038/s41586-021-03446-x

19. Andersson R, Gebhard C, Miguel-Escalada I, et al. An atlas of active enhancers across human cell types and tissues. *Nature*. 2014;507(7493):455-461. doi:10.1038/nature12787

20. Roadmap Epigenomics Consortium. Integrative analysis of 111 reference human epigenomes. *Nature*. 2015;518(7539):317-330. doi:10.1038/nature14248

21. PsychENCODE Consortium. Revealing the brain’s molecular architecture. *Science*. 2018;362(6420):1262-1270. doi:10.1126/science.aau5139

22. Won H, de la Torre-Ubieta L, Stein JL, et al. Chromosome conformation elucidates regulatory relationships in developing human brain. *Nature*. 2016;538(7626):523-527. doi:10.1038/nature19847

23. Bigdeli TB, Chatzinakos C, Bendl J, et al. Biological insights into schizophrenia from ancestrally diverse populations. *Nature*. 2026;651(8105):404-413. doi:10.1038/s41586-025-10000-6

24. Lam M, Chen CY, Li Z, et al. Comparative genetic architectures of schizophrenia in East Asian and European populations. *Nat Genet*. 2019;51(12):1670-1678. doi:10.1038/s41588-019-0512-x

25. de Leeuw CA, Neale BM, Heskes T, Posthuma D. The statistical properties of gene-set analysis. *Nat Rev Genet*. 2016;17(6):353-364. doi:10.1038/nrg.2016.29

26. Dityatev A, Schachner M. Extracellular matrix molecules and synaptic plasticity. *Nat Rev Neurosci*. 2003;4(6):456-468. doi:10.1038/nrn1115

27. Dent EW, Gertler FB. Cytoskeletal dynamics and transport in growth cone motility and axon guidance. *Neuron*. 2003;40(2):209-227. doi:10.1016/S0896-6273(03)00633-0

28. Hall A, Lalli G. Rho and Ras GTPases in axon growth, guidance, and branching. *Cold Spring Harb Perspect Biol*. 2010;2(3):a001818. doi:10.1101/cshperspect.a001818

29. Law AJ, Kleinman JE, Weinberger DR, Weickert CS. Disease-associated intronic nucleotide polymorphism in the ErbB4 gene predicts altered ErbB4 splice-variant expression in schizophrenia. *Proc Natl Acad Sci U S A*. 2007;104(52):20919-20924. doi:10.1073/pnas.0710141104

30. Mei L, Xiong WC. Neuregulin 1 and schizophrenia: 10 years later. *Cell Mol Life Sci*. 2008;65(16):2576-2590. doi:10.1007/s00018-008-8222-5

31. Fazzari P, Paternain AV, Valiente M, et al. Control of cortical GABA circuitry development by Nrg1 and ErbB4 signalling. *Nature*. 2010;464(7293):1376-1380. doi:10.1038/nature08928

32. Penzes P, Cahill ME, Jones KA, Srivastava DP, Woolfrey KM. Dendritic spine pathology in neuropsychiatric disorders. *Nat Neurosci*. 2011;14(3):285-293. doi:10.1038/nn.2741

33. Südhof TC. Towards an understanding of synapse formation. *Neuron*. 2018;100(2):276-293. doi:10.1016/j.neuron.2018.09.040

34. Cameron LP, Tombari RJ, Lu J, et al. A non-hallucinogenic psychedelic analogue with therapeutic potential. *Nature*. 2021;589(7842):474-479. doi:10.1038/s41586-020-3008-z

35. Bean BP. The action potential in mammalian central neurons. *Nat Rev Neurosci*. 2007;8(6):451-465. doi:10.1038/nrn2148

36. Adelman JP, Maylie J, Sah P. Small-conductance Ca2+-activated K+ channels: form and function. *Annu Rev Physiol*. 2012;74:245-269. doi:10.1146/annurev-physiol-020911-153336

37. Shah MM. Cortical HCN channels: function, trafficking and plasticity. *J Physiol*. 2014;592(13):2711-2719. doi:10.1113/jphysiol.2013.270058

