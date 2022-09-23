---
title: "Boostcamp AI Tech - Day 04"
categories:
  - Boostcamp AI Tech
tags:
  - ai math
---

## AI Math & Python Basices for AI

- [AI Math](#ai-math)
    - [Statistics](#statistics)
    - [Bayesian rule](#bayesian-rule)
- [일일 회고](#일일-회고)
- [출처](#출처)
<hr><hr>
<br><br>

# AI Math

## Statistics
<hr>

- 모수
    - 모수란 모집단에서 얻을 수 있는 통계적인 특성치이다.
    - 적절한 가정을 통해 확률 분포를 추정하는 것이다.
    - 모수적 방법론 & 비모수적 방법론
        - 모수적 방법론
            - 데이터가 특정 확률 분포를 따른다고 가정한 뒤 모수를 추정한다.
        - 비모수적 방법론
            - 데이터가 특정 확률 분포를 따른다고 가정하지 **않고** 모수를 유연하게 바꾼다.
            - 모수를 쓰지 않는 것은 아니다!
    - 확률 분포를 가정하기 위해서는 히스토그램 모양을 관찰한다.
    - 정규분포의 모수는 평균 $\mu$과 분산 $\sigma$<sup>2</sup>
    - 표본평균
        - $\overline{X}=\dfrac{1}{N}\sum ^{N}_{i=1}X_{i}$
    - 표본분산
        - $\overline{X}=\dfrac{1}{N-1}\sum ^{N}_{i=1}\left( X_{i}-\overline{X}\right) ^{2}$

- 최대가능도 추정법(```maximum likelihood estimation, MLE```)
    - 가능도 함수
        - x를 확률분포가 가질 수 있는 실수값, $\theta$를 확률밀도함수의 모수라고 하면 확률밀도함수를 $p( x;\theta)$로 나타낼 수 있다. 여기에서 x를 상수로 놓고 $\theta$를 변수로 여긴다. 이렇게 모수를 변수로 보는 경우, 이 함수를 ```가능도 함수```라고 한다. $p\left( x;\theta \right)$를 가능도 함수로 보면 $L\left( x;\theta \right)$로 표기한다.
    - 얻어진 데이터를 바탕으로 확률변수의 모수를 구하는 방법이다.
    - [추가 내용](2022-09-22-day05.md/#statistics)
<br><Br>

## Bayesian rule
- 조건부 확률
    - 조건부확률 $P\left( A\middle| B\right)$는 사건 $B$가 일어났을 때 사건 $A$가 일어날 확률이다.
    - 베이즈 정리는 $P\left( A\cap B\right) =P\left( B\right) P\left( A\middle| B\right)$이고, $P\left( B\middle| A\right) =\dfrac{P\left( A\cap B\right) }{p\left( A\right) }$이므로 $P\left( A\cap B\right)$에 위의 식을 대입하면 $P\left( B\middle| A\right) =P\left( B\right) \dfrac{P\left( A\middle| B\right) }{p\left( A\right) }$를 얻을 수 있다.
    - 베이즈 정리를 통해 앞의 사전확률을 다음 계산의 사전확률로 사용하면 갱신된 사후확률을 얻을 수 있다.
<hr>

# 일일 회고
- 새로 알게된 것
    1. 모수
    2. 표본평균과 표본분산
        - 표본분산을 구할 때 ```불편 추정량```에 의해 $(N - 1)$로 나눈다는 사실
- 더 공부해야 할 점
    1. 최대가능도 추정법 심화과제 풀며 추가 공부 필요
<hr>

# 출처
- [모수](https://ahnjg.tistory.com/55)
- [최대가능도 추정법 I](https://losskatsu.github.io/statistics/mle/#)
- [최대가능도 추정법 II](최대가능도 추정법 I)