---
title: "Loss Function(손실 함수)"
categories:
  - til
toc: true
toc_sticky: true
---

## 1. Loss Function(손실 함수)란?
손실 함수란 입력 값이 들어와 모델을 통해 얻은 예측 값이 실제 값과 차이를 판단하는 기준입니다. 예측 값과 실제 값의 차이를 loss라고 합니다. 이 loss 값을 줄이는 방향으로 weight를 업데이트시키게 됩니다.


## 2. Loss function의 종류
지도 학습에는 분류(classification), 회귀(regression) 두 가지가 있는데, 이에 따라 손실 함수도 두 가지로 나누어집니다. 

### 2.1 regression type
회귀에 사용되는 손실 함수에는 MAE, MSE, RMSE가 있습니다.
#### 2.1.1 Mean Absolute Error(MAE)
먼저 Mean Absolute Error입니다. 이름에서 알 수 있듯이, MAE는 오차(정답 값과 예측 값의 차이)의 절댓값을 모두 더한 뒤 평균을 낸 값입니다. 이를 수식으로 나타내면 아래와 같습니다.

$$ MAE=\dfrac{1}{N}\sum ^{n}_{i=1}\left| \hat{y}_{i}-y_{i}\right| $$

이제 MAE의 특징을 알아보겠습니다.
- MAE는 이상값(outlier)의 영향을 크게 받지 않습니다. 즉, 이상값에 강인(robust)합니다.
- 또한, 모든 오차에 동일한 가중치를 부여합니다.
- MAE는 최솟값이 뾰족한 점이어서 이곳에서는 미분이 불가능하다는 특징이 있습니다.

![image](https://miro.medium.com/max/640/1*2vVfKyVjGe6G-cLDcfy03A.png)


#### 2.1.2 Mean Squared Error(MSE)
다음은 Mean squared error입니다. MSE는 오차의 제곱값을 모두 더한 뒤 평균을 낸 값입니다. 이를 수식으로 나타내면 아래와 같습니다.

$$ MSE=\dfrac{1}{N}\sum ^{n}_{i=1}\left( \hat{y}_{i}-y_{i}\right)^{2} $$

이제 MSE의 특징을 알아보겠습니다. 
- MSE는 오차에 제곱을 취하기 때문에 이상값(outlier)에 민감하게 반응합니다. 따라서 정답값과 예측값의 차이가 크다면 오차값이 더 크게 반영이 됩니다.
- 또한, 제곱을 취하기에 오차가 0과 1 사이인 경우, 오차가 더 작게 반영이 되고, 1보다 클 때는 더 크게 반영이 된다는 특징을 가지고 있습니다. 이로 인해 값의 왜곡이 일어날 수 있습니다.
- MSE는 이차함수이기 때문에 뾰족한 점이 없어 모든 함수값이 미분 가능하다는 특징도 가지고 있습니다.
 
![image](https://miro.medium.com/max/640/1*i5VaXBlH7dNuHp-qPwFXnw.png)

#### 2.1.2 Root Mean Squared Error(RMSE)
다음은 Root Mean Squared Error입니다. RMSE는 MSE에 제곱근을 씌운 값입니다. 이를 수식으로 나타내면 아래와 같습니다.

$$  MAE=\sqrt{\dfrac{1}{N}\sum ^{n}_{i=1}\left( \hat{y}_{i}-y_{i}\right)^{2}}  $$

RMSE의 특징은 다음과 같습니다.
- RMSE는 제곱근을 취해 MSE의 단점을 어느정도 해소할 수 있습니다.
- RMSE는 이상값에 대한 민감도가 MAE와 MSE의 사이에 있습니다.
- RMSE는 MSE에 제곱근을 취하기 때문에 뾰족한 점이 생겨 미분이 불가능한 지점이 있습니다.

![image](https://miro.medium.com/max/640/1*JrhjZDbK5g34a28-oZ_igg.png)

## 참고 자료
[# [ML101] #3. Loss Function](https://brunch.co.kr/@mnc/9)<br>
[# 언제 MSE, MAE, RMSE를 사용하는가?](https://jysden.medium.com/%EC%96%B8%EC%A0%9C-mse-mae-rmse%EB%A5%BC-%EC%82%AC%EC%9A%A9%ED%95%98%EB%8A%94%EA%B0%80-c473bd831c62)
