---
title: "Boostcamp AI Tech - Day 02"
categories:
  - Boostcamp AI Tech
tags:
  - python
  - ai math
---

## AI Math & Python Basices for AI

1. [Python](#Python)
    - [Python Data Structure](#variable--list)
        - [Stack](#variables)
        - [Queue](#list)
        - [Tuple](#tuple)
        - [Set](#set)
        - [Dict](#dict)
        - [Collections](#collections)
2. [AI Math](#ai-math)
    - [Gradient Descent I](#gradient-descent-i)
<hr><hr>
<br><br>

# Python

## Python Data Structure
<hr>

### Stack
- 스택은 마지막에 넣은 데이터가 먼저 나오는 구조이다.
- 감자칩 통을 생각하면, 가장 먼저 들어간 감자칩을 가장 나중에 먹게 되는 것과 같다.
- 이를 ```LIFO(Last In First Out)```이라 한다.
- ```push```는 데이터를 넣는 것, ```pop```은 가장 나중에 들어간 데이터를 꺼내 반환하는 것이다.
```python
stack = [1, 2, 3, 4, 5]
stack.append(6)
stack.pop() # 5
```

### Queue
- 스택과 반대로 먼저 들어간 데이터가 먼저 나온다.
- 양쪽이 뚫려 있는 파이프를 생각하면 된다.
- 이를 ```FIFO(First In First Out)```이라 한다.
```python
queue = [1, 2, 3, 4, 5]
queue.append(6)
queue.pop(0) # 1
```

### Tuple
- 값의 변경이 불가능하다.
- 선언할 때 리스트와 다르게 ```()```를 사용한다.
```python
tp = (1, 2, 3)
tp[1] = 4 # 불가능
```

### Set
- 값의 순서가 없고, 중복이 불가능하다.
```python
s = set([1, 2, 1, 2, 1, 2, 3])
print(s) # {1, 2, 3}
```
- 추가(```add```), 삭제(```remove```, ```discard```), 리스트 추가(```update```), 비우기(```clear```) 동작이 가능하다.
- 또한 수학의 집합연산도 가능하다. 합집합(```union```, ```|```), 교집합(```intersection```, ```&```), 차집합(```difference```, ```-```)

### Dict
- ```Key``` : ```Value``` 형태로 저장하는 구조이다.
- 이때 키값은 고유해야 한다.
- ```key```을 통해 ```value```를 찾을 수 있다.

### Collections
1. deque
    - ```stack```, ```queue```가 모두 동작하는 모듈이다.
    - ```append```, ```appendleft```, ```pop```, ```popleft``` 등을 지원한다. ```left```가 들어간 동작을 통해 큐를 쉽게 동작시킬 수 있다.
2. defaultDict
    - dict에 신규 값을 디폴트로 지정할 수 있다. 
    ```python
    dd = defaultdict(object)
    dd = defaultdict(lambda: 0) # 디폴트 값 0
    ```
    - 쉽게 딕셔너리 값들을 초기화할 수 있어, keyError의 발생 가능성을 줄일 수 있다.
3. counter
    - 특정 원소의 개수를 세서 딕셔너리로 반환한다.
4. namedtuple
    - 구조체와 비슷하다.

<br><br>
<hr>

# AI Math

## Gradient Descent (I)
<hr>

- 미분
    - 변화율의 극한이다.
    - 미분을 통해 주어진 점에서의 접선의 기울기를 구할 수 있다.
    - 접선의 기울기를 알면 함수값의 증가/감소 방향을 알 수 있다.
- 경사상승법
    - 미분값을 더하는 것을 ```경사상승법```이라 하며 함수의 극대값 위치를 구할 수 있다.
- 경사하강법
    - 미분값을 빼는 것을 ```경사하강법```이라 하며 함수의 극소값 위치를 구할 수 있다.
    - 미분값이 알고리즘 종료조건보다 클 동안 반복하며 학습률을 이용해 특정 값을 변경시킨다. 업데이트된 값에 다시 미분을 적용하며 최소값을 찾을 때까지 업데이트한다.
- 편미분
    - 변수가 여러 개인 경우 편미분을 사용한다.
    - 특정 변수 외에는 상수취급한 뒤 미분을 진행한다.
    - 각 변수별로 그레디언트 벡터를 이용해 경사하강법 또는 경사상승법에 사용할 수 있다.
    - 그레디언트 벡터는 등위곡선에서 함수값이 가장 빠르게 증가하는/감소하는 방향을 찾을 때 사용된다.