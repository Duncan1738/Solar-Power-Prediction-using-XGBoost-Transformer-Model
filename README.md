# Transformer-Based Solar Power Forecasting with Minimal Feature Selection

This repository presents the code and methodology behind the paper:

**"Enhanced Time Series-Based Solar Power Prediction Using Minimal Feature Selection"**

##  Overview

This project implements a Transformer-based deep learning model for solar power forecasting. Unlike traditional models that rely on dozens of meteorological features, this approach uses **only two features**  *solar irradiance* and *soil temperature* —identified through SHAP feature importance analysis using XGBoost.

Despite the reduced input complexity, the model achieves a **Mean Absolute Error (MAE) of 1.1325**, comparable to a full multivariate Transformer model.

##  Experimental Setup

- **Dataset**: Real-world PV generation and weather data (Gangjin County, South Korea, 2019–2022)
- **Preprocessing**:
  - StandardScaler normalization
  - Sliding window of size 5 for time-series forecasting
- **Feature Selection**:
  - XGBoost + SHAP for importance ranking
- **Model**: Transformer with:
  - 2 encoder layers
  - 2 attention heads
  - Embedding dimension: 64
  - Dropout: 0.1

##  Training Details

- Framework: PyTorch
- Optimizer: Adam
- Learning Rate: 1e-3
- Loss Function: MSE
- Batch Size: 32
- Epochs: 500
- Evaluation Metrics: MAE, RMSE, R²

##  Results Summary

| Model        | MAE (Univariate) | MAE (Multivariate) |
|--------------|------------------|--------------------|
| RNN          | 1.22             | 4.51               |
| GRU          | 1.60             | 3.84               |
| LSTM         | 1.22             | 2.02               |
| Transformer  | 1.21             | **1.14**           |
| **Proposed** | **1.1325**       | (Minimal features) |

---

##  Key Contributions

- Demonstrates effective forecasting using only two features
- Integrates SHAP-based explainability for model interpretability
- Outperforms baseline RNN/GRU/LSTM models with fewer inputs

---

## Citation

If you use this work, please cite: I will update as soon as the paper gets published.


```bibtex
@inproceedings{kibet2025solar,
  title={Enhanced Time Series-Based Solar Power Prediction Using Minimal Feature Selection},
  author={Kibet, Duncan and So, Min Seop and Kang, Hahyeon and Shin, Jong-Ho},
  booktitle={Proceedings of the XXX Workshop},
  year={2025}
}
```

##  Contact

For questions or data access, contact:  
**duncankibet90@gmail.com** 
