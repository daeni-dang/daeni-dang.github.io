---
title: "Transfer Learning"
categories:
  - Boostcamp AI Tech
tags:
  - pytorch
toc: true
toc_sticky: true
---

## 1. Transfer Learning(전이학습)이란?
전이 학습이란 무엇일까요? ```전이```라는 말에서 풍기듯이, 다른 곳에 영향을 미칠 것 같습니다. 전이 학습의 정의를 찾아봤습니다.
>Transfer learning (TL) is a research problem in machine learning (ML) that focuses on storing knowledge gained while solving one problem and applying it to a different but related problem.

[위키 백과 - Transfer learning](https://en.wikipedia.org/wiki/Transfer_learning)

위의 정의를 정리하면 어떤 문제를 해결하면서 얻은 지식을 바탕으로 관련된 문제에 적용한다는 것입니다. 이미 어떤 지식을 가지고 있는 모델을 ```pretrained model```이라고 합니다. ```pretrained model```을 이용해 현재 문제 상황에 맞게 가중치를 변경하여 사용합니다.

## 2. 전이 학습이 왜 필요할까?
전이학습이 어떤 것인지는 알았습니다! 하지만 이런 방법이 왜 필요한 것일까요?

딥러닝 모델을 제대로 훈련시키기 위해서는 데이터가 아주 많이 필요합니다. 하지만 이렇게 많은 데이터를 얻는 것은 어려운 일입니다.

이런 문제점을 해결하기 위한 것이 바로 **전이학습**입니다!!

즉, 전이학습이란 이미 많은 데이터를 가지고 학습된 모델의 지식(가중치)을 가지고와서, 우리가 지금 만든 모델에 적용하는 것입니다. 물론 어떤 조정 과정은 필요하겠지요. 이를 통해 우리의 적은 수의 데이터를 가진 모델로도 더 빠르게 비교적 높은 정확도를 지닌 모델을 만들 수 있습니다.

이렇게 전이학습은 더 빠른 시간 안에 더 높은 정확도를 가진 모델을 만들 수 있습니다.

## 참고 자료
- [[딥러닝 알아가기] Transfer Learning과 Fine Tuning](https://newindow.tistory.com/254)
- [전이학습(Transfer Learning)이란?](https://dacon.io/forum/405988)