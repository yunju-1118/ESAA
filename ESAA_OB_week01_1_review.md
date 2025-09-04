https://www.notion.so/2025-09-04-264dcd5c0b6e8032978ceac7a56d003f

# 2025.09.04

🔗 [https://www.kaggle.com/code/allunia/e-commerce-sales-forecast#Focus-on-daily-product-sales-](https://www.kaggle.com/code/allunia/e-commerce-sales-forecast#Focus-on-daily-product-sales-)

## 주제

- To predict E-commerce Sales (Regression)

## 데이터

**(1) train**

- InvoiceNo, StockCode, Description, InvoiceDate, UnitPrice, CustomerID, Country (feature), Quantity(target)

**(2) test**

- InvoiceNo, StockCode, Description, InvoiceDate, UnitPrice, CustomerID, Country (feature)

## 코드 리뷰

### (1) EDA

- Missing descriptions, Hidden Missing descriptions (“nan” strings, “” empty strings)
- 파생변수 생성 (Revenue, Date)
- Log transformation

### **(2) Modeling**

- Hyperparameter Class
- Catmodel class
- Hyperparameter - Search class
- Time series validation Catfamily

### (4) Evaluation

- R2_score
- Plot_importances

## 차별점 및 배울점

- Null값의 여부를 판별할 수 있는 Descriptions라는 열을 추가해 null 값을 구분한 점이 흥미로웠다.
- 예측 모델링을 위한 Feature Engineering을 통해 필요한 파생변수를 만든 점이 흥미롭다.
