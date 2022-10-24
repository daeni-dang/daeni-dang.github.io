---
title: "추천 시스템의 성능은 어떻게 평가할까?"
categories:
  - til
toc: true
toc_sticky: true
---


## 1. Offline Test vs. Online Test
먼저 offline test와 online test가 무엇인지 알아보도록 하겠습니다.

offline test란 배포 전 이미 구성된 데이터를 바탕으로 성능 지표를 측정하는 평가입니다. 유저로부터 수집한 데이터를 train/valid/test로 나누어 사용하게 됩니다.. 

online test는 모델을 실제 사용자에게 테스트하는 것으로, 새로운 모델(실험군)과 기존의 모델(대조군)의 성능을 비교하여 평가합니다.


## 2. 추천 시스템의 평가 지표
1) Precision@K
	- 추천한 `K`개의 아이템 중 유저가 실제로 관심있는 아이템의 비율
2) Recall@K
	- 관심있는 전체 아이템 중 우리가 추천한 아이템의 비율
3) AP@K (Average Precision@K)
	- `Precision@1`부터 `Precision@K`까지의 평균값
	$$ AP@K=\frac{1}{m}\sum_{i=1}^{K}Precision@i $$
	- 위의 식에서 $m$은 사용자가 반응한 아이템의 개수입니다.
4) MAP@K (Mean Averate Precision@K)
	- AP@K의 평균값
	$$ MAP@K=\frac{1}{|U|}\sum_{u=1}^{|U|}(AP@K)_{u} $$
	- 위의 식에서 $|U|$는 유저 수입니다.
5) NDCG
	- Cumulative Gain
		- 상위 K개 아이템의 관련도를 합한 것
		$$ CG_K=\sum_{i=1}^{K}rel_i $$
		- $rel$은 유저가 아이템을 얼마나 선호하는지 입니다.
	- Discounted Cuvulative Gain
		- 순서에 따라 CG를 discount
		$$ DCG_K=\sum_{i=1}^{K}\frac{rel_i}{log_2(i+1)} $$
	- Ideal DCG
		- 이상적인 경우의 DCG 값
		$$ IDCG=\sum_{i=1}^{K}\frac{rel_i^{opt}}{log_2(i+1)} $$
	- Normalized DCG
		- DCG를 IDCG로 나눈 값
		$$ NDCG=\frac{DCG}{IDCG} $$
6) Hit Rate
	- 전체 사용자 중 추천한 아이템을 선호할 확률
	$$ Hit Rate=\frac{number\; of\; Hit\; User}{number\; of\; User} $$