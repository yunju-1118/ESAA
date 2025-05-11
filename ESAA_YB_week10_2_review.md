https://www.notion.so/2025-05-09-1f0dcd5c0b6e8008a134fca72f7feac7?pvs=4

# 2025.05.09

🔗 [https://www.kaggle.com/code/ambrosm/pss4e5-eda-which-makes-sense#Flood-prediction:-EDA-which-makes-sense](https://www.kaggle.com/code/ambrosm/pss4e5-eda-which-makes-sense#Flood-prediction:-EDA-which-makes-sense)

## 주제

- 홍수 발생 확률 예측을 위한 회귀 모델 개발

## 데이터

**(1) train**

- RiverManageMent, ClimateChange, DamsQuality 등 홍수 발생에 영향을 미칠 수 있는 다양한 합성 데이터 (feature) 및 FloodProbability (target)

**(2) test**

- RiverManageMent, ClimateChange, DamsQuality 등 홍수 발생에 영향을 미칠 수 있는 다양한 합성 데이터

## 코드 리뷰

### (1) EDA

- Target / Feature distributions
- Correlation (No correlation among the features, but all features are correlated with the target)

### **(2) Dimensionality Reduction**

- PCA, UMAP, t-SNE

### **(3) Modeling**

- **Cross-validation** → **Linear models** (linearRegression, Ridge)
- **Tree-based models** (XGBRegressor, CatBoost, LightGBM)

### (4) Evaluation

- r2_score 이용

## 차별점 및 배울점

- 고차원 데이터에 **Dimensionality Reduction**을 적용하여 어떤 구조를 가지는지 시각적으로 파악하였음.
- Target이 불균형 하므로 **Startified k-fold**를 이용해 각 폴드에서 클래스의 비율을 유지함.
- 모든 피처에서의 영향을 파악하고, 안정적인 모델을 추정하기 위해 **Ridge**를 사용하였음.

## **느낀점**

- 아직 차원 축소에 대해 제대로 배우지 않아 차원 축소에 대해 공부한 뒤, 다시 코드를 공부해보고 싶다는 생각이 들었다. 또한, EDA 과정에서 평소에 자주 사용하던 info나 describe를 이용해서 한 것이 아닌 target 변수와의 관계를 위주로 코딩한 것과 Dimensionality Reduction을 EDA 과정 중의 일부로 사용한 것이 인상 깊었다. 또한 ‘Advanced models with feature engineering’ 부분에 대해서는 아직 학습하지 못하였는데 조금 더 공부를 해서 실력을 기른 뒤 해당 부분에 대해 학습해 볼 것이다.
