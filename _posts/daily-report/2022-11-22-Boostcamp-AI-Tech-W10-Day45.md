---
title: "Boostcamp AI Tech - W10 Day 45"
categories:
  - daily-report
tags:
  - DKT
toc: true
toc_sticky: true
---

## DKT

## 1. 오늘 배운 내용

#### 강의 수강
- Riiid 대회에서 피처를 늘리지 않고 좋은 성능을 낸 사례가 있음
- feature engineering으로 좋은 성능 내려면 40~50개는 만들어야 한다?
- layers, head, embedding dimension, sequence length에 따른 성능 차이
- lay로 하이퍼파라미터 튜닝
- -> dkt 모델에 적용해봤는데, seq_len이 50일 때 가장 좋았다(약 0.76). 40, 60 모두 0.74 정도에 그쳤다. 왜?

#### 대회
- lightGCN에 kfold 해보려고 했으나, edge와 label로 구분되어있고, uid iid?로 나눠져있어서 공부가 조금 필요할 것으로 보임.

#### 앞으로 계획
- 먼저 EDA를 간단히 해보면서 데이터를 정확히 파악하기
- 필요한 feature 엔지니어링 해보기
- lightGCN 공부



## 2. 피어세션
- 깃허브 문제 해결