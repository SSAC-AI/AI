# 🛰️ AMCW LiDAR 내부 산란광 자동 보정

> IEEE Transactions on Instrumentation and Measurement, Vol. 73, 2024  
> 저자: Sung-Hyun Lee, Yoon-Seop Lim, Wook-Hyeon Kwon, Yong-Hwa Park

## 📋 개요

이 연구는 **AMCW (Amplitude-Modulated Continuous Wave)** 기반의 **coaxial scanning LiDAR**에서 발생하는 **internal stray light**으로 인한 **깊이 오차(depth error)**를 줄이기 위한 **자동 보정(calibration)** 방법을 제안합니다.

이 방법은 **checkerboard 패턴 이미지**와 함께 **Gaussian Mixture Model (GMM)** 및 **Particle Swarm Optimization (PSO)** 알고리즘을 활용하여 별도의 하드웨어 변경 없이 정확한 깊이 측정을 가능하게 합니다.

---

## 📌 핵심 개념

- **Internal Stray Light**: LiDAR 내부 광학 부품에서 반사되어 발생하는 불필요한 빛으로, 깊이 측정에 오류를 유발합니다.
- **AMCW LiDAR**: 사인파 형태의 광 신호를 사용하여 반사된 빛의 위상 차이를 기반으로 거리를 측정하는 방식입니다.
- **GMM**: checkerboard 이미지의 밝고 어두운 부분을 자동으로 분리하기 위한 통계적 군집화 방법입니다.
- **PSO**: internal stray light의 위상과 세기를 최적화하여 깊이 오차를 최소화하는 전역 최적화 기법입니다.

---

## 🧠 알고리즘 요약

1. **데이터 수집**: 다양한 거리에서 checkerboard 이미지를 획득합니다.
2. **이미지 분할**:
   - 각 이미지의 amplitude map을 GMM으로 분석하여 밝은 영역과 어두운 영역으로 분류합니다.
3. **오차(loss) 계산**:
   - 두 영역의 평균 깊이 차이(L1-norm)를 계산하여 손실 함수로 사용합니다.
4. **최적화**:
   - PSO를 통해 stray light의 위상(ϕs)과 세기(As)를 찾습니다.
5. **깊이 보정**:
   - 위에서 찾은 stray light 정보를 기반으로 cross-correlation 값을 보정하고, 새로운 깊이 지도를 생성합니다.

---

## 📊 결과 요약

- 깊이 오차가 수십 cm → **3.2 mm 이하로 감소**
- 다양한 거리(1m~4m)와 복잡한 장면에서도 **일관된 성능 유지**
- **추가 하드웨어 필요 없음**, checkerboard 이미지와 기존 LiDAR만으로 보정 가능

---

## 🧪 실험 정보

- **LiDAR 종류**: AMCW coaxial scanning
- **변조 주파수**: 31.25 MHz
- **이미지 해상도**: 최대 300 × 200 픽셀
- **사용 조건**: 일반 실내 조명(300 lx), QVGA 기준 15 fps

---

## 📁 폴더 구조 예시

```bash
.
├── data/               # checkerboard 및 raw 이미지
├── calibration/        # GMM + PSO 보정 알고리즘
├── correction/         # 깊이 보정 처리 코드
├── results/            # 보정 전/후 비교 이미지
└── README.md           # 요약 파일 (본 문서)
```
