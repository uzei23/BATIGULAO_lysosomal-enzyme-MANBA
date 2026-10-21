# Lysosomal Enzyme Analysis: Beta-Mannosidase (MANBA)

**Name:** BATIGULAO, JEHIAH BLESS T.  
**Date Completed:** October 14, 2026  
**Course:** Cell and Molecular Biology Laboratory

## 1. Enzyme Summary

- **Enzyme name:** Beta-mannosidase (lysosomal beta-mannosidase)
- **Gene symbol:** *MANBA*
- **NCBI Gene ID:** [4126](https://www.ncbi.nlm.nih.gov/gene/4126)
- **Organism:** *Homo sapiens*
- **NCBI protein accession:** [NP_005899.3](https://www.ncbi.nlm.nih.gov/protein/NP_005899.3)
- **Protein length:** 879 amino acids
- **Normal function:** Beta-mannosidase is a lysosomal enzyme that removes terminal beta-linked mannose residues from mannose-containing oligosaccharides produced during glycoprotein degradation. This process contributes to the breakdown and recycling of complex carbohydrate-containing molecules within lysosomes.

## 2. Objective

The objective of this activity was to retrieve a human lysosomal enzyme protein sequence from NCBI, analyze its amino acid composition, identify potential N-linked glycosylation motifs, visualize the results using R, and document the analysis in a reproducible format.

## 3. Methods

The human MANBA protein sequence was retrieved from the NCBI Protein database using the RefSeq accession NP_005899.3 and the R package `rentrez`.

The R script performed the following steps:

1. Checked whether the required R packages, `rentrez` and `ggplot2`, were installed.
2. Created the `data/`, `results/`, and `figures/` output directories.
3. Retrieved the protein sequence in FASTA format from NCBI and saved it as `data/MANBA.fasta`.
4. Calculated the total protein length and the count and percentage of each of the 20 standard amino acids.
5. Identified potential N-glycosylation motifs following the sequence pattern N-X-S/T, where X is any standard amino acid except proline (P).
6. Exported the summary, amino acid composition, and motif positions as CSV files.
7. Generated PNG figures showing amino acid composition and the positions of potential N-glycosylation motifs.

The motif positions use one-based numbering from the beginning of the retrieved precursor protein sequence.

## 4. Results

### 4.1 Protein Summary

| Gene | Accession | Protein length (aa) | Potential N-glycosylation motifs |
|---|---|---:|---:|
| MANBA | NP_005899.3 | 879 | 8 |

The analyzed MANBA precursor sequence contained 879 amino acids and eight potential N-glycosylation motifs.

### 4.2 Amino Acid Composition

The amino acid composition was calculated by counting each standard amino acid and dividing its count by the total sequence length to obtain its percentage.

| Amino acid | Count | Percentage (%) |
|---|---:|---:|
| A (Alanine) | 41 | 4.66 |
| C (Cysteine) | 17 | 1.93 |
| D (Aspartic acid) | 40 | 4.55 |
| E (Glutamic acid) | 58 | 6.60 |
| F (Phenylalanine) | 53 | 6.03 |
| G (Glycine) | 52 | 5.92 |
| H (Histidine) | 21 | 2.39 |
| I (Isoleucine) | 49 | 5.57 |
| K (Lysine) | 39 | 4.44 |
| L (Leucine) | 77 | 8.76 |
| M (Methionine) | 15 | 1.71 |
| N (Asparagine) | 45 | 5.12 |
| P (Proline) | 39 | 4.44 |
| Q (Glutamine) | 42 | 4.78 |
| R (Arginine) | 33 | 3.75 |
| S (Serine) | 77 | 8.76 |
| T (Threonine) | 50 | 5.69 |
| V (Valine) | 62 | 7.05 |
| W (Tryptophan) | 27 | 3.07 |
| Y (Tyrosine) | 42 | 4.78 |

Leucine (L) and serine (S) were tied as the most abundant amino acids, with 77 residues each (8.76%). Valine (V) was the third most abundant, with 62 residues (7.05%), followed by glutamic acid (E), with 58 residues (6.60%), and phenylalanine (F), with 53 residues (6.03%).

### 4.3 Potential N-Glycosylation Motifs

The sequence analysis identified eight potential N-X-S/T motifs.

| Position | Motif |
|---:|:---:|
| 28 | NWS |
| 35 | NGS |
| 77 | NWT |
| 280 | NIS |
| 284 | NIT |
| 297 | NQT |
| 302 | NMT |
| 763 | NCT |

Each motif satisfies the sequence rule N-X-S/T, with no proline at the middle position. The positions indicate the asparagine (N) residue at the beginning of each motif.

These are potential glycosylation sites predicted from the primary amino acid sequence. Their identification does not establish whether the sites are actually glycosylated in the mature protein.

## 5. Figures

### Figure 1. Amino Acid Composition of MANBA

<img width="2400" height="1350" alt="MANBA_amino_acid_composition" src="https://github.com/user-attachments/assets/ab2b7bef-f1b6-4a10-b2a1-157fe2cdbba6" />

Figure 1 shows the counts of the 20 standard amino acids in the 879-amino-acid MANBA precursor. Leucine (L) and serine (S) have the highest counts, with 77 residues each.

### Figure 2. Positions of Potential N-Glycosylation Motifs

<img width="2400" height="990" alt="MANBA_potential_N_glycosylation" src="https://github.com/user-attachments/assets/07fde568-3a3a-423b-a597-c7dc999400bb" />


Figure 2 shows the locations of the eight potential N-X-S/T motifs along the MANBA precursor sequence. The positions were identified computationally and do not confirm actual glycan attachment.

## 6. Laboratory Questions and Answers

### 1. What does your enzyme normally break down inside lysosomes?

MANBA encodes beta-mannosidase, a lysosomal enzyme that removes terminal beta-linked mannose residues from mannose-containing oligosaccharides produced during glycoprotein degradation. This contributes to lysosomal carbohydrate degradation and recycling.

### 2. What is the total length of your protein, and which amino acids are most common?

The analyzed MANBA precursor protein is 879 amino acids long. Leucine (L) and serine (S) are tied as the most abundant amino acids, with 77 residues each (8.76%). They are followed by valine (V), with 62 residues (7.05%); glutamic acid (E), with 58 residues (6.60%); and phenylalanine (F), with 53 residues (6.03%).

### 3. How many potential N-glycosylation motifs did you find? Where are they located?

The analysis identified eight potential N-X-S/T motifs at positions 28 (NWS), 35 (NGS), 77 (NWT), 280 (NIS), 284 (NIT), 297 (NQT), 302 (NMT), and 763 (NCT). The positions refer to the asparagine residue at the start of each motif in the 879-amino-acid precursor sequence.

### 4. Why can glycosylation matter for lysosomal proteins? Does finding a motif prove the protein is glycosylated?

N-linked glycosylation can contribute to protein folding, stability, quality control, and trafficking through the secretory pathway. Many soluble lysosomal enzymes receive mannose-6-phosphate (M6P) modifications on their N-linked glycans, which are recognized by receptors involved in lysosomal targeting. However, identifying an N-X-S/T motif does not prove that glycosylation occurs at that site. Actual glycan attachment depends on factors such as protein structure, site accessibility, and cellular processing. Sequence analysis alone also cannot establish whether MANBA carries an M6P tag.

### 5. What could happen in the cell if your enzyme did not work properly?

If beta-mannosidase is deficient or nonfunctional, mannose-containing oligosaccharides may accumulate because they cannot be degraded efficiently. Pathogenic variants in *MANBA* cause beta-mannosidosis, a rare lysosomal storage disorder that can affect neurological function and other body systems. Clinical severity varies among affected individuals.

## 7. Notes and Limitations

- N-X-S/T motifs are potential N-glycosylation sites, not experimental confirmation of glycan attachment.
- A potential N-glycosylation motif does not demonstrate the presence of an M6P targeting marker.
- The analysis describes the retrieved primary amino acid sequence and does not directly measure protein structure, glycosylation, enzyme activity, or lysosomal localization.
- Motif positions are numbered relative to the complete retrieved precursor sequence.
- The reported protein length, amino acid composition, and motif count correspond to the R script output for accession NP_005899.3.

## 8. Reproducibility

### Requirements


Install the packages once in R:

```r
install.packages(c("rentrez", "ggplot2"))
```

### Configuration

The following settings were used in `lysosomal_enzyme_analysis.R`:

```r
gene <- "MANBA"
accession <- "NP_005899.3"
```

### Running the Analysis

From the repository directory, run the script in RStudio using the **Source** button or execute the following command in a terminal:

```bash
Rscript lysosomal_enzyme_analysis.R
```

Alternatively, in the R console, with the working directory set to the repository folder:

```r
source("lysosomal_enzyme_analysis.R")
```

The script retrieves the protein sequence from NCBI and generates the FASTA file, CSV results, and PNG figures.

### Expected Output Files

```text
lysosomal-enzyme-MANBA/
├── lysosomal_enzyme_analysis.R
├── README.md
├── data/
│   └── MANBA.fasta
├── results/
│   ├── MANBA_summary.csv
│   ├── MANBA_amino_acid_counts.csv
│   └── MANBA_motif_positions.csv
└── figures/
    ├── MANBA_amino_acid_composition.png
    └── MANBA_potential_N_glycosylation.png
```

## 9. Reference

National Center for Biotechnology Information (NCBI). Human beta-mannosidase (MANBA), RefSeq protein NP_005899.3.  
https://www.ncbi.nlm.nih.gov/protein/NP_005899.3

NCBI Gene: MANBA, Gene ID 4126.  
https://www.ncbi.nlm.nih.gov/gene/4126
