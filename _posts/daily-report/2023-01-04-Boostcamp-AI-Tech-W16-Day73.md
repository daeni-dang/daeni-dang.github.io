---
title: "Boostcamp AI Tech - W16 Day 73"
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
- 저번에 새로운 `MultiVAE`, `MultiDAE` 코드의 속도 문제는 gpu를 사용하지 않아서였다.
```python
args.device = torch.device("cuda" if torch.cuda.is_available() else "cpu")
```
- 위 코드를 추가하여 해결하였다.
- inference가 잘 되지 않는 문제가 있었는데 해결하여 베이스라인 작성을 완료하였다.
- 베이스라인 성능은 `MultiDAE`: 0.1281, `MultiVAE`: 0.1209로 `MultiDAE`가 조금 더 좋은 성능을 보였다.


### 프로젝트
- v1에서는 프론트앤드를 담당하게 되었다.
- 백앤드는 fastAPI, 프론트앤드는 새로 나온 프레임워크인 스벨트(svelte)를 사용하기로 하였다.
- 부트스트랩 템플릿을 활용해 메인 화면의 큰 틀을 구성하였다. [템플릿 링크](https://startbootstrap.com/template/shop-homepage)

## 2. 앞으로의 계획
- 최종 프로젝트
  - 로그인 기능의 화면을 구성
- 대회
  - 내일이 대회 마무리이므로 MultiDAE sweep을 이용해 하이퍼파라미터 튜닝


## 3. 피어세션
- 프로젝트에서 담당할 역할을 분배하였다.
- 대회의 wrap report를 작성하는 시간을 가졌다.