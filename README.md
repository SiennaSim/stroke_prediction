# Stroke Prediction (EDA + Logistic Baseline)


##  Overview
- **목표**: 환자의 나이, 성별, 혈당, BMI, 흡연 여부 등 데이터를 기반으로 뇌졸중 발생 여부를 예측
- **사용 기술**: Python, pandas, scikit-learn, imbalanced-learn, matplotlib
- **핵심 포인트**: 데이터 전처리, 클래스 불균형(SMOTE) 처리, 여러 머신러닝 모델 비교

##  Dataset
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

- **Confusion Matrices**:  
  <img src="figures/confmat_logit_default.png" width="350"/>  
  <img src="figures/confmat_logit_tuned.png" width="350"/>

- **Clean data**: [`data/stroke_clean.csv`](data/stroke_clean.csv)  
  *(원본 데이터: Kaggle Stroke Prediction — 링크만 안내하고 원본 파일은 업로드하지 않음)*

## Results (Logistic, class_weight=balanced)
- Accuracy **0.738** · Precision **0.134** · Recall **0.800** · F1 **0.230**  
- ROC-AUC **0.839** · PR-AUC **0.259**
