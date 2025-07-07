# 🧠 머신러닝(Machine Learning) 기초 정리

머신러닝은 명시적인 규칙을 프로그래밍하지 않고, 데이터로부터 학습하여 예측이나 분류를 수행하는 기술입니다.  
이 문서는 머신러닝의 핵심 개념과 주요 알고리즘, 대표 라이브러리 등에 대해 정리합니다.

---

## 📌 머신러닝이란?

- 머신러닝(Machine Learning)은 데이터를 기반으로 패턴을 학습하고, 학습된 모델을 이용해 새로운 데이터에 대한 예측을 수행하는 기술입니다.
- **프로그래밍적 규칙 없이**, 데이터 자체로부터 **경험적으로 학습**합니다.

> **정의 (Tom Mitchell)**  
> "컴퓨터가 경험 E로부터 학습하여 작업 T에 대해 성능 P를 향상시키는 것"

---

## 📂 머신러닝 분류

머신러닝은 크게 다음 세 가지 범주로 나뉩니다.

### 1. 지도학습 (Supervised Learning)

- 입력 데이터와 정답(Label)이 있는 상태에서 학습
- 목표: 새로운 입력에 대해 **정답을 예측**
- 예시:
  - 회귀 (Regression): 가격 예측, 수치 예측
  - 분류 (Classification): 스팸 메일 분류, 질병 진단

### 2. 비지도학습 (Unsupervised Learning)

- 정답(Label) 없이 입력 데이터만으로 **구조나 패턴**을 학습
- 예시:
  - 군집화 (Clustering): 고객 세그먼트 분류
  - 차원 축소 (Dimensionality Reduction): 시각화, 정보 압축

### 3. 강화학습 (Reinforcement Learning)

- **환경과 상호작용**하며 보상(Reward)을 통해 최적의 행동을 학습
- 예시: 게임 에이전트, 로봇 제어, AlphaGo

---

## ⚙️ 머신러닝 일반적인 과정

1. **데이터 수집**  
   → 분석 대상 데이터를 확보

2. **데이터 전처리**  
   → 결측치 처리, 정규화, 특성 추출 등

3. **학습/훈련**  
   → 알고리즘에 데이터를 넣어 모델을 학습

4. **검증 및 테스트**  
   → 과적합 방지를 위해 검증 데이터로 성능 평가

5. **예측 및 배포**  
   → 실데이터에 모델을 적용하여 예측 수행

---

## 📈 대표 알고리즘

### 🎯 지도학습

| 알고리즘 | 설명 |
|----------|------|
| 선형 회귀 (Linear Regression) | 연속적인 값을 예측 |
| 로지스틱 회귀 (Logistic Regression) | 이진/다중 분류 |
| 결정 트리 (Decision Tree) | 조건 분기 기반 예측 |
| 랜덤 포레스트 (Random Forest) | 여러 트리를 결합한 앙상블 |
| SVM (Support Vector Machine) | 최대 마진 분류기 |
| K-NN (K-Nearest Neighbors) | 주변 이웃 기반 분류 |

### 🧩 비지도학습

| 알고리즘 | 설명 |
|----------|------|
| K-평균 군집화 (K-Means) | 데이터를 K개의 클러스터로 분류 |
| PCA (Principal Component Analysis) | 차원 축소 및 시각화 |

---

## 🛠️ 대표 Python 라이브러리

| 라이브러리 | 용도 |
|-----------|------|
| `scikit-learn` | 전통적 머신러닝 모델 및 전처리 |
| `pandas` | 데이터 처리 및 조작 |
| `NumPy` | 수치 연산 |
| `Matplotlib`, `Seaborn` | 시각화 도구 |
| `TensorFlow`, `PyTorch` | 딥러닝 구현 프레임워크 |

---

## 💡 과적합(Overfitting)과 과소적합(Underfitting)

- **과적합**: 학습 데이터에 지나치게 최적화되어 테스트 데이터에서 성능 저하
- **과소적합**: 모델이 너무 단순해 학습 데이터도 제대로 학습하지 못함

### 🔄 해결 방법
- 더 많은 데이터 확보
- 정규화(Regularization)
- 적절한 모델 선택
- 교차 검증(Cross Validation) 사용

---

## 🧪 교차 검증(Cross Validation)

- 데이터를 여러 부분으로 나눈 후 번갈아가며 훈련/검증을 수행
- 일반적으로 K-Fold Cross Validation을 많이 사용

---

## 📚 참고 자료

- [Scikit-learn 공식 문서](https://scikit-learn.org/)
- [Machine Learning by Andrew Ng (Coursera)](https://www.coursera.org/learn/machine-learning)
- [Hands-On Machine Learning with Scikit-Learn, Keras, and TensorFlow](https://www.oreilly.com/library/view/hands-on-machine-learning/9781492032632/)

---

📌 **추가 팁**  
- 머신러닝은 수학(선형대수, 통계)과 프로그래밍(Python)의 기초가 중요합니다.  
- 간단한 프로젝트부터 시작해보세요! 예: 타이타닉 생존자 예측, 손글씨 숫자 분류 등

---

📝 작성자: [감영반]  
📅 작성일: 2025-07-07
