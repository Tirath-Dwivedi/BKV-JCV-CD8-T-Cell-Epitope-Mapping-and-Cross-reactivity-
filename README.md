# BKV-JCV-CD8-T-Cell-Epitope-Mapping-and-Cross-reactivity-
Epitope sequece cross-reactivity analysis

Cross-reactivity
To identify cross-reactivity of BKV epitopes across different strains of JCV This Python script aims to analyze cross-reactive epitopes between BKV and JCV by matching epitopes from one dataset with protein sequences from another dataset. The analysis involves reading Excel files containing epitopes and protein sequences, identifying matches, and generating pivot tables to summarize the occurrence of epitopes across different strains.

Dependencies:
Python 3.x Pandas Seaborn Regular Expressions (re)

Files:
crossreactive_epitope_analysis.py Purpose: Matches epitopes from one dataset with protein sequences from another dataset to identify cross-reactive epitopes between BKV and JCV. Usage: Execute this script after placing the respective Excel files (BKV_scored_epitopes.xlsx and JCV_strains_protein_sequences.xlsx) in the same directory. It generates result files: results_BKV_crossreactive_epitopes.xlsx and pivot_table_BKV_crossreactive_epitopes.xlsx.
Instructions:
Running the Script: Ensure all required packages are installed (Pandas, Seaborn). Place the input Excel files (BKV_scored_epitopes.xlsx and JCV_strains_protein_sequences.xlsx) in the same directory as the script. Run the script to perform epitope matching and pivot table generation for cross-reactive epitopes.

Input Files:
BKV_scored_epitopes.xlsx: Contains epitopes for BKV. JCV_strains_protein_sequences.xlsx: Contains protein sequences for JCV strains.

Output Files:
Upon execution, the script generates two output files: results_BKV_crossreactive_epitopes.xlsx: Epitopes matched with gene names and strains. pivot_table_BKV_crossreactive_epitopes.xlsx: Pivot table summarizing epitope occurrences across strains.

Adjustments:
Modify the file paths in the script if the input file locations or names change. Customize additional data processing or visualization as needed for further analysis.
