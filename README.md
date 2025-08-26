# stroke_prediction
Machine learning models to predict stroke risk using patient demographic and clinical data.


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

##  Results
- ROC-AUC: XX (추가 예정)
- 주요 변수: 나이, 혈당, 흡연 여부 등
- 샘플 그래프: (추후 업로드)
![ROC Curve](figures/roc_rf.png)

## 💡 Next Steps
- ECG 데이터 분석 프로젝트 확장
- 전자의무기록(EMR) 데이터 마이닝 적용
