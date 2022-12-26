---
title: "Boostcamp AI Tech - W15 Day 69"
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
- `MultiVAE` 베이스라인을 작성하였다.
  - sparse 데이터를 압축할 때 shape에서 인덱스 오류가 발생하였다. 
    ```python
    train_data = sparse.csr_matrix((np.ones_like(rows),
      (rows, cols)), dtype="float64",
      shape=(end_idx - start_idx + 1, self.n_items))
    ```
  - 원인을 분석해본 결과, user id와 item(movie) id가 1부터 최대 id까지 모두 균일하게 있지 않기 때문이라고 판단하였다.
  - 따라서 user와 item을 dictionary를 이용해 인덱스로 변경해주었다.
    ```python
    def numerize(self, df, user2id, item2id):
      user = df['user'].apply(lambda x: user2id[x])
      item = df['item'].apply(lambda x: item2id[x])
      return pd.DataFrame(data={'user': user, 'item': item}, columns=['user', 'item'])
    ```


## 2. 앞으로의 계획
- 최종 프로젝트
  - 데이터 크롤링
  - 데이터 EDA 및 전처리
- Movie Recommendation 대회
  - MultiVAE inference 코드 작성
  - 하이퍼파라미터 튜닝, feature engineering으로 모델 성능 개선


## 3. 피어세션
- MultiVAE 코드에서 발생한 오류를 함께 해결하였다.
- S3Rec 모델에 적용한 sweep과, 앞으로의 진행 방향을 공유하였다.