# 📊 Matplotlib 기초 학습 레포트

## 🧾 목차
1. [Matplotlib이란?](#1-matplotlib이란)
2. [Matplotlib 설치](#2-matplotlib-설치)
3. [기본 차트 사용법](#3-기본-사용법)
4. [그래프 종류](#4-그래프-종류)
5. [그래프 커스터마이징](#5-그래프-커스터마이징)
6. [다중 플롯(subplot)](#6-다중-플롯subplot)
7. [한글 폰트 설정](#7-한글-폰트-설정)
8. [실습 예제](#8-실습-예제)
9. [마무리 및 참고자료](#9-마무리-및-참고자료)

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
```
import matplotlib.pyplot as plt

x = [1, 2, 3, 4]
y = [10, 20, 25, 30]

plt.plot(x, y)
plt.title("기본 선 그래프")
plt.xlabel("X축")
plt.ylabel("Y축")
plt.show()
```
