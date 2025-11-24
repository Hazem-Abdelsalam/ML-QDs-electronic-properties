# Machine Learning Prediction of Frontier Orbital Energies in Graphene and Silicon Carbide Quantum Dots

This repository contains the dataset, code, and trained models associated with our work on predicting the highest occupied molecular orbital (HOMO) and lowest unoccupied molecular orbital (LUMO) energies of functionalized graphene quantum dots (GQDs) and silicon carbide quantum dots (SiCQDs) using graph neural networks.

## 📊 Dataset

- **File**: `data/GQDs_SiCQDs_Data.csv`
- **Size**: 254 quantum dot structures
- **Properties**: DFT-computed `E_HOMO` and `E_LUMO` (in eV)
- **Functional groups**: COOH, COH, NO₂, CN, SO₂H, POH, and dopants (B, N, S, O)
- **Computational method**: B3LYP/6-31G in Gaussian 16

## 💻 Code

- **File**: `code/ML_GQDs_Training.ipynb`
- **Framework**: [Chemprop v2](https://github.com/chemprop/chemprop) (D-MPNN)
- **Environment**: Google Colab (Python, PyTorch, RDKit)
- **Tasks**: SMILES conversion, data loading, 5-fold cross-validation, property prediction

> 🔗 To run: Open the notebook in Google Colab and follow the cells from top to bottom.

## 📈 Key Results

- **Test set performance**:  
  - HOMO: R² = 0.95, MAE = 0.15 eV  
  - LUMO: R² = 0.90, MAE = 0.15 eV
- **5-Fold CV**: Confirms robustness of HOMO prediction; LUMO more sensitive to chemical diversity.

## 📄 Citation

If you use this dataset or code, please cite our manuscript:

> Abdelsalam, H., Wang, Z., Teleb, N. H., Abd-Elkader, O. H., Zhang, L., & Zhang, Q. (2025).  
> *Machine Learning Prediction of Frontier Orbital Energies in Graphene and Silicon Carbide Quantum Dots.*


