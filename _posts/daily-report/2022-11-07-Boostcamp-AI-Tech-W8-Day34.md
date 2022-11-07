---
title: "Boostcamp AI Tech - W8 Day 34"
categories:
  - daily-report
tags:
  - AI Service Development Fundamentals
toc: true
toc_sticky: true
---

## AI 서비스 개발 기초

## 1. 오늘 배운 내용
### MLOps 개론
머신 러닝 모델은 `Research` 상황인지,  `Production` 상황인지에 따라 다르게 개발해야 한다.
- `Research`
	- `문제 정의` -> `EDA` -> `Feature Engineering` -> `Train` -> `Predict`
	- 고정된 데이터를 사용해 학습을 진행하며, 모델의 성능에 초점을 맞춘다.
- `Production`
	- `문제 정의` -> `EDA` -> `Feature Engineering` -> `Train` -> `Predict` -> `Deploy`
	- 웹, 앱 서비스를 실제로 활용할 수 있도록 배포하는 `deploy` 과정이 추가된다. 이 과정은 모델에게 데이터를 제공하면서 예측해달라고 요청하는 과정이다.
	- 이렇게 실제로 배포하면 모델의 결과값이 이상한 경우가 존재한다. 
	- 또한 성능이 `Research` 환경에선 좋았지만 `Production` 상황에서는 좋지 않은 경우가 발생한다.

MLOps란 ML(Machine Learning)과 Ops(perations)를 합한 것으로 **머신러닝 모델을 운영하면서 반복적으로 필요한 업무를 자동화시키는 과정**이다. 즉, 모델링에 집중할 수 있도록 관련된 인프라를 만들어 자동으로 운영되도록 하는 일이다.


### MLOps Component
**Server 인프라** : 레스토랑 장소 선정 (트래픽, 서버의 성능, 스케일 업/아웃, 자체 서버 구축/클라우드)
**GPU 인프라** : 식기 임대(클라우드 GPU)
**Serving** : 음식 서빙(Batch serving-일정 주기/online serving-실시간)
**Experiment, Model Management** : 파라미터, 모델 구조, 모델 Artifact, 여러 모델 운영 -> mlflow : 파라미터, metric 등 자동으로 로그 기록해주는 라이브러리
**Feature Store** : feature를 미리 만들어 둠 -> FEAST
**Data Validation** : feature의 분포 확인, Data drift, model drift, concept drift -> AWS Deequ
**Continuous Training** : retrain(다시 만듦)
**Monitoring** : 모델 지표, 인프라 성능 지표 등 기록 -> AutoML

### Further Question
- MLOps가 필요한 이유
	- `Research` 환경과는 다르게 실제로 서비스를 제공할 때는 인프라도 고려해야 하고, 지속적으로 모델을 업그레이드 해주어야 하기 때문이다.
- MLOps의 각 Component에 대해 이해하기(왜 이런 component가 생겼는가?) MLOps의 각 컴포넌트에서 해결하고 싶은 문제는 무엇이고, 그 문제를 해결하기 위한 방법으로 어떤 방식을 활용할 수 있는지
	- Server Infra
	- GPU Infra
	- Serving
	- Experiment, Model Management
	- Feature Store
	- Data Validation
	- Continuous Training
	- Monitoring
- MLOps와 관련된 자료, 논문 읽어보며 강의 내용 외에 어떤 부분이 있는지 파악해보기
- MLOps Component 중 내가 매력적으로 생각하는 TOP3를 정해보고 왜 그렇게 생각했는지 작성해보기

## 2. 피어세션
- NGCF 논문 리뷰하기로 결정하였다. (11/10 목 피어세션 시간)

## 3. 더 공부할 내용
- MLE
- Transformer
- MF, ALS