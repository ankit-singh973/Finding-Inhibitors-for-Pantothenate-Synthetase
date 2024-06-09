#  **Pantothenate synthetase protein inhibitor finding**
 A ML classification model is created to find potential ligand molecules for Pantothenate synthetase protein to inhibiting Micobacterium Tuberculosis replication

## **Literature Review**
- Pantothenate synthetase is an enzyme found in **Mycobacterium tuberculosis**. This enzyme plays a crucial role in the `biosynthesis of coenzyme A (CoA)`, a molecule essential for multiple metabolic pathways, including the synthesis and degradation of fatty acids.
- `Inhibition of pantothenate synthetase can disrupt the biosynthesis of CoA`, leading to the impairment of essential metabolic processes in M. tuberculosis.
- This makes pantothenate synthetase an `attractive target` for the development of novel anti-tuberculosis drugs. Inhibitors of pantothenate synthetase have the potential to selectively target the bacteria without harming the host cells.

### **This project is divided into 3 phases:**
 1. Machine Learning classification model building and screening of DrugBank
 2. Virtual screening of potential active molecules using Maestro
 3. Perform MD Simulation of selected molecules using Gromacs

## **1. ML part**
## **Steps Involved**
1. Pantothenate synthetase protein bioactivity data collection from CHEMBL
2. Selecting data on the basis of IC50 values
3. Pre-processing data (handling missing values, removing invalid smiles, converting smiles to canonical smiles)
4. Dividing molecules into active and inactive on the basis of IC50 values (`IC50<=1000nM --> Active`, `IC50>=10000nM ----> Inactive`)
5. Generating Morgan fingerprints using rdkit
6. Applying PCA to reduce dimesnion of data
7. Training various machine learning classification models and selecting the best ones
8. Screening drug bank molecules uing trained models to get potential active molecules

**Result:** After screening we got 103 potential active molecules and virtual screening performed on these molecules.
**Learning:** In this project I have learned how to use machine learning algorithms when we have very less data available
