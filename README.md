# TenderHack
Predict of recession and participant amount of quotation session
## Task
Development of a predictive system for analyzing key metrics of quotation sessions on the Supplier Portal
## Input Data
- Discription of quotation session 
- Caterogry of product
- Region of product
- Base cost
- Final cost
- Data
- inn
## Solve
1. Prepare data and create A LOT OF features
2. Get clusters from discription of quotation sessions by compression UMAP and clustering by HDBSCAN
3. Fit CatBoostClassifier to predict status of session - very important feature
4. Add the cluster feature to main dataset
5. Fit two CatBoostRegression to predict two main targets - recession and participant of quotation session
## Metrics
- I use ROC-AUC and PR-AUC for predict cluster (ROC-AUC = 0.85, PR-AUC = 0.62)
- I use MAE for predict recession and participant of quotation session (MAE = 25.46 on recession and MAE = 2.16 on participant of quotation session)

