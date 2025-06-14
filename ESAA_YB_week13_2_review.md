# 2025.06.16

🔗 [https://www.kaggle.com/code/ambrosm/pss4e5-eda-which-makes-sense#Flood-prediction:-EDA-which-makes-sense](https://www.kaggle.com/code/itasps/0-96218-logistic-regression-plus-ensemble)

## 주제

- To predict rainfall for each day of the year (Classifcation)

## 데이터

**(1) train**

- day, pressure, maxtemp, temperature, mintemp, dewpoint, humidity, cloud, sunshine, winddirection, windspeed (feature) , rainfall(target, binary)

**(2) test**

- day, pressure, maxtemp, temperature, mintemp, dewpoint, humidity, cloud, sunshine, winddirection, windspeed (feature)

## 코드 리뷰

### (1) EDA

- Target / Feature distributions
- Null 값 처리(winddirection, windspeed) → mean
- Class imbalance → Class weight
- train/test split

### **(2) Modeling**

- Logistic Regression (solver, penalty 등 hyperparameter 조정)

### (4) Evaluation

- accuracy

## 차별점 및 배울점

- 해당 코드에서 null 값을 먼저 파악하고 해당 값의 특성에 맞춰 mean 값으로 결측치를 처리한 것이 인상 깊었다.
- target의 분포를 확인한 후 불균형할 때는 보통 log를 자주 사용했는데 여기서는 class weight를 이용해 불균형을 해소한 부분이 인상 깊었다.
