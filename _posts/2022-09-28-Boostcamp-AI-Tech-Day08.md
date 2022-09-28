---
title: "Boostcamp AI Tech - Day 08"
categories:
  - Boostcamp AI Tech
tags:
  - pytorch
toc: true
toc_sticky: true
---

## PyTorch

## 1. 오늘 배운 내용
### 1.1 Dataset
  1. ```__init__(self,)```
        - 파일로부터 읽어온 데이터, 경로, 클래스 등을 초기화 작업을 하는 곳이다.
  2. ```__len__(self)```
        - 읽어온 데이터셋의 길이를 반환한다.
  3. ```__getitem__(self, idx)```
        - 읽어온 데이터셋의 ```idx```번째 데이터를 반환한다.

### 1.2 DataLoader
  - dataset, batch_size, shuffle, sample, collate_fn 등을 지정한다.
    
### 1.3 학습 과정
  - ```Data``` ==> ```Dataset``` ==> ```DataLoader``` ==> ```Model```

## 2. 과제 수행
- (기본-2) Custom Dataset 및 Custom DataLoader 생성
    - 여러 데이터셋을 이용해 Custom Dataset의 ```__init__```, ```__len__```, ```__getitem__```을 작성해보았다.
    - ```DataLoader```의 인자들을 직접 작성해보았다.
        - ```collate_fn```을 활용해보았다.
            - ```collate_fn```은 기존의 [(label, data), (label, data) ...] 형식으로 있던 데이터를 [(label, label, ...)과 (data, data, ...)] 형식으로 변경하는 것이다.
            - 이를 활용해보는 과제 중 tensor을 0으로 padding하는 문제가 있었다. 이를 위해 ```tensor.cat```을 사용하였다.

## 3. Peer Session
- 멘토님이 주신 질문을 보며 답을 하는 시간을 가졌다.