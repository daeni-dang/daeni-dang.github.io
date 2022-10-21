---
title: "Boostcamp AI Tech - Day 23"
categories:
  - daily-report
tags:
  - RecSys
toc: true
toc_sticky: true
---

## 추천 시스템 Basic

## 1. 오늘 배운 내용
- Deep Interest Network (DIN)
	- Embedding & MLP 방식으로는 사용자의 다양한 관심사를 반영할 수 없다.
	- -> 사용자가 과거에 소비한 아이템 리스트를 `user behavior feature`로 만듦.
	- 모델 구성
		1. Embedding layer
		2. Local Activation Layer
			- user behavior feature(소비자가 과거에 소비한 아이템 리스트)와 현재 예측하려는 아이템의 관련성을 학습
		3. Fully-connected Layer
- Behavior Sequence Transformer (BST)
	- Transformer 구조를 CTR 예측에 적용
	- ![image](../../assets/img/din.png)
		- Embedding layer, Transformer layer, MLP layer로 구성.
		- User behavior sequence를 입력으로 사용
		- Transformer layer에서 encoder 부분만 사용
		- transformer encoder layer를 n개 쌓아서 정확도 높이기를 시도함. (하지만 best는 1개)
		- 아이템을 소비한 물리적 시간의 차이를 사용함.(custom positional encoding)

## 2. 피어세션
- 논문 리뷰 하기로 결정하였다.

## 3. 더 공부할 내용
- MLE
- Transformer
- MF, ALS

## 4. 출처
- DIN image - "behavior sequence transformer for e-commerce recommendation" 논문