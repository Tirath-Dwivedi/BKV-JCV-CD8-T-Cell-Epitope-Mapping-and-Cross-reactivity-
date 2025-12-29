# BKV-JCV-CD8-T-Cell-Epitope-Mapping-and-Cross-reactivity-
Epitope sequence cross-reactivity analysis


This repository provides tools to compute and visualize peptide similarity between BK polyomavirus (BKV) and JC polyomavirus (JCV) epitopes using the method described in Frankild et al., 2008. It identifies 13 mismatch peptide pairs, scores their similarity, categorizes them, and produces annotated heatmaps for visual analysis.

Features

Compute asymmetric peptide similarity using BLOSUM62.

Filter BKVJCV epitope pairs with 13 amino acid mismatches.

Categorize similarity scores:

High ( 0.90)

Moderate (0.800.89)

Low (< 0.80)

Output a summary table with similarity scores, mismatch counts, and categories.

Installation

Ensure Python  3.8 and install required dependencies:

pip install biopython matplotlib seaborn numpy pandas

Usage

Clone the repository:

git clone <repo-url>
cd <repo-folder>


Run the analysis script:

python BLOSUM_peptide_similarity_analysis.py



Methodology

### BLOSUM peptide similarity score

The similarity between a BKV peptide $x$ and a JCV peptide $y$ is computed as a normalized score:

$$
S(x,y) = \frac{A(x,y) - A_x^{\min}}{A_x^{\max} - A_x^{\min}}
$$

where

- $A(x,y)$ is the sum of BLOSUM62 scores for aligned residues between $x$ and $y$.
- $A_x^{\max}$ is the sum of BLOSUM62 scores for identical residues in $x$ (the self-score).
- $A_x^{\min}$ is the sum of the worst possible substitutions for the residues in $x$.

This normalization scales the raw BLOSUM sum to the range $[0,1]$, facilitating comparison across peptides of the same length.

Filtering

Only pairs with 13 mismatches are considered.

Visualization

Heatmaps show BLOSUM62 scores for each residue pair.


Dependencies

Biopython

NumPy

Pandas

Matplotlib

Seaborn

References

Frankild, S., de Boer, R., Lund, O., & Nielsen, M. (2008). Extending the functionality of peptideMHC class I binding predictions using similarity matrices. BMC Bioinformatics, 9, 369.

Henikoff, S., & Henikoff, J. G. (1992). Amino acid substitution matrices from protein blocks. PNAS, 89(22), 1091510919.

## BLOSUM workflow

![BLOSUM workflow](BLOSUM%20workflow.png)
