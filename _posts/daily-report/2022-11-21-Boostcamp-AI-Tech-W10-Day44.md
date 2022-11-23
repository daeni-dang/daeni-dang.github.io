---
title: "Boostcamp AI Tech - W10 Day 44"
categories:
  - daily-report
tags:
  - DKT
toc: true
toc_sticky: true
---

## DKT

## 1. 오늘 배운 내용

### 대회
- lstmattn에 kfold를 적용해봤다.
  - dkt에 lstm, lstmattn, bert 세 개가 있었는데 가장 성능이 좋았던 lstmattn에 적용.
  - 유저별로 train, validation을 split했다.
  - **결과 :** 0.01 정도의 성능 개선이 있었다. 왜?
  - 하이퍼파라미터를 잘 설정하니 0.7657까지 나옴.
  - lightgcn 최고 성능과 앙상블해서 0.7934 당시 3등.
- feature engineering 해서 lstmattn에 적용해보려 했는데 베이스라인 코드를 너무 많이 수정해야 함. 
  - dkt를 버린다? -> 나는 버리는 게 맞다고 생각함.

### 앞으로 계획
- lightGCN에 kfold를 적용해보자.
- feature engineering을 통해 feature 개수를 늘린 다음 catboost를 적용해보자.



## 2. 피어세션
- 깃허브 브랜치 방식 논의 -> 개인 브랜치 생성 그 안에서 실험 후 main에 merge
- 컨벤션 논의 -> 노션에 정리
- gitignore 파일 생성