# Stroke Prediction (EDA + Logistic Baseline)
Predicting stroke risk using demographic and clinical data with a logistic regression baseline.

## Overview
- **목표**: 환자의 나이, 성별, 혈당, BMI, 흡연 여부 등 데이터를 기반으로 **뇌졸중 발생 여부를 예측**  
- **사용 기술**: Python, pandas, scikit-learn(Pipeline, ColumnTransformer), matplotlib, Plotly
- **핵심 포인트**: 데이터 전처리, 클래스 불균형 가중치 적용, 베이스라인 모델 구축  

## Dataset
- Kaggle Stroke Prediction Dataset
- 링크: [https://www.kaggle.com/datasets/fedesoriano/stroke-prediction-dataset](https://www.kaggle.com/datasets/fedesoriano/stroke-prediction-dataset)

##  Project Structure
```
stroke-prediction/
├─ notebooks/
│   ├─ 01_eda.ipynb        # 데이터 확인, 전처리, 시각화
│   └─ 02_modeling.ipynb   # 모델 학습 및 평가
├─ figures/                # 그래프 및 결과 이미지
└─ README.md
```
- **Notebooks**:  
  - [01_eda.ipynb](notebooks/01_eda.ipynb)  
  - [02_modeling.ipynb](notebooks/02_modeling.ipynb)

- **Key Figures**:  
  ROC | PR
  --- | ---
  <img src="figures/roc_logit.png" width="400"/> | <img src="figures/pr_logit.png" width="400"/>

- **Confusion Matrix**:  
  <img src="figures/confmat_logit_default.png" width="350"/>  

*(튜닝 임곗값 결과도 기본값과 동일한 분포였음)*

- **Clean Data**: [`data/stroke_clean.csv`](data/stroke_clean.csv)  
  *(원본 데이터: Kaggle Stroke Prediction)*

## Results (Logistic, class_weight=balanced)
- Accuracy **0.738** · Precision **0.134** · Recall **0.800** · F1 **0.230**  
- ROC-AUC **0.839** · PR-AUC **0.259**

**해석**: 불균형 데이터 상황에서도 재현율(Recall) 0.80으로 환자를 놓치지 않는 모델을 구현했지만, 정밀도는 낮음. 향후 RandomForest, XGBoost 등의 기법으로 개선 여지 있음.
