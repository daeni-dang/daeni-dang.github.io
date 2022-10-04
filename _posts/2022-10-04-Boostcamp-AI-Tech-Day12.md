---
title: "Boostcamp AI Tech - Day 12"
categories:
  - daily-report
tags:
  - DL
toc: true
toc_sticky: true
---

## DL Basic

## 1. 오늘 배운 내용
- 딥러닝의 구성 요소
	1. data
	2. model
	3. [loss function](../_posts/2022-10-04-loss-function.md)
	4. optimization algorithm
- Multi Layer Perceptron(MLP)
- Optimization
	- generalization
		- train 데이터로 학습시킨 모델이 테스트 데이터(새로운 데이터)에 관해서도 잘 동작하도록 하는 것이다.
	 - underfitting & overfitting
	 - cross-validation
		 - train 데이터를 k개의 fold로 나눈 뒤 한 fold만 validation set으로 사용하고 나머지는 training set으로 사용하는 방법이다. 모든 fold에 대해 이를 적용한다.
	 - bias & variance
		 -  ![image](https://nvsyashwanth.github.io/machinelearningmaster/assets/images/bias_variance.jpg)
		<center><small>출처 : https://nvsyashwanth.github.io/machinelearningmaster/bias-variance/</small></center>
	 - Bootstrapping
		 - Bagging & Boosting
			 - ![image](https://res.cloudinary.com/dyd911kmh/image/upload/f_auto,q_auto:best/v1542651255/image_2_pu8tu6.png)
		 <center><small>출처 : https://www.datacamp.com/tutorial/adaboost-classifier-python</small></center>
- Gradient descent method
- Regularization

## 2. 과제 수행
- (기본-1) MLP Assignment
- (기본-2) Optimization Assignment


## 3. Peer Session
- Loss Function 중 MAE와 MSE의 차이에 대해 이야기하였다.


## 4. 더 공부할 내용
- Adam 공부

