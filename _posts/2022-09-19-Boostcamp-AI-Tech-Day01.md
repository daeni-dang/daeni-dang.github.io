---
title: "Boostcamp AI Tech - Day 01"
categories:
  - Boostcamp AI Tech
tags:
  - python
  - ai math
toc: true
toc_sticky: true
---

## AI Math & Python Basices for AI

<br>

## Python

### Variable & List
<hr>

#### Variables
- 변수란 ```값을 저장하는 장소```이다.

- 각 변수는 메모리 주소를 가지고 있으며, 변수에 들어가는 값은 메모리 주소에 할당된다.

- 자료형
 자료형은 처리할 수 있는 데이터 유형으로 종류는 아래 표와 같다.

|유형|설명|
|:---:|:---:|
|integer|정수|
|float|실수|
|string|문자형|
|boolean|참 or 거짓|

- 파이썬은 ```Dynamic Typing 언어```로, 사용자가 직접 자료형을 지정하지 않고 실행 중 자료형이 결정된다는 특징이 있다.

#### List
- List는 ```여러 개의 데이터의 집합```이다.
- 파이썬의 경우 리스트 안에 ```다양한 자료형의 데이터```를 넣을 수 있다.
```python
a = ['hello', 1, 0.35]
```
- 리스트 안의 값들은 주소(offset)을 가지므로, ```주소를 사용```해서 할당된 값을 호출한다.
```python
array = ['a', 'b', 'c']
print(array[2]) # c
```
- 리스트 안의 값을 ```슬라이싱```하여 부분 값을 얻을 수 있다.
```python
array = ['a', 'b', 'c', 'd', 'e', 'f', 'g']
print(array[1:6]) # b ~ f
```
- 리스트의 연산
    1. **concatenation**
        - 여러 개의 리스트를 이어붙인다.
        ```python
        arr1 = ['a']
        arr2 = ['b']
        print(arr1 + arr2) # ['a', 'b']
        ```
    2. **is_in**
        - 특정 원소가 리스트에 있는지 확인한다.
        ```python
        arr = ['apple', 'banana']
        print('apple' in arr) # true
        ```
    3. **append**
        - 특정 원소를 리스트의 뒤에 추가한다.
        ```python
        arr = ['apple', 'banana']
        arr.append('melon')
        print(arr) # ['apple', 'banana', 'melon']
        ```
    4. **extend**
        - 리스트에 새로운 리스트를 추가한다.
        ```python
        arr = ['apple', 'banana']
        arr.extend(['melon', 'watermelon'])
        print(arr) # ['apple', 'banana', 'melon', 'watermelon']
        ```
    5. **insert**
        - 리스트의 x번째 위치에 추가한다.
        ```python
        arr = ['apple', 'banana']
        arr.insert(0, 'grape')
        print(arr) # ['grape', 'apple', 'banana']
        ```
    6. **remove & del**
        - 리스트에서 특정 원소를 삭제한다.
        ```python
        arr = ['apple', 'banana', 'grape']
        arr.remove('apple')
        print(arr) # ['banana', 'grape']
        del arr[0]
        print(arr) # ['grape']
        ```
- 패킹과 언패킹
    1. **패킹**
        - 한 변수에 ```여러 개의 데이터```를 넣는 것이다.
            ```python
            a = [1, 2, 3]
            ```
    2. **언패킹**
        - 한 변수로 패킹되어있는 데이터를 ```각각 변수로 변환```하는 것이다.
            ```python
            a = [1, 2, 3]
            x, y, z = a
            ```
<br>
<br>

### Functions & Console IO
<hr>

#### function
- 함수란 ```특정 동작을 하는 코드의 덩어리```이다.
- 함수로 코드를 ```캡슐화```할 수 있다.
```python
def 함수명(parameter1, ...):
    statements
    return 반환값
```
- parameter & argument
    - **parameter**
        - 함수에서 입력받는 값으로, 아래 코드에서 x에 해당한다.
        ```python
        def f(x):
            return x
        ```
    - **argument**
        - 실제로 parameter에 대입된 값으로, 아래 코드에서 f에 대입된 값인 2이다.
        ```python
        print(f(2))
        ```
