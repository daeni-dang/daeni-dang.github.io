---
title: "Boostcamp AI Tech - Day 07"
categories:
  - daily-report
tags:
  - pytorch
toc: true
toc_sticky: true
---

## PyTorch

## 1. 오늘 배운 내용
### 1.1 torch.nn
- => [torch.nn documentation](https://pytorch.org/docs/stable/nn.html#linear-layers)
- ```basic building block```
  1. ```nn.Linear```
    - [nn.Linear documentation](https://pytorch.org/docs/stable/nn.html#linear-layers)
  2. ```nn.Identity```

### 1.2 nn.Module
- => [nn.Module documentation](https://pytorch.org/docs/stable/generated/torch.nn.Module.html)
- 여러 기능들을 한 곳에 모아두는 역할
  1. ```nn.Sequential```
    - 모듈들을 하나로 묶어 순서대로 실행
  2. ```nn.ModuleList```
    - ```List```와 같이 ```index```를 통해 접근 가능
    - ```ModuleList```를 사용해야 ```mm.Module```의 파라미터가 된다.
  3. ```nn.ModuleDict```
    - ```dictionary```와 같이 ```key```와 ```value```로 구성

### 1.3 Parameter
- => [nn.parameter](https://pytorch.org/docs/stable/generated/torch.nn.parameter.Parameter.html?highlight=parameter)
- ```nn.Module``` 안에 ```tensor```을 보관할 수 있다.
- ```tensor```와 다르게 ```parameter```로 만들어야 ```module```의 파라미터가 된다.

### 1.4 Buffer
- => [buffer](https://pytorch.org/docs/stable/generated/torch.nn.Module.html?highlight=register_buffer#torch.nn.Module.register_buffer)
- ```tensor```을 ```buffer```로 등록하면 저장이 된다.

### 1.4 ```Tensor``` vs ```Parameter``` vs ```Buffer```

|-|Tensor|Parameter|Buffer|
|:---:|:---:|:---:|:---:|
|gradient 계산|X|X|X|
|값 업데이트|O|O|O|
|모델 저장 시 값 저장|X|X|O|

### 1.5 hook
- 자신의 코드를 package 중간중간에 실행할 수 있도록 하는 인터페이스
- 프로그램 실행 앞/뒤 모두 가능하다.
  1. ```forward hook```
    - ```module```에만 적용할 수 있다. [register_forward_hook](https://pytorch.org/docs/stable/generated/torch.nn.Module.html?highlight=hook#torch.nn.Module.register_forward_hook)
  2. ```backward hook```
    - ```module```과 ```tensor``` 모두에 적용할 수 있다. [tensor - register_hook](https://pytorch.org/docs/stable/generated/torch.Tensor.register_hook.html#torch.Tensor.register_hook), [module - register_full_backward_hook](https://pytorch.org/docs/stable/generated/torch.nn.Module.html?highlight=register_full#torch.nn.Module.register_full_backward_hook)
- 참고 링크
  - https://blog.paperspace.com/pytorch-hooks-gradient-clipping-debugging/
  - https://medium.com/the-dl/how-to-use-pytorch-hooks-5041d777f904

### 기타: Class의 forward 함수
- forward() 함수는 model 객체를 호출하면 자동으로 실행되는 함수이다.
- => [forward](https://wikidocs.net/60036)


## 2. 과제 수행
- (기본-1) Custom Model 제작
  - [Math operations - Blas and LAPACK Operation] 부터 hook까지 수행


## 3. Peer Session
- 책 리뷰 => 10/3
- ```torch.normal``` 질문 (해결) : [Day06 질문 1](2022-09-26-Boostcamp-AI-Tech-Day06.md/#4-회고)
- ```torch.anble``` 질문 => 오일러 공식