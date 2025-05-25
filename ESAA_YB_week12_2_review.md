https://www.notion.so/2025-05-26-1fedcd5c0b6e80c8b27aea003d66aed3

# 2025.05.26

🔗 [https://www.kaggle.com/code/sumelahmad/advanced-eda-ml-predictions](https://www.kaggle.com/code/sumelahmad/advanced-eda-ml-predictions)

## 주제

- Forecasting sticker sales in different countries.

## 데이터

**(1) train**

- id, date, country, store, product (feature) 및 num_sold (target)

**(2) test**

- id, date, country, store, product

## 코드 리뷰

### (1) EDA

- Plot overall sales trends
- one-hot encoding
- 파생 변수 (lag, rolling)
- train, test split

### **(2) Modeling**

- **Cross-validation**
- LightGBM (→Feature Importance)

### (3) Evaluation

- MAE

## 차별점 및 배울점

- 파생변수를 만들어 모델에 반영하는 부분이 인상 깊었다.
- 변수를 만들어 시각화를 통해 데이터를 이해하는 부분이 인상 깊었다.
