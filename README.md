# Differential Expression Analysis of **GCM1** Knock‑out vs. Wild‑type

This repository contains an R‑based RNA‑seq workflow that identifies differentially expressed genes (DEGs) between **GCM1** knock‑out (KO) and wild‑type (WT) samples, visualises the results, and performs Gene Ontology (GO) enrichment analysis.

---

## Project Contents

| File/Folder        | Description                                                                                        |
| ------------------ | -------------------------------------------------------------------------------------------------- |
| **analysis.ipynb** | Jupyter notebook (R kernel) containing the complete analysis pipeline.                             |
| `data/`            | count matrix (`counts.tsv`) and sample metadata (`metadata.tsv`). |

> **Note**: Large data files are *not* included in the repo.

---

## Input Files

| File           | Format        | Required columns                                             |
| -------------- | ------------- | ------------------------------------------------------------ |
| `counts.tsv`   | tab‑separated | `gene_id` + raw integer counts per sample                    |
| `metadata.tsv` | tab‑separated | `sample` *(row names)*, `condition` (`WT`/`KO`), `replicate` |

Example `metadata.tsv`:

```tsv
		condition	replicate	path
GCM1_KO_C1	KO		C1		GCM1_KO_C1_GT23-11436_TCCAACGC-AAGTCCAA_S58_L002
GCM1_KO_E4	KO		E4		GCM1_KO_E4_GT23-11437_CCGTGAAG-ATCCACTG_S56_L002
GCM1_KO_G4	KO		G4		GCM1_KO_G4_GT23-11438_TTACAGGA-GCTTGTCA_S53_L002
GCM1_WT_1	WT		1		GCM1_WT_1_GT23-11433_ACTAAGAT-CCGCGGTT_S57_L002
GCM1_WT_2	WT		2		GCM1_WT_2_GT23-11434_GTCGGAGC-TTATAACC_S46_L002
GCM1_WT_3	WT		3		GCM1_WT_3_GT23-11435_CTTGGTAT-GGACTTGG_S41_L002
```
---


