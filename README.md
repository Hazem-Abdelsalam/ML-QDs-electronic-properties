# Machine Learning Prediction of Frontier Orbital Energies in Graphene and Silicon Carbide Quantum Dots

This repository contains the dataset, code, and trained models associated with our work on predicting the highest occupied molecular orbital (HOMO) and lowest unoccupied molecular orbital (LUMO) energies of functionalized graphene quantum dots (GQDs) and silicon carbide quantum dots (SiCQDs) using graph neural networks.

## 📊 Dataset

- **File**: `data/GQDs_SiCQDs_Data.csv`
- **Size**: 254 quantum dot structures
- **Properties**: DFT-computed `E_HOMO` and `E_LUMO` (in eV)
- **Functional groups**: COOH, COH, NO₂, CN, SO₂H, POH, and dopants (B, N, S, O)
- **Computational method**: B3LYP/6-31G in Gaussian 16
- **Also included**: The original **PDB files** for all 254 quantum dots are provided in the `data/pdb_files/` directory,

## 💻 Code

All code is implemented in **Google Colab** using **Chemprop** (D-MPNN).

### 1. Standard Training (`code/ML_GQDs_Training.ipynb`)
- Splits data into fixed train (80%), validation (10%), and test (10%) sets.
- Trains a Chemprop model for 300 epochs.
- Evaluates performance on the held-out test set (R² ≈ 0.95 for HOMO, 0.90 for LUMO).

### 2. K-Fold Cross-Validation (`code/ML_GQDs_CV.ipynb`)
- Performs **5-fold stratified cross-validation** for robust performance estimation.
- Each fold uses 90% for training/validation and 10% for testing.
- Reports mean and per-fold metrics, highlighting sensitivity of HOMO/LUMO to chemical diversity.
- Demonstrates that while HOMO prediction is robust, LUMO is more sensitive to rare functional groups (e.g., –B, –NO₂).


## 📈 Key Results

- **Test set performance**:  
  - HOMO: R² = 0.95, MAE = 0.15 eV  
  - LUMO: R² = 0.90, MAE = 0.15 eV
- **5-Fold CV**: Confirms robustness of HOMO prediction; LUMO more sensitive to chemical diversity.

## 📄 Citation

If you use this dataset or code, please cite our manuscript:

> Abdelsalam, H., Wang, Z., Teleb, N. H., Abd-Elkader, O. H., Zhang, L., & Zhang, Q. (2025).  
> *Machine Learning Prediction of Frontier Orbital Energies in Graphene and Silicon Carbide Quantum Dots.*