#### console I/O
- input 함수를 이용해 ```문자열을 입력```받을 수 있다.
```python
something = input()
```
- 숫자를 입력받기 위해서는 ```형변환```을 해주어야 한다.
```python
something_int = int(input())
something_float = float(input())
```
- print formatting
    1. **%-format**
        - ```%datatype % (variable)``` 형태로 표현한다.
        ```python
        print("I have %d pens." % 3)
        print("I have %s." % "pen")
        print("I have %d %s." % (3, "pens"))
        ```
        - %와 자료형 문자 사이에 숫자를 집어넣어 총 차지하는 공간을 설정할 수 있다.
        ```python
        print("I have %5d pens." % 3)
        ```
        - 또한 float형 숫자를 표현할 때는 아래와 같이 표현하여 소수점 뒤의 자릿수를 결정할 수 있다.
        ```python
        print("%8.2f" % 39.4444)
        ```
    2. **str.format()**
        - ```"~~{datatype}~~".format(argument)``` 형태로 표현한다.
        - 중괄호 안에는 format 내에서 쓰고자 하는 파라미터의 인덱스를 넣는다.
        ```python
        number = 10
        print("I have {0} pens".format(number))
        ```
        - 이 형태에서도 마찬가지로 총 차지하는 공간과 소수점 뒤의 자릿수를 정할 수 있다.
        ```python
        print("{0:5d}, {1:8.2f}".format(123, 48.2314)
        ```
        - '>'와 '<'를 사용하여 정렬할 수 있다.
        ```python
        print("{0:>10s}".format("apple")) # 오른쪽 정렬
        print("{0:<10s}".format("apple")) # 왼쪽 정렬
        ```
    3. f-string (현재 많이 사용!)
        ```python
        name = "Daeun"
        age = 23
        print(f"Hello, my name is {name}. My age is {age}".)
        ```

<br>
<br>

## Conditionals & Loops
<hr>

### condition
- 조건문이란 조건에 따라 특정한 동작을 하게 하는 것이다.
- ```if```, ```elif```, ```else```의 예약어를 사용한다.
```python
if <조건>:
    <동작>
elif <조건>:
    <동작>
else:
    <동작>
```
- ```if/elif``` 다음에 나오는 조건의 참 또는 거짓을 판단한다. 비교 연산자로는 ```<, >, <=, >=, ==, !=``` 가 있다.
- 조건문에는 ```and, or, not``` 논리 키워드를 사용해 참과 거짓을 판단할 수도 있다.
- 삼항 연산자는 참일 경우와 거짓일 경우를 한 줄에 표현하는 연산자이다.
```python
num = 12
is_odd = True if num % 2 != 0 else False
```

### loop
- 반복문이란 특정 동작을 반복적으로 수행하는 것이다.
- 반복문은 ```반복 시작 조건```, ```반복 종료 조건```, ```수행 명령```으로 구성된다.
- ```for```, ```while```의 예약어를 사용한다.
```python
for i in range(10):
    print(i)
num = 0
while num < 10:
    print(num)
    num += 1
```
- for문에서 range에 ```step```을 줄 수 있다. 음수를 넣으면 역순으로 탐색한다.
```python
for i in range(0, 10, 2):
    print(i) # 0부터 10까지 2씩 증가시킴
for i in range(10, 0, -1):
    print(i) # 10부터 0까지 1씩 감소시킴
```
- ```break```를 통해 특정 조건에서 반복문을 종료시킬 수 있다.
- ```continue```를 통해 특정 조건에서 남은 명령을 건너뛰고 반복문 상단으로 이동할 수 있다.

### debugging
- 디버깅이란 코드에서 오류를 발견해 수정하는 작업이다.
- 문법적 에러 & 논리적 에러.
    1. **문법적 에러**
        - 들여쓰기 실수, 오탈자 등 오류 메시지를 통해 알 수 있는 에러이다.
    2. **논리적 에러**
        - 의도하지 않은 동작을 하는 에러이다.

<br>
<br>

## String and advanced function concept
<hr>

