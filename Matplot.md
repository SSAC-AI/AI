# 📊 Matplotlib 기초 학습 레포트

## 🧾 목차
1. [Matplotlib이란?](#1-matplotlib이란)
2. [Matplotlib 설치](#2-matplotlib-설치)
3. [기본 차트 사용법](#3-기본-사용법)
4. [그래프 종류](#4-그래프-종류)
5. [그래프 커스터마이징](#5-그래프-커스터마이징)
6. [다중 플롯(subplot)](#6-다중-플롯subplot)
7. [플롯 레이블 글꼴 설정](#7-플롯 레이블 글꼴-설정)
8. [마무리 및 참고자료](#9-마무리-및-참고자료)

---

## 1. Matplotlib이란?

Matplotlib은 파이썬에서 **데이터 시각화를 위한 대표적인 라이브러리**입니다.  
주로 2D 플롯을 그리는 데 사용되며, MATLAB 스타일의 API를 제공합니다.

---

## 2. Matplotlib 설치

```bash
pip install matplotlib
```

## 3. 기본 차트 사용법

Matplotlib을 사용하려면 `matplotlib.pyplot` 모듈을 불러와야 합니다.  
아래 예제는 기본 선 그래프를 그리는 방법입니다.
```
import matplotlib.pyplot as plt
import numpy as np

xpoints = np.array([1, 8])
ypoints = np.array([3, 10])

plt.plot(xpoints, ypoints)
plt.show()
```

## 4. 그래프 종류
그래프의 종류는 매우 다양합니다.
아래는 막대그래프, 히스토그램, 산점도, 파이차트에 대한 예제 입니다.
### 막대그래프(Bar Chart)
```
x = np.array(["A", "B", "C", "D"])
y = np.array([3, 8, 1, 10])

plt.bar(x,y)
plt.show()
```
### 히스토그램(Histogram)
```
x = np.random.normal(170, 10, 250)

plt.hist(x) # 히스토그램 생성
plt.show()
```
### 산점도(Scatter Plot)
```
x = np.array([5,7,8,7,2,17,2,9,4,11,12,9,6])
y = np.array([99,86,87,88,111,86,103,87,94,78,77,85,86])

plt.scatter(x, y)
plt.show()
```
### 파이차트(Pie Chart)
```
y = np.array([35, 25, 25, 15])

plt.pie(y) # 원형 차트 생성
plt.show()
```

## 5. 그래프 커스터 마이징
그래프의 선 색깔, 스타일, 마커, 범례 등을 지정할 수 있습니다.
```
x = [1, 2, 3, 4]
y = [10, 20, 15, 25]

plt.plot(x, y, color='green', linestyle='--', marker='s', label='데이터1')  # 스타일 지정
plt.title("커스터마이징 예제")
plt.xlabel("X축")
plt.ylabel("Y축")
plt.legend()           # 범례 표시
plt.grid(True)         # 그리드 추가
plt.show()
```

### 6. 다중 플롯(subplot)
하나의 창에 여러 그래프를 배치할 수 있습니다.
```
#plot 1:
x = np.array([0, 1, 2, 3])
y = np.array([3, 8, 1, 10])

plt.subplot(1, 2, 1)
plt.plot(x,y)

#plot 2:
x = np.array([0, 1, 2, 3])
y = np.array([10, 20, 30, 40])

plt.subplot(1, 2, 2)
plt.plot(x,y)

plt.show()
```

## 7. 플롯 레이블 글꼴 설정
그래프의 레이블 글꼴을 지정할 수 있습니다.
```
x = np.array([80, 85, 90, 95, 100, 105, 110, 115, 120, 125])
y = np.array([240, 250, 260, 270, 280, 290, 300, 310, 320, 330])

font1 = {'family':'serif','color':'blue','size':20}
font2 = {'family':'serif','color':'darkred','size':15}

plt.title("Sports Watch Data", fontdict = font1)
plt.xlabel("Average Pulse", fontdict = font2)
plt.ylabel("Calorie Burnage", fontdict = font2)

plt.plot(x, y)
plt.show()
```
## 8. 마무리 및 참고자료
Matplotlib은 매우 강력한 시각화 라이브러리로, 다양한 그래프와 커스터마이징 기능을 제공합니다.
처음엔 기본 예제를 따라해보고, 점차 여러 기능을 익혀나가면 데이터 분석에 큰 도움이 됩니다.
### 참고자료
- W3schools
- ChatGPT
