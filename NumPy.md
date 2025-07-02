# 📘 NumPy 기초 학습 레포트

## 🧾 목차
1. [NumPy란?](#1-numpy란)
2. [NumPy 설치](#2-numpy-설치)
3. [ndarray 객체](#3-ndarray-객체)
4. [배열 생성 방법](#4-배열-생성-방법)
5. [배열의 속성](#5-배열의-속성)
6. [배열 연산](#6-배열-연산)
7. [인덱싱과 슬라이싱](#7-인덱싱과-슬라이싱)
8. [브로드캐스팅](#8-브로드캐스팅)
9. [유용한 함수들](#9-유용한-함수들)
10. [마무리 및 참고자료](#10-마무리-및-참고자료)

---

## 1. NumPy란?

NumPy(Numerical Python)는 파이썬에서 **과학 계산을 위한 핵심 라이브러리**입니다.  
고성능 다차원 배열 객체인 `ndarray`를 기반으로 다양한 수치 연산과 선형대수 연산 기능을 제공합니다.

---

## 2. NumPy 설치

```bash
pip install numpy
```
## 3. ndarray 객체

NumPy의 핵심 객체는 **ndarray**입니다. 리스트보다 빠르고 메모리 효율이 높습니다.
```
import numpy as np

a = np.array([1, 2, 3])
print(type(a))  # <class 'numpy.ndarray'>
```

## 4. 배열 생성 방법
```
np.array([1, 2, 3])           # 리스트로부터 생성
np.zeros((2, 3))              # 0으로 채우기
np.ones((2, 3))               # 1로 채우기
np.arange(0, 10, 2)           # 연속된 값
np.linspace(0, 1, 5)          # 구간을 나눠 생성
np.random.rand(2, 3)          # 0~1 난수
```
## 5. 배열의 속성
```
a = np.array([[1, 2, 3], [4, 5, 6]])

a.shape      # (2, 3)
a.ndim       # 2
a.dtype      # dtype('int64')
a.size       # 6
a.itemsize   # 8 (바이트 단위)
```
## 6. 배열 연산
```
a = np.array([1, 2, 3])
b = np.array([4, 5, 6])

a + b        # array([5, 7, 9])
a * b        # array([ 4, 10, 18])
a ** 2       # array([1, 4, 9])
```
## 7. 인덱싱과 슬라이싱
```
a = np.array([[1, 2, 3], [4, 5, 6]])

a[0, 1]      # 2
a[:, 1]      # array([2, 5])
a[1, :]      # array([4, 5, 6])
```
## 8. 브로드캐스팅
```
a = np.array([[1], [2], [3]])  # shape: (3, 1)
b = np.array([10, 20, 30])     # shape: (3,)
a + b
```
## 9. 유용한 함수들
```
np.sort(a)          # 정렬
a.T                 # 전치 (transpose)
np.mean(a)          # 평균
np.std(a)           # 표준편차
np.sum(a)           # 합계
np.dot(a, b)        # 행렬 곱
```
## 10. 마무리 및 참고자료

NumPy는 데이터 분석, 머신러닝, 과학 계산 등 다양한 분야에서 핵심적인 역할을 합니다.
**pandas, scikit-learn, TensorFlow** 등 여러 라이브러리들도 NumPy를 기반으로 동작합니다.
# 🔗 참고자료
- [w3schools] (https://www.w3schools.com/)
- chatGPT
