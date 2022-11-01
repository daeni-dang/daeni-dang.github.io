---
title: "Boostcamp AI Tech - Day 30"
categories:
  - daily-report
tags:
  - RecSys Contest
toc: true
toc_sticky: true
---

## RecSys 기초 대회

## 1. 오늘 배운 내용
- 프로젝트
	- hybrid 방식을 거치고 나면 인덱스가 변경되므로, submission 파일과 맞추기 위해 반환되는 predict을 딕셔너리 형태로 변경하였다.
	- user가 처음 나온 경우와 isbn이 처음 나온 경우를 나누어 처리해야 한다. 
	- user가 처음 나온 경우 -> book data를 통해 IBCF 진행
	- book이 처음 나온 경우 -> user data를 통해 UBCF 진행. 만약 user 정보가 모두 공백이라면 고민 필요.

## 2. 피어세션
- cold start 해결 방법에 대해 논의하였다.
- 결측치를 채워야 하는 이유에 대해 논의하였다.

## 3. 더 공부할 내용
- MLE
- Transformer
- MF, ALS