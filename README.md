## Raiffeisen Hackathon for DS
### Dataset 
The dataset is available via [link](https://drive.google.com/drive/folders/1vPOy8de3iRw70TKu9BRycdJloyKye_v4?usp=sharing)
### Preprocessing 
- Target Encoding for columns 'region' and 'osm_city_nearest_name' as there are huge variety of values in these columns and One-Hot-Encoding would inflate the dataset 
- Filling in missing values by values' median grouped by 'city'
- 'Floor' column was preprocessed by hand ('str' values were replaced by 'int', specific values - by special class '9999')
- 'City' column was lemmatized using WordNetLemmatizer to bring city names to one standard
- Other categorical columns were preprocessed with One-Hot-Encoding
- Numeric columns were normalized using StandardScaler
### Model 
**Auto ML:** <br>
- estimator_list: LightGBM, XGBoost, Catboost, RandomForest
### Results 
The best model - LightGBM <br>
Custom metric = 0.023312913617357624<br>
MAPE =  0.04459696339846211<br>
RMSE = 0.710851683628062<br>
### Leaderboard
Custom metric on private dataset = 1.2<br>
Top-10% 
