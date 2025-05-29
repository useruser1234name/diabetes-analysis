
---

## 분석 목표

- 당화혈색소 수치(`glyhb`) 기준으로 당뇨병 여부 이진 분류
- 머신러닝 모델 성능 비교 (Random Forest vs Logistic Regression)
- KMeans 클러스터링을 통한 고위험군 자동 분류
- 주요 변수(BMI, 나이, 혈당)의 영향력 비교 및 시각적 해석
- 자동 리포트 생성을 통해 비전문가에게도 이해 가능한 결과 제공

---

## 사용 기술

- Python (pandas, numpy, scikit-learn, matplotlib, seaborn, plotly)
- Jupyter Notebook
- Streamlit (대시보드 버전에서 사용 가능)
- KMeans Clustering, RandomForest, LogisticRegression

---

## 주요 분석 흐름

1. **데이터 전처리 및 BMI 계산**
2. **당뇨병 여부(GlyHb > 6.5) 이진 분류**
3. **모델 학습 및 ROC/AUC 기반 성능 비교**
4. **변수 중요도 시각화**
5. **KMeans 클러스터링으로 위험군 분류**
6. **위험군별 평균 특성 자동 해석 리포트 생성**

---

## 클러스터링 결과 요약

| 클러스터 | 평균 혈당 | 평균 나이 | 평균 BMI | 당뇨율 | 해석 |
|----------|-----------|-----------|-----------|--------|--------|
| Cluster 0 | 6.5       | 50.9세    | 35.5      | 32.2%  | 고위험군 |
| Cluster 2 | 5.3       | 46.3세    | 24.2      | 9.1%   | 중간 위험 |
| Cluster 1 | 5.1       | 43.4세    | 26.7      | 9.4%   | 저위험군 |

---

## 결과 시각화

- ROC Curve (모델 비교)
- Feature Importance Bar Chart
- Age vs GlyHb 클러스터링 시각화 (Plotly)
- 자동 위험군 해석 리포트 (텍스트)

---

## 결론 요약

- `glyhb`(혈당 수치)는 분류와 클러스터링에서 가장 영향력이 큰 변수로 확인
- BMI와 나이도 보조 지표로 작용하지만, **혈당 중심의 위험 분류**가 핵심
- 머신러닝 + 클러스터링 기반 자동화 분석은 **비전문가 대상 리포트 제공에도 유용**

---

## 향후 발전 방향

- Streamlit을 통한 웹 기반 대시보드 배포
- 실제 의료기관용 환자 모니터링 툴로 확장
- 더 다양한 분류 알고리즘 도입 (XGBoost, LightGBM 등)

---

## 작성자

-  [류양환]
-  kci01184@naver.com
