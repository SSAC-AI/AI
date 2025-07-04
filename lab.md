# 🌐 AMCW LiDAR 내부 스트레이 라이트 보정을 위한 딥러닝 연구

이 저장소는 **Helios 2 AMCW LiDAR**를 활용한 **내부 스트레이 라이트(Stray Light)** 보정 연구를 문서화한 프로젝트입니다.  
기존 GMM + PSO 최적화 기반의 보정 방식을 기반으로, 실시간 딥러닝 기반 거리 보정 모델을 구현하는 것을 목표로 합니다.

---

## 📝 참고 논문

**논문명:**  
*Automatic Internal Stray Light Calibration of AMCW Coaxial Scanning LiDAR Using Black and White Image Patterns*  
**저자:** Sung-Hyun Lee, Yoon-Seop Lim, Wook-Hyeon Kwon, Yong-Hwa Park  
**저널:** IEEE Transactions on Instrumentation and Measurement, 2024  
**DOI:** [10.1109/TIM.2023.3343786](https://doi.org/10.1109/TIM.2023.3343786)

---

## 🎯 연구 개요

- 내부 stray light는 **AMCW LiDAR 내부에서 발생하는 다중 반사 신호**로, 거리 왜곡을 유발함
- 기존 논문은 checkerboard 이미지에서 흑백 영역을 GMM으로 분리하고, PSO로 (As, ϕs)를 추정
- 본 프로젝트에서는 이를 **딥러닝으로 대체**하여 실시간 보정이 가능하도록 확장함

---

## 🧠 핵심 개념

| 항목 | 설명 |
|------|------|
| AMCW LiDAR | 정현파 기반의 간접 ToF 방식 |
| Stray Light | 내부 광학계에서 발생하는 정적 간섭 신호 |
| GMM | checkerboard의 밝기 분포를 분류하여 보정 기준 생성 |
| PSO | 깊이 편차를 최소화하는 stray light 파라미터를 최적화 |
| 딥러닝 방식 | 입력(depth, amplitude)을 통해 직접 보정된 depth 추정 |

---

## 🧪 실험 장비 및 환경

| 항목 | 내용 |
|------|------|
| 센서 | Helios 2 (LUCID Vision Labs) |
| 출력 | Depth map, Amplitude map, Confidence map |
| 해상도 | VGA (640x480), 최대 60fps |
| SDK | Arena SDK (Python 또는 C++), GenICam 호환 |

---

## 🧰 데이터 구성 예시
/dataset/
├── raw/
│ ├── scene_001_depth.png
│ ├── scene_001_amplitude.png
│ └── scene_001_confidence.png
├── gt/
│ └── scene_001_corrected_depth.png
- `raw/`: Helios 2에서 얻은 원본 데이터
- `gt/`: PSO 기반 GMM 알고리즘 또는 수동 보정을 통해 생성한 정답 거리맵

---

## 🧠 딥러닝 모델 설계

### 기본 구조 (U-Net 기반)

- 입력: `[depth, amplitude, confidence]` (3채널)
- 출력: `보정된 depth map`
- Loss:  
  - MSE 또는 L1 Loss  
  - Checkerboard 기반 평탄화 Loss (flatness)  
  - (선택) Physically-constrained loss

### 기타 구성

- Residual 방식: 보정값만 예측하여 `corrected = raw + delta`
- Hybrid 방식: (As, ϕs) 추정 후 수식으로 보정 (논문 수식 9 기반)

---

## 🔄 실측 실험 계획

- checkerboard를 다양한 거리(1~4m)에 배치하여 stray light 유도
- 각 거리에서 depth, amplitude, confidence map 저장
- 기존 PSO + GMM 방식으로 정답 보정값 생성
- 이를 기반으로 딥러닝 모델 학습

---

## 🛠 향후 목표

- Helios 2용 데이터 수집 스크립트 제작 (Python + Arena SDK)
- PSO + GMM 보정 알고리즘 Python 포팅
- PyTorch 기반 딥러닝 학습 파이프라인 구성
- 실시간 보정 데모 (OpenCV + PyTorch)

---

## 📂 관련 파일
```
| 파일 | 설명 |
|------|------|
| `model.py` | 딥러닝 보정 네트워크 구조 |
| `train.py` | 학습 루프 |
| `data_loader.py` | 실측 이미지 데이터셋 로딩 |
| `eval_tools.py` | checkerboard 평탄도 평가 도구 |
```

---
