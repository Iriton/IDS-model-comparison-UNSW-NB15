# Intrusion Detection System (IDS) Model Evaluation using UNSW-NB15 Dataset

본 프로젝트는 UNSW-NB15 침입 탐지 데이터를 활용하여 다양한 머신러닝/딥러닝 모델의 성능을 비교하고, 전처리 및 오버샘플링 기법(SMOTE), 하이퍼파라미터 튜닝을 통해 최적의 모델을 도출한 실험 결과를 담고 있습니다.

---

## 프로젝트 개요

- **데이터셋**: [UNSW-NB15 Dataset](https://research.unsw.edu.au/projects/unsw-nb15-dataset)
- **주요 목표**: 침입 탐지 시스템(IDS)을 위한 상황별 최적 모델 도출
- **비교 모델**:
  - 머신러닝: Random Forest, Extra Trees
  - 딥러닝: LSTM, GRU
- **기법**:
  - 데이터 전처리
  - 특성 추출
  - SMOTE (Synthetic Minority Over-sampling Technique)
  - 하이퍼파라미터 튜닝 (Random Search)

---

## 실험 구성 및 코드 파일

| 실험 버전 | 구성 | 코드 파일명 |
|-----------|------|-------------|
| V1 | 전처리만 적용 | `v1_preprocessing.ipynb` |
| V2 | 전처리 + 특성 추출 | `v2_feature_extraction.ipynb` |
| V3 | 전처리 + SMOTE | `v3_smote.ipynb` |
| V4 | 전처리 + 특성 추출 + SMOTE | `v4_feature_smote.ipynb` |

---

## 결론 요약

| 평가 요소 | 추천 모델 | 설명 |
|-----------|-----------|------|
| **실시간 탐지 능력** | Random Forest, Decision Tree | 빠른 예측 속도 |
| **정확성** | XGBoost, Random Forest | 높은 정확도 |
| **적응성과 확장성** | XGBoost | 튜닝으로 성능 향상 |
| **학습 효율** | Extra Trees | 빠른 학습 |
| **클래스 불균형 대응** | XGBoost, CNN | 우수한 성능 |
| **다양한 공격 유형 탐지** | CNN, GRU | 딥러닝의 강점 |

---

## 주요 특징

- 전처리 및 데이터셋 특성 반영
- 다양한 모델 비교 (Decision Tree, Random Forest, Extra Trees, XGBoost, LSTM, GRU, CNN)
- 상황 기반 최적 모델 도출

---

## 향후 과제

- 딥러닝 모델 최적화를 위한 추가 연구
- AutoML 도입 및 파이프라인 자동화
- 최신 IDS 데이터셋에 대한 적용 테스트

---

## 폴더 구조
자세한 내용은 개인 보고서 및 발표 PPT를 통해 보실 수 있습니다.

IDS-model-comparison-UNSW-NB15
├── README.md                      - 프로젝트 설명
│
├── notebooks/                     - 실험별 Jupyter Notebook 모음
│   ├── v1_preprocessing.ipynb              - V1: 전처리만 적용
│   ├── v2_feature_extraction.ipynb         - V2: 전처리 + 특성 추출
│   ├── v3_smote.ipynb                      - V3: 전처리 + SMOTE
│   └── v4_feature_smote.ipynb              - V4: 전처리 + 특성 추출 + SMOTE
│
└── results/                     # 실험 결과 및 평가 자료
    ├── project_ppt.pdf                    - 발표 자료
    └── model_evaluation_report.pdf        - 개인 보고서

