---
title: "Boostcamp AI Tech - Day 19"
categories:
  - daily-report
tags:
  - Recommend system
toc: true
toc_sticky: true
---

## 추천 시스템 Basic

## 1. 오늘 배운 내용
- Graph Neural Network
  - 그래프 데이터에 적용 가능한 신경망
  -  naive approach : 그래프 및 feature data를 인접 행렬로 변환
  - Graph Convolution Network (GCN)
	  - local connectivity, shared weights, multi-layer를 이용해 convolution 연산
	  - 간접 관계 특징까지 추출 가능
- Neural Graph Collaborative Filtering (NGCF)
	- user-item 상호작용이 embedding에서부터 학습될 수 있도록 접근
	- GNN을 통해 경로가 1보다 큰 연결을 임베딩한다.
- LightGCN
	- NGCF에 비해 파라미터와 연산량 감소(가중합)
	- 레이어 깊어질수록 임베딩 시그널이 약해짐
- GRU4Rec
	- session을 병렬적으로 구성하여 mini-batch 학습


## 2. 피어세션
-   질문
	 1. FFM의 필드 구성 중 Numerical Feature에서 discretize
		- n개의 구간으로 나누는데, 이 n은 어떻게 설정하는 것인가?
	2. GRU4Rec 중 Session Parallel Mini batches 부분
- 멘토링 수요일(10/19) 오후 6시

## 3. 회고
- 강의를 들으며 이해가 잘 되지 않은 부분을 피어세션을 통해 놓친 부분까지 이해할 수 있었다.

## 3. 더 공부할 내용
- MLE
- Transformer
- MF, ALS