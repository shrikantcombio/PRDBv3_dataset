# PRDBv3.0 Dataset

## Overview
The protein-RNA docking benchmark version 3.0 (**PRDBv3.0**) is a comprehensive update to the previous benchmark, offering a significant expansion in docking test cases for evaluating protein-RNA docking methods. Key features of PRDBv3.0 include:

1. Total 197 test cases curated from 288 non-redundant protein-RNA complexes at 35% sequence identity in the Protein Data Bank.

2. Classification of docking test cases:
   - unbound-unbound (UU) cases: 27
   - unbound-bound (UB) cases: 160
   - bound-unbound (BU) cases: 10

3. Categorization based on protein interface flexibility:
   - rigid-body (R) complexes: 117
   - semi-flexible (S) complexes: 41
   - full-flexible (F) complexes: 29

4. Structural classes:
   - (A) complexes with tRNA: 40
   - (B) complexs with rRNA: 9
   - (C) complexes with duplex-RNA: 62
   - (D) complexes with signle-stranded RNA: 86 

5. Inclusion of binding affinity (Kd) values for 105 protein-RNA complexes, along with experimental details.

6. Cataloging of 255 unique RNA-binding domains present in RNA-binding proteins.

## Description of the protein-RNA docking benchmark v3.0
1. The downloadable protein-RNA benchmark version 3.0 dataset contains **197** directories, each named according to the protein-RNA complex present in our benchmark. 

   **For example**, the directory '1ASY' corresponds to a protein-RNA complex Aspartyl-tRNA synthetase/ tRNA (ASP). Each of the directories contains the files
   described below (1ASY is taken as an example). The files containing the atomic coordinates are in '.pdb' format.

2. **1ASY.pdb**: This file contains the coordinates of superposed equivalent atoms of the protein-RNA complex. Superposition is performed between bound and its corresponding unbound structure. It contains only the protein and the RNA chains mentioned in Table 1 and Table S1.

3. **1ASY_full.pdb**: This file contains the full atomic coordinates of the protein-RNA complex as obtained from PDB.  The 4-letter PDB code contains only those chains that have been used in Table 1 and Table S1.

4. **1EOV.pdb**: This file contains the equivalent atomic coordinates of the unbound protein structure corresponding to the bound complex 1ASY.pdb.

5. **1EOV_full.pdb**: This file contains the full atomic coordinates of the unbound protein structure as obtained from PDB.  The 4-letter PDB code contains only those chains that have been used in Table 1 and Table S1.

1. **2TRA.pdb**: This file contains the equivalent atomic coordinates of the unbound RNA structure corresponding to the bound complex 1ASY.pdb.

2. **2TRA_full.pdb**: This file contains the full atomic coordinates of the unbound RNA structure as obtained from PDB.  The 4-letter PDB code contains only those chains that have been used in Table 1 and Table S1.

3. **1ASY_1EOV.pdb**: Equivalent coordinates of the superposed bound and unbound protein structures are given in this file. The file has been named on the bound structure followed by the unbound structure.

4. **1ASY_2TRA.pdb**: Same as above for the superposed bound and unbound RNA structures. In this file, model 1 represents the bound structure and model 2 represents the transformed unbound RNA structure.

5.  **1ASY_mod.pdb**: The modified version of the protein-RNA complex. Upon superposition of bound and unbound strutures, only the equivalent residues and nucleotides are retained in this file. The residues and the nucleotides have been renumbered starting from the same numbers that followed in the modified unbound PDBs.

6.  **1EOV_mod.pdb**: The modified version of the unbound protein file. Upon superposition of bound and unbound strutures, only the equivalent residues are retained in this file. Residues have been renumbered starting from the same as the modified bound PDBs.

7.  **2TRA_mod.pdb**: The modified version of the unbound RNA file. Upon superposition of bound and unbound strutures, only the equivalent nucleotides are retained in this file. Nucleotides have been renumbered starting from the same as the modified bound PDBs.

## File Information
- **Filename:** PRDBv3_info.json
- **Format:** JSON
- **Data Entries:** Multiple records, each containing details on a protein-RNA complex and their unbound structures.

## Data Fields
Each record in the dataset consists of the following key-value pairs:

