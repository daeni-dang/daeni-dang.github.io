---
title: "Boostcamp AI Tech - Day 20"
categories:
  - daily-report
tags:
  - RecSys
toc: true
toc_sticky: true
---

## 추천 시스템 Basic

## 1. 오늘 배운 내용
- Context-aware Recommendation
	- user-item 상호작용 정보 뿐만 아니라, context 정보도 함께 반영
- Factorization Machine (FM)
$$ \hat{y}(x) = w_0 + \sum_{i=1}^{n}w_ix_i + \sum_{i=1}^{n}\sum_{j=i+1}^{n}<v_i, v_j>x_ix_j $$
	- sparse한 데이터에 대해서도 높은 예측 성능을 보임
	- 많은 수의 데이터에서도 빠르게 학습함
	- 다른 부가 정보들도 모델의 feature로 사용할 수 있음
- Field-aware Factorization Machine (FFM)
	- FM을 발전시킨 모델
	- 3차원으로 확장시킴 (user, item, tag)
	- 입력 변수를 field로 나누어 field별로 다른 latent factor 가짐.
$$ \hat{y}(x) = w_0 + \sum_{i=1}^{n}w_ix_i + \sum_{i=1}^{n}\sum_{j=i+1}^{n}<v_{i, f_j}, v_{j, f_i}>x_ix_j $$
- Gradient Boosting Machine (GBM)
	- loss function이 줄어드는 방향으로 weak learner를 연속적으로 학습하여 결합
- 깃헙 특강 Part 2
	- ```git branch```
	- ```git push```
	- ```git pull```
	- conflict 해결
	- ```add```의 3대 의미
		1. commit 대기 상태로 만들음
		2. untracked -> tracked로 만들음
		3. 충돌 해결했다는 것을 git에게 알려줌
	- ```git reset```
		- HEAD가 가리키는 branch를 옮긴다.
		- ```git reset --hard HEAD@{1}```로도 사용 가능
	- ```git remote```
		- 원격 저장소와 로컬 저장소 연결
	
## 2. 피어세션
-   질문
	 1. 작업을 많이 하다 보면 commit id 중 안 쓰는 것들이 점점 쌓일 것 같은데, 이 부분들은 git이 알아서 관리하는 건가요? → [Garbage collection](https://en.wikipedia.org/wiki/Garbage_collection_(computer_science))가 존재(git gc)

## 3. 회고
- 깃헙 특강을 들으며 브랜치를 여러 번 연습할 수 있었다.

## 4. 더 공부할 내용
- MLE
- Transformer
- MF, ALS