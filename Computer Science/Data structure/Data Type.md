<h1>Data Type</h1>
자료형(Data type)은 프로그래밍 언어에서 사용되는 데이터의 종류를 나타내며, 컴퓨터 메모리에 어떤 종류의 데이터를 저장할 것인지를 정의합니다. 각 프로그래밍 언어마다 다양한 자료형을 제공하며, 일반적으로 기본 자료형(Primitive data types)과 참조 자료형(Reference data types)으로 구분됩니다.

<h2>1. 기본 자료형(Primitive data types)</h2>
가장 기본적인 데이터 타입으로, 정수, 실수, 문자, 논리형 등이 포함됩니다. <br><br>
<h3>1-1. 정수형(Integer)</h3>
정수를 저장하는 자료형입니다.

```python
num = 42
print(num)  # 출력: 42
```

<h3>1-2. 실수형(Float)</h3>
소수점을 포함한 실수 값을 저장하는 자료형입니다.

```python
pi = 3.14
print(pi)  # 출력: 3.14
```

<h3>1-3. 문자열(String)</h3>
문자의 나열로 구성된 데이터를 저장하는 자료형입니다.

```python
text = "Hello, Python!"
print(text)  # 출력: Hello, Python!

```

<h3>1-4. 논리형(Boolean)</h3>
참(True) 또는 거짓(False)의 값을 저장하는 자료형입니다.

```python
is_true = True
print(is_true)  # 출력: True

```
<h2>2. 참조 자료형(Reference data types)</h2>
기본 자료형을 기반으로 만들어진 복합 데이터 타입으로, 배열, 리스트, 튜플, 딕셔너리, 집합 등이 포함됩니다.
<h3>2-1. 튜플(Tuple)</h3>
리스트와 유사하지만 변경 불가능한(immutable) 순차적인 데이터를 저장하는 자료형입니다. 여러 개의 데이터를 저장할 수 있으며, 중복된 값이나 다른 자료형의 데이터도 저장할 수 있습니다.

```python
my_tuple = (1, 2, 3, 4, 5)
print(my_tuple)  # 출력: (1, 2, 3, 4, 5)
```

<h3>2-2. 집합(Set)</h3>
중복을 허용하지 않고, 순서가 없는 데이터를 저장하는 자료형입니다. 기본적으로 수학적 집합 연산을 지원합니다(교집합, 합집합, 차집합 등).

```python
my_set = {1, 2, 3, 4, 5}
print(my_set)  # 출력: {1, 2, 3, 4, 5}
```

<h3>2-3. 딕셔너리(Dictionary)</h3>
키(Key)와 값(Value) 쌍으로 이루어진 데이터를 저장하는 자료형입니다. 키를 이용하여 값을 빠르게 검색할 수 있습니다.

```python
my_dict = {"apple": 3, "banana": 5, "orange": 2}
print(my_dict)  # 출력: {'apple': 3, 'banana': 5, 'orange': 2}

```

이러한 자료형들을 이용하여 파이썬 프로그래밍에서 다양한 데이터를 저장하고 처리할 수 있습니다. 이 외에도 파이썬에서는 사용자 정의 자료형을 클래스를 통해 만들어 사용할 수도 있습니다.
