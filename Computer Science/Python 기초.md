<h1>Python 기초</h1>
지금까지 제가 배운 모든 알고리즘과 개념들은 파이썬 코드로 설명할 것이기 때문에, <br>
파이썬의 기초적인 사용법에 대해 간략하게 설명하겠습니다.
자세한 내용은 공식 문서를 참조해주시길 바랍니다. (https://docs.python.org/ko/3/)<br><br>

1. 출력: **`print()`** 함수를 사용하여 값을 출력할 수 있습니다.

```python
print("Hello, Python!")
```

1. 변수 할당: 변수에 값을 저장하려면 **`=`** 연산자를 사용합니다.

```python
x = 10
y = 20

```

1. 연산: 사칙연산 및 다양한 수학적 연산을 수행할 수 있습니다.

```python
result = x + y  # 덧셈
result = x - y  # 뺄셈
result = x * y  # 곱셈
result = x / y  # 나눗셈
result = x % y  # 나머지
result = x ** y  # 거듭제곱

```

1. 조건문: **`if`**, **`elif`**, **`else`** 키워드를 사용하여 조건에 따라 코드를 실행할 수 있습니다.

```python
x = 10

if x > 0:
    print("x is positive")
elif x < 0:
    print("x is negative")
else:
    print("x is zero")

```

1. 반복문: **`for`**와 **`while`** 루프를 사용하여 코드를 반복적으로 실행할 수 있습니다.

**`for`** 루프:

```python
for i in range(5):
    print(i)

```

**`while`** 루프:

```python
i = 0
while i < 5:
    print(i)
    i += 1

```

1. 함수: **`def`** 키워드를 사용하여 코드의 재사용성을 높일 수 있는 함수를 정의할 수 있습니다.

```python
def add(x, y):
    return x + y

result = add(10, 20)
print(result)  # 출력: 30

```

1. 모듈 임포트: 다양한 라이브러리나 사용자 정의 모듈을 **`import`** 키워드를 사용하여 가져올 수 있습니다.

```python
import math

result = math.sqrt(16)
print(result)  # 출력: 4.0

```

1. 클래스: 파이썬에서 클래스를 정의하는 기본 구조는 다음과 같습니다:

```python
class ClassName:
    def __init__(self, parameters):
        # 생성자 코드

    def method1(self, parameters):
        # 메서드1 코드

    def method2(self, parameters):
        # 메서드2 코드

```

예제로 간단한 **`Person`** 클래스를 만들어 보겠습니다.

```python
class Person:
    def __init__(self, name, age):
        self.name = name
        self.age = age

    def say_hello(self):
        print(f"Hello, my name is {self.name} and I am {self.age} years old.")

    def celebrate_birthday(self):
        self.age += 1
        print(f"Happy birthday! Now, I am {self.age} years old.")

```

위 예제에서 **`Person`** 클래스는 **`__init__`**, **`say_hello`**, **`celebrate_birthday`** 세 가지 메서드를 가지고 있습니다. **`__init__`** 메서드는 클래스의 생성자로 객체가 생성될 때 자동으로 호출됩니다. **`self`** 매개변수는 객체 자신을 참조하며, 클래스 내의 메서드에서는 첫 번째 매개변수로 **`self`**를 사용해야 합니다.

**`Person`** 클래스를 사용해 객체를 생성하고 메서드를 호출하는 방법은 다음과 같습니다.

```python
# 객체 생성
person1 = Person("Alice", 30)
person2 = Person("Bob", 25)

# 메서드 호출
person1.say_hello()  # 출력: Hello, my name is Alice and I am 30 years old.
person2.say_hello()  # 출력: Hello, my name is Bob and I am 25 years old.

person1.celebrate_birthday()  # 출력: Happy birthday! Now, I am 31 years old.

```

이렇게 클래스를 사용하면 관련된 데이터와 기능을 묶어 코드의 재사용성과 가독성을 높일 수 있습니다.
