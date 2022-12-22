---
title: "Boostcamp AI Tech - W14 Day 67"
categories:
  - daily-report
tags:
  - Movie Recommendation
toc: true
toc_sticky: true
---

## Movie Recommendation

## 1. 오늘 배운 내용

### 대회
- `MultiVAE` 데이터로더를 구현하였다.
- 처음에는 유저 단위로 train/valid 데이터를 나누려고 했으나, test 데이터 구성이 train 데이터에 있는 모든 유저를 포함하고 있기 때문에 이는 좋지 않은 방법이라 판단하였다.
- 따라서 유저 시퀀스에서 10%를 가지고와서 이를 valid 데이터로 사용하기로 하였다.

- 구현 방법
  - `raw data`를 불러온 뒤, `Counter`을 이용해 각 user 시퀀스의 길이를 셌다.
  - `sklearn.model_selection`의 `train_test_split`을 사용해 각 유저 시퀀스에서 train 데이터로 사용할 인덱스와 valid 데이터로 사용할 인덱스를 뽑아주었다.
  - 해당 인덱스에 일치하는 train_data와 valid_data를 나누어주었다.

- MultiVAE는 user와 item의 interaction 정보를 input으로 사용하기 때문에 sparse해진다. 따라서 `sparse.csr_matrix`를 이용해 sparse 데이터를 압축해주었다.

### 멘토링
- 최종 프로젝트 주제에 대한 논의
- 이력서에 대한 피드백
  - 직무에 fitting해서 쓰기
  - 프로젝트 요약 빼기
  - 교육에는 공인에서 인정받은 것만(학교) -> 부캠은 외부 교육(추가 활동) 파트로 빼기

  - 기술 역량
    - 프로그래밍 언어, pytorch, tensorflow, scikit - learn
  - IDE는 괜찮다.
 
  - 자기소개
    - 직무에 맞춘 PR
    - 프로젝트 했을 때도 반영. 스토리 라인을 관심 직무에 맞춰서.
 
  - 베스트는 한페이지, 최대 두페이지
 
  - educational experience
 
  - framework 에서 django 따로 빼기(backend)
 
  - 수상경력(Honors and Awards) 주최 적기
 
  - project experience -> project
  - 프로젝트는 시간순으로
  - 고민했던 점은 optional. 너무 길면 빼기
 


## 2. 앞으로의 계획
- MultiVAE basline 작성



## 3. 피어세션
- 최종 프로젝트 주제에 대해 논의하였다.