### General Information
- **C_PDB**: PDB ID of the complex (bound) structure
- **U_pro_PDB**: PDB ID of the unbound protein structure
- **U_RNA_PDB**: PDB ID of the unbound RNA structure (if available)
- **Structural_class**: Structural class of the protein-RNA complex (A, B, C and D)
- **Flexible_category**: Rigid-body (R), Semi-flexible (S) and Full-Flexible (F).
- **Docking_case**: Type of docking cases (e.g., UU, UB, BU)
- **Binding_affinity**: Whether the binding affinity of a protein-RNA complex is availabile (yes/no)

### Protein Information
- **C_pro_name**: Name of the protein in the complex (bound) structure
- **C_pro_source_organism**: Organism name of the complex protein chain
- **rcsbpdb_C_pro_seq_length**: Length of amino acid construct used in complex protein chain obtained from [RCSB protein data bank](https://www.rcsb.org/) (PDB).
- **C_pro_seq_full_length**:  Full length of residues in complex protein chain obtained from [RCSB protein data bank](https://www.rcsb.org/) (PDB).
- **C_pro_seq_length**: Length of residues in complex protein chain in PRDBv3.0.
- **C_pro_chain**: Chain ID of the complex protein
- **U_pro_structure_title**: Title of the unbound protein structure
- **U_pro_source_organism**: Organism for the unbound protein structure
- **rcsbpdb_U_pro_seq_length**: Length of amino acid construct used in unbound protein chain obtained from [RCSB protein data bank](https://www.rcsb.org/) (PDB).
- **U_pro_seq_full_length**:  Full length of  residues in unbound protein chain obtained from [RCSB protein data bank](https://www.rcsb.org/) (PDB).
- **U_pro_seq_length**: Length of residues in unbound protein chain in each entry of PRDBv3.0.
- **U_pro_macromolecule_name**: Name of the unbound protein structure

### RNA Information
- **C_RNA_name**: Name of the RNA in the complex
- **C_RNA_source_organism**: Organism name of the complex RNA structure
- **rcsbpdb_C_RNA_seq_length**: Length of nucleotides construct used in unbound RNA chain obtained from [RCSB protein data bank](https://www.rcsb.org/) (PDB).
- **C_RNA_seq_full_length**: Full length of nucleotides in complex RNA chain obtained from [RCSB protein data bank](https://www.rcsb.org/) (PDB).
- **C_RNA_seq_length**: Length of the complex RNA sequence
- **C_RNA_chain**: Chain ID of the complex RNA structure in PRDBv3.0.
- **U_RNA_structure_title**: Title of the unbound RNA structure (if available)
- **U_RNA_source_organism**: Source organism of the unbound RNA
- **rcsbpdb_U_RNA_seq_length**: Length of nucleotides construct used in unbound RNA chain obtained from [RCSB protein data bank](https://www.rcsb.org/) (PDB).
- **U_RNA_seq_full_length**: Full length of nucleotides in unbound RNA chain obtained from [RCSB protein data bank](https://www.rcsb.org/) (PDB).
- **U_RNA_seq_length**: Length of nucleotides in unbound RNA chain in PRDBv3.0.
- **U_RNA_macromolecule_name**: Name of the unbound RNA 

### Structural Information
- **C_structure_title**: Title of the PDB ID of the complex structure
- **C_resolution**: Resolution of the complex structure (Å)
- **C_chain_PR**: protein and RNA chain ID in a protein-RNA complex
- **U_pro_resolution**: Resolution of the unbound protein structure (Å)
- **U_RNA_resolution**: Resolution of the unbound RNA structure (Å)

### Missing nucleotides Information
**RNA_mismatched_nucleotides**:  we have added an additional sheet namely `mismatched_nucleotide` in the PRDBv3_Supplementary_details.xlsx.
PRDBv3_Supplementary_details.xlsx can ne found in PRDBv3.0.zip file provided at http://www.csb.iitkgp.ac.in/applications/PRDBv3/PRDBv3.0.zip 

## Usage
This updated benchmark will be valuable for:
- Studying protein-RNA interactions
- Evaluating both rigid-body and flexible docking methods
- Testing methods aimed at predicting binding affinity
- Developing and improving protein-RNA docking algorithms

## Citation
If you use this dataset in your research, please cite:

Shri Kant, NITHIN Chandran, Sunandan Mukherjee, et al. Protein-RNA Docking Benchmark v3.0 integrated with Binding Affinity. Authorea. September 23, 2024. DOI:[10.22541/au.172712541.17955138/v1](https://doi.org/10.22541/au.172712541.17955138/v1)

