# Amazon Product Recommendation System

A recommendation engine that suggests electronics to Amazon users based on how they rated other products. It compares four modeling approaches.

**Tools:** Python · pandas · Surprise (KNN, SVD) · scikit-learn · Matplotlib · Seaborn


## Key achievements

- **Shrank 7.8 million ratings into a dataset suitable for modeling:** 65,290 ratings from 1,540 active users (50+ ratings each) on 5,689 products (5+ ratings each).
- **Built and compared four recommenders:** a popularity-based ranking, user-user and item-item collaborative filtering (KNN), and matrix factorization (SVD).
- **Tuned each model with GridSearchCV** (3-fold cross-validation), which improved F1 for every model.
- **Best model: tuned SVD**, with **precision@10 of 0.86, recall@10 of 0.81 and F1 of 0.84**. It also made real predictions for user-product pairs where the similarity models had too little data and fell back to the overall average.

| Model (tuned) | RMSE | Precision@10 | Recall@10 | F1 |
|---|---|---|---|---|
| User-user KNN | 0.963 | 0.850 | 0.809 | 0.829 |
| Item-item KNN | 0.970 | 0.834 | 0.799 | 0.816 |
| **SVD** | **0.906** | **0.860** | **0.814** | **0.836** |

## Takeaway

SVD is the strongest single model. A hybrid that combines SVD with similarity-based models could improve recommendations further for users and products with little rating history.

---
