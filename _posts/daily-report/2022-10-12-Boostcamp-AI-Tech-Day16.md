---
title: "Boostcamp AI Tech - Day 16"
categories:
  - daily-report
tags:
  - RecSys
toc: true
toc_sticky: true
---

## 추천 시스템 Basic

## 1. 오늘 배운 내용
- Collaborative Filtering
  - 다수의 의견을 이용해 유저의 관심사를 추천하는 방법.
  - 특정 유저가 특정 아이템에 부여할 평점을 예측하는 것.
- Neighborhood-based CF
  - memory-based
  1. user-based CF (UBCF)
    - 유저 간 유사도를 구해 유사도가 높은 유저들이 선호하는 아이템을 추천해준다.
  2. item-based CF (IBCF)
    - 아이템 간 유사도를 구해 유사도가 높은 아이템 중 선호도가 높은 아이템을 추천해준다.
  - NBCF는 유저/아이템이 많아지면 연산이 늘어나서 성능이 떨어지기도 한다.
- K-Nearest Neighbors CF (KNN CF)
  - 유저와 가장 유사한 K명의 유저를 이용해 평점을 예측한다.
- Model Based Collaborative Filtering (MBCF)
  - 데이터에 숨어 있는 패턴을 이용해 추천한다.
- Singular Value Decomposition (SVD)
  - user와 item으로 구성된 행렬을 right singular vector, right singular vector, singular value로 나누는 것이다.
- Matrix Factorization (MF)
  - user-item 행렬을 user latent factor와 item latent factor 곱으로 분해하는 방법
  - $R$과 $\hat{R}$이 최대한 유사하도록 P(user latent factor)와 Q(item latent factor)를 학습한다.
- Alternating Least Square (ALS)
- Bayesian Personalized Ranking (BPR)  

## 2. Peer Session
- latent vector에 대해 질문


## 4. 더 공부할 내용
- MLE
- Transformer
- MF, ALS