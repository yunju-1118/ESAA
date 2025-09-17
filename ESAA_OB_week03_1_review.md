https://www.notion.so/2025-09-15-271dcd5c0b6e8016a8a0c737f37cf1ba

# 2025.09.15

🔗 [https://www.kaggle.com/code/yannisp/sf-crime-analysis-prediction#Data-Preprocessing](https://www.kaggle.com/code/yannisp/sf-crime-analysis-prediction#Data-Preprocessing)

## 주제

- To predict the category of crime that occurred.

## 데이터

- **Dates** - timestamp of the crime incident (2003/1/1 ~ 2015/5/13)
- **Category** - category of the crime incident (only in train.csv). **This is the target variable you are going to predict.**
- **Descript** - detailed description of the crime incident (only in train.csv)
- **DayOfWeek** - the day of the week
- **PdDistrict** - name of the Police Department District
- **Resolution** - how the crime incident was resolved (only in train.csv)
- **Address** - the approximate street address of the crime incident
- **X** - Longitude
- **Y** - Latitude

## 코드 리뷰

### (1) EDA

- Remove the duplicated data
- 시각화
    - Incident coordinates on a map (GeoDataFrame 이용)
    - Distribution of number of incidents per day
    - Incidents per Weekday
    - Incidents per Crime Category
    - Incidents per Police Districts
    - Geographic Density of Different Crimes
    - Average number of incidents per hour
- 이상치 제거
- 파생변수 생성
    - n_days, Block

### **(2) Modeling**

- label encoding
- train_test split
- LGBMClassifier(objective=’multiclass’)
- Permutation Importances → 피처 중요도 시각화

### (4) Evaluation

- PDP(Partial Dependence Plot) → 피처 중요도 시각화
- SHAP → 모델의 개별 예측 설명
- logloss

## 차별점 및 배울점

- 지난 프로젝트에서 워싱턴의 집 값을 예측해보는 프로젝트를 진행했는데, 그때는 위도와 경도를 어떻게 사용해야 하는지에 대해 어려움이 있었는데 해당 좌표와 geopandas 라는 라이브러리를 통해서 지도 위에 데이터를 시각화 해볼 수 있음을 깨달았다.
- Incidents per Police Distircts에 대한 시각화를 하는 과정에서 우리에게 없는 정보를 외부 URL을 통해 가져와 매핑하여 시각화를 한 점이 인상 깊었다.
