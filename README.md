# BKV-JCV-CD8-T-Cell-Epitope-Mapping-and-Cross-reactivity-
Epitope sequece cross-reactivity analysis


This repository provides tools to compute and visualize peptide similarity between BK polyomavirus (BKV) and JC polyomavirus (JCV) epitopes using the method described in Frankild et al., 2008. It identifies 1–3 mismatch peptide pairs, scores their similarity, categorizes them, and produces annotated heatmaps for visual analysis.

Features

Compute asymmetric peptide similarity using BLOSUM62.

Filter BKV–JCV epitope pairs with 1–3 amino acid mismatches.

Categorize similarity scores:

High (≥ 0.90)

Moderate (0.80–0.89)

Low (< 0.80)

Output a summary table with similarity scores, mismatch counts, and categories.

Installation

Ensure Python ≥ 3.8 and install required dependencies:

pip install biopython matplotlib seaborn numpy pandas

Usage

Clone the repository:

git clone <repo-url>
cd <repo-folder>


Run the analysis script:

python BLOSUM_peptide_similarity_analysis.py



Methodology
BLOSUM Peptide Similarity Score

The similarity between a BKV peptide 
𝑥
x and a JCV peptide 
𝑦
y is computed as:

𝑆
(
𝑥
,
𝑦
)
=
𝐴
(
𝑥
,
𝑦
)
−
𝐴
𝑥
min
⁡
𝐴
𝑥
max
⁡
−
𝐴
𝑥
min
⁡
S(x,y)=
A
x
max
	​

−A
x
min
	​

A(x,y)−A
x
min
	​

	​


𝐴
(
𝑥
,
𝑦
)
A(x,y) = sum of BLOSUM62 scores for aligned residues

𝐴
𝑥
max
⁡
A
x
max
	​

 = sum of BLOSUM62 scores for identical residues in 
𝑥
x

𝐴
𝑥
min
⁡
A
x
min
	​

 = sum of the worst possible substitutions in 
𝑥
x

Filtering

Only pairs with 1–3 mismatches are considered.

Visualization

Heatmaps show BLOSUM62 scores for each residue pair.


Dependencies

Biopython

NumPy

Pandas

Matplotlib

Seaborn

References

Frankild, S., de Boer, R., Lund, O., & Nielsen, M. (2008). Extending the functionality of peptide–MHC class I binding predictions using similarity matrices. BMC Bioinformatics, 9, 369.

Henikoff, S., & Henikoff, J. G. (1992). Amino acid substitution matrices from protein blocks. PNAS, 89(22), 10915–10919.

## BLOSUM workflow

![BLOSUM workflow](BLOSUM%20workflow.png)

