---
title: "Boostcamp AI Tech - Day 15"
categories:
  - daily-report
tags:
  - Recommend system
toc: true
toc_sticky: true
---

## 추천 시스템 Basic

## 1. 오늘 배운 내용
- 추천 시스템이란?
  - 사용자는 상품을 `search`한다. 이렇게 사용자가 검색을 하는 것은 직접 결과를 가져오므로 `pull`방식이다.
  - 이렇게 검색하는 것은 사용자가 정확한 의도를 가지고 있고, 높은 연관성을 지닌 결과가 검색된다.
  - `recommend`는 사용자가 어떤 의도를 가진 키워드를 제공하지 않아도 상품을 사용자에게 노출시키는 `push` 방식이다.
  - long-tail recommendation(개인화 추천)
  - 추천을 위해서는 세 가지 데이터가 필요하다.
    1. 유저 관련 정보
    2. 아이템 관련 정보
    3. 유저-아이템 상호작용 정보
      - explicit feedback
        - 사용자가 직접 만족도를 평가한 종류의 피드백
      - implicit feedback
        - 사용자가 아이템을 클릭하거나 구매한 종류의 피드백
  - 사용자에게 추천을 위해서는 유저와 아이템 사이의 상호작용을 평가할 score 값이 필요하다.
    1. 랭킹 : top k개를 추천
    2. 예측 : 아이템의 선호도 정확하게 예측
- 평가 지표
  - offline test
    - 데이터를 train, valid, test로 나누어 모델을 학습시켜 사용자에게 추천한다.
      1. Precision@K
        - 추천한 K개의 아이템 중 실제로 유저가 관심을 가지는 아이템의 비율
      2. Recall@K
        - 유저가 관심있는 전체 아이템 중 추천한 아이템(K개)의 비율
      3. MAP@K
        - AP@K : Precision@1부터 @K까지의 평균값. 높은 순위일수록 점수 상승.
        - MAP@K : 모든 유저에 대한 AP의 평균
      4. NDCG@K
        - 순서에 가중치를 둠
        - DCG를 IDCG로 나눈 값
  - online test
    - 유저가 소비한 데이터가 로그를 통해 데이터에 추가되어 모델이 다시 생성된다.
- 인기도 기반 추천
  1. Most popular
    - 최신성이 중요하다.
    - Hacker news formula
      - gravity 상수를 통해 시간이 지날수록 score가 작아지게 함.
    - Reddit formula
      - 최근 글에 더 높은 점수를 부여함
    - Steam rating formula
      - 전체 리뷰 개수에 따라 값 보정
  2. Highly rated
- 연관 분석
  - 연속된 거래들 사이의 규칙 찾음.
  - {A}->{B}
  - IF (antecedent) THEN (consequent) 
    - 특정 사건이 발생했을 때 함께 자주 발생하는 사건의 규칙
  - 반발 집합(frequent itemset)
    - support count($sigma$)
      - 전체 transaction에서 itemset이 등장하는 횟수
    - support
      - itemset이 전체 transaction에서 등장하는 비율
    - frequent itemset
      - minimum support 값 이상의 itemset
  - 연관 규칙의 척도
    - support : 전체 transaction에 대한 itemset의 확률값
    - confidence : X가 포함된 transaction 중 Y도 포함하는 비율
    - lift : 1보다 클 수 있음. 1이면 X와 Y가 독립. 1보다 크면 양의 상관관계, 1보다 작으면 음의 상관관계.

## 2. Peer Session
- 멘토링 질문에 답을 다는 시간을 가졌다.


## 4. 더 공부할 내용
- MLE
- Transformer