---
title: "Boostcamp AI Tech - W9 Day 39"
categories:
  - daily-report
tags:
  - DKT
toc: true
toc_sticky: true
---

## DKT

## 1. 오늘 배운 내용
### DKT란?
DKT란 Deep Knowledge Tracing으로, 딥러닝을 이용해 지식 상태를 추적하는 task이다. DKT는 교육 AI 연구에서 많이 사용되고 있다. DKT는 문제 풀이를 한 정보를 가지고 다음 문제를 맞출지 예측한다. 이런 DKT를 이용하면 다음에 풀 문제를 추천해주거나 얼마나 이해했는지 학생의 이해도를 파악할 수 있다. 또한, DKT는 시퀀스 데이터를 다룬다.


### DKT의 평가 지표
#### Confusion Matrix
DKT에서는 평가 지표로 AUC(Area Under the ROC Curve)를 사용하는데, 이를 이해하기 위해서는 confusion matrix를 알아야 한다. 

![[confusion_matrix.png]]
위 이미지는 binary 상황에서의 confusion matrix이다. 위쪽이 모델이 예측한 값이고, 왼쪽이 실제 값이다. 그럼 `TN`, `FP`, `FN`, `TP`는 각각 무엇일까? 위 그림에서 초록색 부분은 모델이 올바르게 예측한 경우로, `TN`은 `True Negative`이다. 즉, negative를 true하게 예측했다는 의미이다. `TP`는 `True Positive`로, positive를 true하게 예측했다. 반대로 주황색 부분은 잘못 예측한 경우이다. `FN`은 `False Negative`, `FP`는 `False Positive`이다.

이런 값들을 이용해 어떤 정보를 알 수 있을까?
- Accuracy : $\frac{TP+TN}{TP+TN+FP+FN}$ 이는 모든 값 중 옳게 예측한 비율을 나타낸다.
- Specificity : $\frac{TN}{TN+FP}$ 이는 negative임을 옳게 예측한 비율을 나타낸다.
- Recall, Sensitivity, TPR : $\frac{TP}{TP+FN}$ 이는 positive임을 옳게 예측한 비율을 나타낸다.
- Precision, PPV : $\frac{TP}{TP+FP}$ 이는 정답이 positive인 것 중에 맞은 것의 비율을 나타낸다.

여기에서 Recall과 Precision은 trade-off 관계를 가진다. recall은 1로 많이 예측할수록 값이 커지고, precision은 1로 적게 예측할수록 값이 커지기 때문이다. 이러한 점을 반영하여 만든 것이 **F1-score**이다.
$$ F1-score = 2 \times\frac{Recall \times Precision}{Recall + Precision}$$

#### Area Under the ROC Curve (AUC)
AUC는 TPR과 FPR을 이용해 나타낸 그래프이다.
![[auc.png]]
FPR은 실제 0인데 1로 예측한 비율이고, TPR은 실제 1이고 1로 에측한 비율이다. 따라서 0인 지점에서 시작하여 옳게 예측했으면 그래프에서 위로 그려지고, 잘못 예측하면 오른쪽으로 그려지게 된다. 이 AUC는 그래프에서 면적이 커질수록 틀린 부분이 적어지게 된다.

AUC의 범위는 0~1이다. AUC가 0이라면 예측이 모두 잘못되었다는 것이다.

## 2. 피어세션
- level2 팀원들과 첫 피어세션 시간을 가졌다.
- 수요일에 우팀소 발표 준비를 하면서 level3 주제에 대해 논의하였다.


## 3. 더 공부할 내용
- MLE
- Transformer
- MF, ALS

## 4. 참고 자료
- [confusion matrix 이미지](https://pub.towardsai.net/deep-understanding-of-confusion-matrix-6ab1f88a267e)
- [AUC 이미지](https://bioinformaticsandme.tistory.com/328)