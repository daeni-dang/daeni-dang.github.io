---
title: "Boostcamp AI Tech - Day 17"
categories:
  - daily-report
tags:
  - RecSys
toc: true
toc_sticky: true
---

## 추천 시스템 Basic

## 1. 오늘 배운 내용
- Word2Vec
  - embedding
    - 주어진 데이터를 낮은 차원의 벡터로 표현하는 방법이다.
    1. sparse representation
      - 이진값으로 이루어진 벡터로 표현하는 방법이다.
    2. dense representation
      - 실수값으로 이루어진 벡터로 표현하는 방법이다.
  - word embedding
    - 단어를 벡터로 표현하는 방법이다.
    - 단어 간 유사도를 구할 수 있다.
  - Word2Vec 학습 방법
    1. CBOW
      - 주변의 단어로 가운데 단어를 예측하는 방법
    2. Skip-Gram
      - CBOW의 입력층과 출력층이 반대로 구성
    3. Skip-Gram with Negative Sampling (SGNS)
      - 입력과 레이블 데이터를 둘 다 입력으로 하여 새로운 레이블을 매김.
      - 문장에 없던 새로운 단어를 추가하여 레이블을 0(negative)로 매김.
- Item2Vec
  - 단어가 아닌 추천 아이템을 임베딩
  - 소비한 아이템 리스트가 문장, 아이템이 단어로 가정
- Approximate Nearest Neighbor (ANN)


## 2. 더 공부할 내용
- MLE
- Transformer
- MF, ALS