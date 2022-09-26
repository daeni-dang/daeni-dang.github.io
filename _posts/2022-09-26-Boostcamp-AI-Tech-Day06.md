---
title: "Boostcamp AI Tech - Day 06"
categories:
  - Boostcamp AI Tech
tags:
  - pytorch
toc: true
toc_sticky: true
---

## PyTorch

## 1. 오늘 배운 내용

### 1.1 [PyTorch Documentation](https://pytorch.org/docs/stable/index.html)

### 1.2 PyTorch란?
- PyTorch란 Python 기반의 오픈소스 머신러닝 라이브러리이다.

### 1.3 PyTorch의 특징
- ```pythonic```
- ```Define by Run```
- ```GPU support```
- ```Auto grad```



## 2. 과제 수행
- (기본-1) Custom Model 제작
  - [Pytorch Documentation](https://pytorch.org/docs/stable/index.html) 보면서 필요한 기능을 찾기 위한 연습 및 어떤 기능이 있는지 살펴보았다.
  - pytorch를 이용해 기초 실습을 진행하였다.


## 3. Peer Session
- ```leaf tensor``` 질문 (미해결)
- 멘토링 날짜 => 09/28 오후 1시
- pytorch 프로젝트 구조 분석 => 09/30


## 4. 회고
- 질문
  1. torch.normal와 randn과 같이 정규분포에서 랜덤한 숫자를 추출하는 것들에서 추출되는 숫자들이 랜덤한데 평균에 거의 근접하게 출력된다. 이거는 평균에 밀집되어있기 때문인가?
  2. [normal](https://pytorch.org/docs/1.12/generated/torch.normal.html#torch.normal), [randn](https://pytorch.org/docs/1.12/generated/torch.randn.html#torch.randn)
  3. pointwise
  4. torch.angle에서 예시 [torch.angle](https://pytorch.org/docs/1.12/generated/torch.angle.html#torch.angle)
  5. torch.allclose [torch.allclose](https://pytorch.org/docs/1.12/generated/torch.allclose.html#torch.allclose)