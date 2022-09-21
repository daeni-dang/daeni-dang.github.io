---
title: "Boostcamp AI Tech - Day 01"
categories:
  - Boostcamp AI Tech
tags:
  - python
  - ai math
---

## AI Math & Python Basices for AI

1. [Python](#Python)
    - [Pythonic Code](#pythonic-code)
        - [split & join](#split--join)
        - [list comprehension](#list-comprehension)
        - [enumerate & zip](#enumerate--zip)
        - [asterisk](#asterisk)
    - [Python Object Oriented Programming](#python-object-oriented-programming)
2. [AI Math](#ai-math)
    - [Deep Learning Basic](#deep-learning-basic)
    - [Probability theory](#probability-theory)
<hr><hr>
<br><br>

# Python

## Pythonic Code
<hr>

### split & join
1. split
    - ```string``` 타입의 값을 매개변수로 넘긴 구분자를 기준으로 나누어 리스트로 변환한다.
2. join
    - ```string```으로 구성되어있는 ```list```를 지정한 구분자로 구분해 하나의 ```string```으로 합친다.
    ```python
    fruits = ['apple', 'grape', 'banana']
    print(','.join(fruits)) # apple,grape,banana
    ```

### list comprehension
- ```list```를 이용해 다른 ```list```로 만드는 기법
```python
numbers = [i for i in range(10)]
```

### enumerate & zip
1. enumerate
    - ```list```의 원소들에 순서대로 번호를 붙여서 얻어낼 수 있다.
    ```python
    for num, value in enumerate(['apple', 'banana', 'grape']):
        print(num, value) 
        # 0 apple
        # 1 banana
        # 2 grape
    ```
2. zip
    - 두 개의 ```list```에서 병렬적으로 값을 추출한다.
    ```python
    list1 = ['a', 'b', 'c']
    list2 = ['A', 'B', 'C']
    for one, two in zip(list1, list2):
        print(one, two)
        # a A
        # b B
        # c C
    ```
### asterisk
- 가변인자를 사용하는 방법
- ```asterisk(*)``` 기호를 사용해 ```parameter```를 표시한다.
1. ```*args```
    - ```asterisk``` 변수는 는 가장 마지막 ```parameter``` 위치에 한 개만 사용할 수 있다.
    - 아래 코드에서 ```args``` 부분의 이름을 지정할 수 있다.
    ```python
    def asterisk(a, b, *args):
        return a + b + sum(args)
    asterisk(1, 2, 3, 4, 5, 6, 7)
    ```
    - ```tuple``` 형태이다.
2. ```kwargs```
    - 함수를 호출할 때 (키워드=값) 형태를 사용한다.
    - ```dict``` 형태로 함수 내부로 전달된다.
    ```python
    def asterisk(a, **kwargs):
        print(kwargs)
    asterisk(1, b=2, c=3)
    ```

## Python Object Oriented Programming

- 객체는 ```attribute```(=```variable```)와 ```action```(=```method```)을 가진다. 
- ```OOP```는 ```class```와 ```instance```로 구성된다.
- ```class```는 설계도이고, ```instance```는 실제로 구현되는 부분이다.
- 파이썬에서 ```class``` 구현
    ```python
    class ClassName(object):
    ```
    - 위의 코드에서 클래스 이름과, ```object``` 부분에는 상속받는 객체를 넣으면 된다.
    - ```__init__```은 객체를 초기화하는 예약 함수이다.
    ```python
    def __init__(self, ...):
    ```
    - ```class```의 ```method```를 구현하기 위해서는 매개변수로 ```self```를 추가해야 한다.
- ```OOP```의 특징
    1. 상속(```inheritance```)
        - 자식 클래스에게 부모 클래스로의 ```attribute```와 ```action```을 물려주는 것이다.
        - 클래스명 뒤에 물려받고자 하는 클래스명을 적으면 된다.
    2. 다형성(```polymorphism```)
        - ```method```가 같은 이름을 가졌지만 내부 로직은 다른 경우이다.
    3. 가시성(```visibility```)
        - 객체 내부의 정보를 누구나 볼 수 있지 않도록 하는 것이다.


<br><br>
<hr>

# AI Math

## Deep Learning Basic
<hr>

- 신경망
    - 신경망이란 ```선형모델 + 활성함수```를 합성한 것이다. 
    - 활성함수가 사용되지 않았다면 딥러닝이라 할 수 없다.
    - ```activation function```
        1. ```sigmoid``` 함수
        2. ```tanh``` 함수
        3. ```ReLU``` 함수
    - 주어진 입력 데이터들로부터 선형모델로 인해 변형된 벡터에 ```activation function```을 씌워 ```잠재벡터```로 만들 수 있다.
    - 여러 층으로 구성하면 학습에 더 효율적이다.
    - **역전파 알고리즘**
        - ```연쇄법칙```을 사용한다.
        - 연쇄법칙을 통해 합성함수를 미분할 수 있다.
        - 역전파(```backpropagation```) 알고리즘은 이름 그대로 ```윗층에서부터 아래층으로``` 계산 결과를 전달하며 계산한다. 이때 연쇄법칙을 이용한다.

## Probability theory
<hr>

- **확률 변수**
    - 확률 변수란 결과값이 어떤 확률로 정해지는 ```변수```이다.
    1. 이산확률변수
        - 확률 변수가 어떤 값을 가지며, 가지는 값의 개수를 ```셀 수 있는``` 확률분포이다.
    2. 연속확률변수
        - 확률 변수가 가지는 값의 개수를 ```셀 수 없다```.
        - 확률 밀도 함수를 이용해 분포를 표현할 수 있다.
- **확률 분포**
    - 확률 분포란 확률 변수가 특정한 값을 가질 확률을 나타내는 ```함수```이다. 확률 변수와 특정 값을 가질 확률이 ```mapping```되므로, 함수이다.
    
- **몬테카를로 샘플링 방법**
    - 몬테카를로 방법은 이산형, 연속형 모두 성립한다.
    - 몬테카를로 방법은 ```random number```을 이용해 함수의 값을 계산하는 방법이다.
    - 즉, ```대수의 법칙```에 의해 수렴할 수 있다.
    - ```대수의 법칙```이란 측정 횟수가 아주 많으면 예상 결과와 인접한다는 법칙이다.


## 출처
- [확률 분포 위키백과](https://ko.wikipedia.org/wiki/%ED%99%95%EB%A5%A0_%EB%B6%84%ED%8F%AC)
- [확률 변수와 확률 분포](https://losskatsu.github.io/statistics/prob-distribution/#%EC%9D%B4%EC%82%B0%ED%99%95%EB%A5%A0%EB%B6%84%ED%8F%AC)