### string
- 시퀀스 자료형으로, 문자 데이터를 메모리에 저장한다.
- 문자열의 각 문자는 각각의 주소를 가진다.
- 리스트와 같은 형태이다.
- raw string
    - ```\```와 같은 특수문자를 있는 그대로 출력한다.

### function 2
- **함수 호출 방식**
    1. 값에 의한 호출(call by value)
        - 함수에 인자를 넘길 때 ```값```만 넘긴다.
        - 함수 내에서 인자의 값을 변경하더라도, 호출자에는 영향을 주지 않고 함수 내에만 영향을 끼친다.
    2. 참조에 의한 호출(call by reference)
        - 함수에 인자를 넘길 때 ```메모리 주소```를 넘긴다.
        - 함수 내에서 인자의 값을 변경하면, 호출자에서의 값도 변경된다.
    3. 객체 참조에 의한 호출(call by object reference)
        - ```객체의 주소```가 함수로 전달된다.
        - 전달된 객체를 참조하여 변경한다면 호출자에 영향을 준다.
        - 하지만 새로운 객체를 만들면 호출자에게 영향을 주지 않는다.
- **scoping rule**
    - 지역 변수 : ```함수내```에서만 사용
    - 전역 변수 : ```프로그램 전체```에서 사용
    - 함수 내에서 전역변수를 사용하려면 ```global``` 키워드를 사용해야 한다. 사용하지 않는다면 같은 이름이라도 지역 변수 취급된다.
- **recursive function**
    - ```자기 자신을 호출```하는 함수이다.
    ```python
    def factorial(n):
        if n == 1:
            return 1
        else:
            return n * factorial(n - 1)
    ```
- **function type hint**
    - 파라미터에 변수 타입을 함께 적어주고, 함수 선언 뒤에 반환 타입을 함께 명시하는 것이다.
    ```python
    def f(var_name : var_type) -> return_type:
        pass
    ```
    - 이를 통해 사용자가 사용하기 쉽게 제공할 수 있다.
    - 시스템의 안정성을 확보할 수 있다.

<hr> 
<br><br>

# AI Math
## Vector
- 벡터란 ```숫자를 원소로 가지는 리스트 또는 배열```이다.
- 벡터는 공간에서 ```한 점 또는 원점으로부터 상대적 위치```이다.
- 같은 모양의 벡터끼리는 덧셈, 뺄셈, 성분곱 연산이 가능하다.
- **벡터의 덧셈**
    - 두 벡터의 덧셈은 다른 벡터로부터 상대적 위치이동이다.
- **벡터의 norm**
    - ```벡터의 norm```이란 원점으로부터의 거리이다.
    1. **L1 norm**
        - 각 성분 변화량의 ```절댓값의 합```
    2. **L2 norm**
        - ```유클리드 거리```
- **두 벡터 사이의 거리**
    - 벡터의 뺄셈을 이용해 두 벡터 사이의 거리를 계산할 수 있다.
- **두 벡터 사이의 각도**
    - L2 norm과 내적을 이용해 각도를 구할 수 있다.
- **내적**
    - 내적은 정사영 길이를 \|\|**y**\|\|만큼 조정한 값이다.
    - 내적은 두 벡터의 유사도 측정에 사용할 수 있다.

## Matrix
- 행렬이란 ```벡터를 원소로 가지는 2차원 배열```이다.
- 행렬은 ```행(row)```과 ```열(column)```을 가진다.
- 행렬은 ```여러 점들```을 나타낸다.
- 같은 모양의 행렬끼리는 덧셈, 뺄셈, 성분곱을 연산할 수 있다.
- 행렬 곱셈은 i번째 행벡터와 j번째 열벡터 사이의 내적 연산을 통해 구할 수 있다.
- 따라서 행렬 곱셈을 하기 위해서는 한 행렬의 ```열의 개수```와 다른 행렬의 ```행의 개수```가 같아야 한다.
- 행렬은 벡터공간에서 사용되는 연산자이다.

- **역행렬**
    - 행렬의 연산을 거꾸로 되돌리는 행렬이며, A<sup>-1</sup>로 표기한다.
    - 역행렬이 가능하기 위해서는, 
        1. 행과 열 숫자가 같아야 한다.
        2. 행렬식이 0이 아니어야 한다.
    - 역행렬을 계산할 수 없다면 ```유사역행렬(pseudo-inverse)``` 또는 ```무어 펜로즈(Moore-Penrose) 역행렬``` A<sup>+</sup>를 이용한다. 이를 이용하면 행과 열이 같지 않아도 역행렬과 유사한 동작을 할 수 있다.
    
<br>