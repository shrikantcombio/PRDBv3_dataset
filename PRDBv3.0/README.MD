# PRDBv3 Dataset

## Overview
The **PRDBv3** dataset provides structural and functional information on protein-RNA complexes, with a focus on docking cases, binding affinities, and flexibility classifications. It includes structural details of both complexed (C) and unbound (U) states of proteins and RNAs from various organisms.

## File Information
- **Filename:** PRDBv3_info.json
- **Format:** JSON
- **Data Entries:** Multiple records, each containing details on a protein-RNA complex

## Data Fields
Each record in the dataset consists of the following key-value pairs:

### General Information
- **C_PDB**: PDB ID of the complexed structure
- **U_pro_PDB**: PDB ID of the unbound protein
- **U_RNA_PDB**: PDB ID of the unbound RNA (if available)
- **Structural_class**: Classification of the complex (A, B, C, etc.)
- **Flexible_class**: Flexibility category (Rigid (R), Flexible (F), Semi-flexible (S))
- **Docking_case**: Type of docking scenario (e.g., UU, UB)
- **Binding_affinity**: Whether the protein-RNA complex exhibits binding affinity (yes/no)

### Protein Information
- **C_pro_name**: Name of the protein in the complex
- **C_pro_source_organism**: Organism from which the protein originates
- **C_pro_seq_length**: Length of the protein sequence
- **C_pro_chain**: Chain ID of the protein
- **U_pro_structure_title**: Title of the unbound protein structure
- **U_pro_source_organism**: Organism for the unbound protein
- **U_pro_seq_length**: Length of the unbound protein sequence
- **U_pro_macromolecule_name**: Name of the unbound protein macromolecule

### RNA Information
- **C_RNA_name**: Name of the RNA in the complex
- **C_RNA_source_organism**: Organism from which the RNA originates
- **C_RNA_seq_length**: Length of the RNA sequence
- **C_RNA_chain**: Chain ID of the RNA
- **U_RNA_structure_title**: Title of the unbound RNA structure (if available)
- **U_RNA_source_organism**: Source organism of the unbound RNA
- **U_RNA_seq_length**: Length of the unbound RNA sequence
- **U_RNA_macromolecule_name**: Name of the unbound RNA macromolecule

### Structural Information
- **C_structure_title**: Description of the complexed structure
- **C_resolution**: Resolution of the complexed structure (Å)
- **C_chain_PR**: Chain mapping between protein and RNA
- **U_pro_resolution**: Resolution of the unbound protein structure (Å)
- **U_RNA_resolution**: Resolution of the unbound RNA structure (Å)

## Usage
This dataset can be used for:
- Studying protein-RNA interactions
- Benchmarking docking and molecular modeling algorithms
- Understanding binding affinities and structural flexibility of complexes

## Citation
If you use this dataset in your research, please cite the relevant sources or publications associated with the data.

