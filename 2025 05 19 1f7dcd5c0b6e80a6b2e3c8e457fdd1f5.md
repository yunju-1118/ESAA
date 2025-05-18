# 2025.05.19

🔗 [https://www.kaggle.com/code/satyaprakashshukl/predict-podcast-listening-time](https://www.kaggle.com/code/satyaprakashshukl/predict-podcast-listening-time)

## 주제

- Your task it to predict listening time of a podcast episode.

## 데이터

**(1) train**

- Genre, Publication_Time, Publication_Day 등 podcast 청취 시간에 영향을 미치는 데이터 (feature) 및 Listening_Time_minutes (target)

**(2) test**

- Genre, Publication_Time, Publication_Day 등 podcast 청취 시간에 영향을 미치는 데이터

## 코드 리뷰

### (1) EDA

- Handling Missing Values (Median, Mode 이용)
- train, test split

### **(2) Modeling**

- **Cross-validation**
- **XGBRegressor**  (→Feature Importance)

### (4) Evaluation

- RMSE
- 그 외 다양한 plot 이용

## 차별점 및 배울점

- Residual plot, actual vs predicted plot 등 결과에 대한 다양한 plot을 그려봄으로써 결과를 나타내는 부분이 좋았다.
- XGBRegressor을 돌리고 있기 때문에 계산에 오랜 시간에 소요될 수 있는데 early_stopping 옵션을 이용하는 부분이 인상 깊었다.
- 결측치를 핸들링하는 부분에서 변수의 특성에 따라 Median, Mode를 사용하는 부분이 좋았다.