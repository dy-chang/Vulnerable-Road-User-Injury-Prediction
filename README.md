# NYC Vulnerable Road User (VRU) Injury Prediction
**AUC-ROC: 0.57 baseline → 0.82 with domain-informed feature engineering**

> A Transportation Data Science portfolio project demonstrating that  
> *problem framing matters more than algorithm choice.*

---

## Quick Start

```bash
pip install -r requirements.txt
jupyter lab nyc_vru_injury_prediction.ipynb
```

The notebook fetches live data from the NYC Open Data SODA API — no manual downloads needed.

## Project Summary

| | |
|---|---|
| **Data** | 30,000 NYC crash records (2023–2026), NYC Open Data SODA API |
| **Target** | `vru_injury`: pedestrian or cyclist was injured |
| **Best model** | Random Forest, rich features + class-weight balanced |
| **Best AUC-ROC** | **0.820** |
| **VRU Recall** | **75%** (3 of 4 actual VRU crashes detected) |

## AUC Improvement Path

| Model | Features | AUC-ROC |
|---|---|---|
| LR baseline | Temporal + borough | 0.609 |
| RF baseline | Temporal + borough | 0.620 |
| LR improved | Rich + class balanced | 0.818 |
| GB improved | Rich + class balanced | 0.816 |
| **RF improved** | **Rich + class balanced** | **0.820 ✓** |

**Why it improved:** redesigned target variable + domain feature engineering  
(vehicle types, multi-vehicle flag, cyclic time encoding, NLP on contributing factors).

## Skills Demonstrated

- REST API ingestion (NYC Open Data SODA)  
- Transportation-domain feature engineering  
- Imbalanced classification (class weighting, AUC-ROC, Precision-Recall)  
- Random Forest, Gradient Boosting, Logistic Regression  
- Feature importance + partial dependence interpretation  
- Vision Zero policy communication

## Author

**Daeyeol Chang, Ph.D.**  
Postdoctoral Researcher, Morgan State University  
Transportation Data Scientist — travel demand modeling · evacuation simulation · urban safety analytics
