---
title: "Boostcamp AI Tech - Day 09"
categories:
  - daily-report
tags:
  - pytorch
toc: true
toc_sticky: true
---

## PyTorch

## 1. 오늘 배운 내용
### 1.1 모델 저장하기 & 불러오기
- [모델 저장 & 불러오기](https://daeni-dang.github.io/til/model-save/)

### 1.2 전이 학습
- 공부중!

## 2. 과제 수행
- (기본-2) Custom Dataset 및 Custom DataLoader 생성
    - 여러 데이터셋을 이용해 ```__init__```, ```__len__```, ```__getitem__```을 완성하였다.
    1. Titanic
        - Titanic 데이터셋은 타이타닉에 탑승했던 승객들의 정보와 생존 여부가 들어있어, 데이터에는 drop_features와 Survived를 제외한 정보를 담았고, 라벨에는 생존 여부를 담았다.
    2. MNIST
        - 이미지와 라벨로 구성되어 있어, 이미지 라벨을 각각 데이터, 라벨로 구성하였다.
    3. AG_NEWS
        - 기사 제목/내용과 카테고리가 들어있었다. 데이터를 제목+내용으로, 라벨을 카테고리로 구성하였다.

## 3. Peer Session
- 과제 수행 중 어려웠던 점을 얘기하였다.