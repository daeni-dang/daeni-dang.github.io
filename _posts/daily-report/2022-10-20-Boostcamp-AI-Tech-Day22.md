---
title: "Boostcamp AI Tech - Day 22"
categories:
  - daily-report
tags:
  - GitHub
toc: true
toc_sticky: true
---

## 추천 시스템 Basic

## 1. 오늘 배운 내용
- 깃헙 특강 Part 3
	- [.gitignore 파일 자동 생성](https://www.toptal.com/developers/gitignore)
	- ```git pull``` = ```git fetch``` + ```git merge```
	- ```git branch```
		- [git flow](https://techblog.woowahan.com/2553/) / github flow
	-  ```git tag```
		- 움직이지 않는 reference에 이름을 붙임
		- cf) head, branch : 움직이는 reference
	- 로컬 branch push
		- ```git push --set-upstream [branch]```
		- fastforward
			- fastforward를 못하게 merge하려면 ```--no-ff``` 옵션 추가하여 merge
		- 브랜치 삭제
			- ```git branch -d [branch]```
	- pull request
		- branch를 master로 합쳐달라고 요청을 보내는 것
	- ```cherry-pick```
		- 부분 병합
	- ```rebase```
	- ```revert```

## 2. 과제 수행
- (기본-3) FM + FFM
	1. FM 구현
		- FMLayer의 pairwise interetion은 아래와 같다.
		- ![image](../../assets/img/fmlayer.png)
		- 따라서 아래 수식이 FMLayer임을 알 수 있다.
	$$\mathrm{FMLayer}\left( \mathrm{x} \right) = \frac{1}{2} \sum_{f=1}^{k} \left[ \left( \sum_{i=1}^{n} v_{i,f} x_i \right)^2 - \sum_{i=1}^{n} v_{i,f}^2 x_i^2 \right]$$
		- Factorization Machine은 Linear + FMLayer이므로 아래와 같다.
$$\hat{y}(\mathrm{x}) = w_0 + \sum_{i=1}^{n}{\mathrm{w}_i x_i} + \mathrm{FMLayer}\left( \mathrm{x} \right) \\ \, = \mathrm{Linear}\left( \mathrm{x} \right) + \mathrm{FMLayer}\left( \mathrm{x} \right)$$
		2. FFM	$$ \mathrm{FFMLayer} \left( \mathrm{x} \right) = \sum_{i=1}^{n} \sum_{j=i+1}^{n}{\left \langle \mathrm{v}_{i,f_j} \, , \mathrm{v}_{j,f_i} \right \rangle x_i x_j} \\ = \sum_{i=1}^{n} \sum_{j=i+1}^{n}{\left \langle x_i \mathrm{v}_{i,f_j} \, , x_j \mathrm{v}_{j,f_i} \right \rangle}$$
## 3. 더 공부할 내용
- MLE
- Transformer
- MF, ALS

## 4. 출처
- [fmlayer image](https://d2l.ai/chapter_recommender-systems/fm.html)