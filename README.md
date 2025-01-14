# Supplementry materials
## Protein-RNA Docking Benchmark v3.0 integrated with Binding Affinity
Shri Kant, NITHIN Chandran, Sunandan Mukherjee, et al. Protein-RNA Docking Benchmark v3.0 integrated with Binding Affinity. Authorea. September 23, 2024.
DOI:[10.22541/au.172712541.17955138/v1](https://doi.org/10.22541/au.172712541.17955138/v1)
### Protein-RNA docking benchmark dataset
1. A script is included to generate the figures used in this manuscript.
2. Tables are provided in JSON and CSV format. 
### Protein-RNA binding affinity dataset
### Protein domain details of PRDBv3.0
### Description of the protein-RNA docking benchmark v3.0
The downloadable protein-RNA benchmark version 3.0 dataset contains 197 directories, each named according to the protein-RNA complex present in our benchmark. For example, the directory '1ASY' corresponds to a protein-RNA complex Aspartyl-tRNA synthetase/ tRNA (ASP). Each of the directories contains the files described below (1ASY is taken as an example). The files containing the atomic coordinates are in '.pdb' format.
1ASY.pdb: This file contains the atomic coordinates of the protein-RNA complex. The 4-letter PDB code represents it and contains only those chains that have been used in Table 1 and Table S1
1EOV.pdb: This file contains the atomic coordinates of the unbound protein structure corresponding to the bound complex 1asy.pdb.
2TRA.pdb: This file contains the atomic coordinates of the unbound RNA structure corresponding to the bound complex 1asy.pdb.
1ASY_1EOV.pdb: The coordinates of the superposed bound and unbound protein structures are given in this file. The file has been named the bound structure, followed by the unbound structure.
1ASY_2TRA.pdb: Same as above for the superposed bound and unbound RNA structures. Model 1 represents the bound structure, and model 2 is the transformed unbound RNA structure.
1ASY_mod.pdb: The modified version of the protein-RNA complex. Only the residues and nucleotides available in the unbound structure are retained in this file. The residues and nucleotides have been renumbered starting from the same numbers that followed in the modified unbound PDBs.
1EOV_mod.pdb: The modified version of the unbound protein file. Only the residues available in the bound structure are retained in this file. The residues have been renumbered starting from the same as the modified bound PDBs.
2TRA_mod.pdb: The modified version of the unbound RNA file. Only the nucleotides available in the bound structure are retained in this file. The nucleotides have been renumbered starting from one, the same as the modified bound PDBs.
