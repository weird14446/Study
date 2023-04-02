<h1>함수형 프로그래밍</h1>
함수형 프로그래밍(functional programming)은 프로그래밍 패러다임 중 하나로, 함수와 불변성(immutability)에 초점을 맞춘 방식입니다. 함수형 프로그래밍은 수학적 함수의 개념에 기반하며, 부작용(side-effects)을 최소화하고, 데이터 변형을 피하고자 합니다. 이로 인해 함수형 프로그래밍은 병렬 처리와 같은 복잡한 시스템에서의 프로그램의 예측 가능성과 안정성을 높일 수 있습니다.

함수형 프로그래밍의 핵심 개념은 다음과 같습니다:
<h2>순수 함수(Pure functions)</h2>
순수 함수(pure function)는 프로그래밍에서 특정한 특성을 가진 함수입니다. 순수 함수는 다음과 같은 조건을 만족합니다:

입력에만 의존: 순수 함수는 외부 상태에 의존하지 않고 오직 입력 매개변수에만 의존하여 결과를 반환합니다.
부작용 없음: 순수 함수는 외부 상태를 변경하지 않고, 입력 값을 수정하지 않습니다.
동일한 입력에 대해 항상 동일한 결과: 주어진 입력에 대해 항상 같은 결과를 반환합니다.
Python에서 순수 함수의 예시를 살펴보겠습니다.

```py
def add(a, b):
    return a + b

def multiply(a, b):
    return a * b

result = add(3, 4)
result2 = multiply(result, 2)
```
위 예제에서 add와 multiply 함수는 순수 함수입니다. 이 함수들은 입력 매개변수에만 의존하고 외부 상태를 변경하지 않으며, 동일한 입력에 대해 항상 동일한 결과를 반환합니다.

비순수 함수의 예시를 살펴보겠습니다.
```py
counter = 0

def increment_counter():
    global counter
    counter += 1
    return counter
 ```
위 예제에서 increment_counter 함수는 비순수 함수입니다. 함수는 전역 변수 counter에 의존하고, 외부 상태를 변경합니다. 이로 인해 동일한 입력에 대해 항상 동일한 결과를 반환하지 않습니다.

순수 함수를 사용하면 프로그램의 예측 가능성과 안정성을 높일 수 있으며, 테스트와 디버깅이 쉬워집니다. 함수형 프로그래밍에서는 순수 함수를 사용하여 코드의 복잡성을 줄이고, 부작용을 최소화하려고 합니다.



<h2>불변성(Immutability)</h2>
불변성(Immutability)은 데이터의 상태가 한 번 생성된 후 변경되지 않는 특성을 말합니다. 함수형 프로그래밍에서는 불변성을 활용하여 예기치 않은 데이터 변경으로 인한 버그를 방지하고 프로그램의 예측 가능성을 높입니다.

Python에서 불변성을 지원하는 데이터 구조로 튜플(tuple)과 문자열(string)이 있습니다. 리스트와 달리 튜플은 변경이 불가능한 데이터 구조입니다.

예를 들어, 두 숫자를 더하는 함수를 생각해봅시다. 불변 데이터 구조인 튜플을 사용하여 결과를 반환하도록 작성할 수 있습니다.

```python
def add(a, b):
    return (a + b,)

result = add(3, 4)
```
위 예제에서 add 함수는 두 숫자를 더한 결과를 튜플로 반환합니다. 반환된 튜플은 불변이기 때문에 함수 외부에서 변경할 수 없습니다. 이렇게 불변성을 활용하면 프로그램의 복잡성을 줄일 수 있습니다.

다음 예제에서는 리스트를 사용한 경우와 불변성을 활용한 경우를 비교해보겠습니다.

```python
# 리스트를 사용한 경우
def add_value(lst, value):
    lst.append(value)
    return lst

my_list = [1, 2, 3]
new_list = add_value(my_list, 4)
print(my_list)  # [1, 2, 3, 4]
print(new_list)  # [1, 2, 3, 4]

# 불변성을 활용한 경우
def add_value_immutable(lst, value):
    return lst + (value,)

my_tuple = (1, 2, 3)
new_tuple = add_value_immutable(my_tuple, 4)
print(my_tuple)  # (1, 2, 3)
print(new_tuple)  # (1, 2, 3, 4)
```
리스트를 사용한 경우, add_value 함수는 입력 리스트에 값을 추가하여 외부 상태를 변경합니다. 반면 불변성을 활용한 경우, add_value_immutable 함수는 새로운 튜플을 반환하며 원래 튜플은 변경되지 않습니다. 이렇게 불변성을 유지하면 프로그램의 안정성을 높일 수 있습니다.
<h2>고차 함수(Higher-order functions)</h2>
고차 함수(higher-order function)는 다른 함수를 인자로 받거나, 함수를 반환하는 함수를 말합니다. 고차 함수는 함수를 값으로 취급하여 코드의 가독성을 높이고, 함수의 재사용성을 높이는 데 도움이 됩니다. Python에서는 고차 함수를 사용할 수 있습니다.

다음은 Python에서 고차 함수의 예시입니다:

함수를 인자로 받는 고차 함수:
```python
def apply(func, x, y):
    return func(x, y)

def add(a, b):
    return a + b

def multiply(a, b):
    return a * b

result1 = apply(add, 3, 4)       # 7
result2 = apply(multiply, 3, 4)  # 12
```
위 예제에서 apply 함수는 고차 함수로, 다른 함수 func를 인자로 받아 실행합니다. 이를 통해 add 함수와 multiply 함수를 동적으로 전달하고 실행할 수 있습니다.

함수를 반환하는 고차 함수:
```python
def make_adder(x):
    def add(y):
        return x + y
    return add

add5 = make_adder(5)
add10 = make_adder(10)

result1 = add5(3)   # 8
result2 = add10(3)  # 13
```
위 예제에서 make_adder 함수는 고차 함수로, 내부에 정의된 add 함수를 반환합니다. 이를 통해 add5와 add10처럼 동적으로 생성된 함수를 사용할 수 있습니다.

Python에서는 또한 map, filter, reduce와 같은 내장 고차 함수도 제공됩니다. 이 함수들은 함수를 인자로 받아 리스트나 이터러블에 대한 연산을 수행합니다.

예를 들어, map 함수는 다음과 같이 사용할 수 있습니다.

```python
def square(x):
    return x * x

numbers = [1, 2, 3, 4, 5]
squares = map(square, numbers)  # 결과: [1, 4, 9, 16, 25]
```
map 함수는 square 함수와 numbers 리스트를 인자로 받아 각 요소에 대해 제곱 연산을 수행하고 결과를 반환합니다. 이처럼 고차 함수를 활용하면 코드의 가독성과 모듈성을 높일 수 있습니다.
<h2>함수 합성(Function composition)</h2>
함수 합성(function composition)은 두 개 이상의 함수를 결합하여 새로운 함수를 만드는 과정입니다. 함수 합성을 사용하면 함수를 모듈화하여 코드의 가독성과 재사용성을 높일 수 있습니다.

수학에서, 두 함수 f(x)와 g(x)가 주어졌을 때, 함수 합성 h(x)는 다음과 같이 정의됩니다:

```
h(x) = (f ∘ g)(x) = f(g(x))
```
Python에서 함수 합성을 구현하려면, 두 개의 함수를 인자로 받아 새로운 함수를 반환하는 고차 함수를 정의할 수 있습니다.

예를 들어, 두 개의 함수를 합성하는 compose 함수를 다음과 같이 작성할 수 있습니다.

```python
def compose(f, g):
    def composed(x):
        return f(g(x))
    return composed

def double(x):
    return x * 2

def square(x):
    return x * x

double_then_square = compose(square, double)

result = double_then_square(3)  # 결과: 36
```
위 예제에서 compose 함수는 고차 함수로, 두 함수 f와 g를 인자로 받고, 합성된 함수 composed를 반환합니다. 이를 통해 double 함수와 square 함수를 합성한 새로운 함수 double_then_square를 생성할 수 있습니다.

이렇게 함수 합성을 활용하면 코드의 가독성을 높이고, 함수 간 연산의 결합을 명확하게 표현할 수 있습니다. 함수 합성은 함수형 프로그래밍에
<h2>지연 평가(Lazy evaluation)</h2>
지연 평가(lazy evaluation)는 식(expression)을 필요한 시점에 평가하는 프로그래밍 기법입니다. 이 방식은 불필요한 계산을 피하거나, 무한한 데이터 구조를 다루는 경우에 유용합니다. Python에서 지연 평가를 구현하는 대표적인 방법은 제너레이터(generator)를 사용하는 것입니다.

제너레이터는 yield 키워드를 사용하여 값을 생성하는 함수입니다. 제너레이터는 호출될 때 값을 즉시 계산하지 않고, 요청에 따라 값을 순차적으로 생성하며 이전 상태를 기억합니다.

예를 들어, 피보나치 수열을 생성하는 제너레이터를 작성해보겠습니다.

```python
def fibonacci():
    a, b = 0, 1
    while True:
        yield a
        a, b = b, a + b

fib = fibonacci()

# 처음 10개의 피보나치 수를 출력
for i, value in enumerate(fib):
    if i >= 10:
        break
    print(value)
```
위 예제에서 fibonacci 함수는 제너레이터로, yield를 사용하여 피보나치 수를 생성합니다. 이 함수는 값을 즉시 계산하지 않고, 필요한 시점에 값을 생성합니다. 따라서 무한한 피보나치 수열을 다루는 것도 가능합니다.

Python에서는 지연 평가를 적용한 map, filter와 같은 내장 함수도 제공됩니다. 이 함수들은 제너레이터를 반환하여 값의 생성을 지연시킵니다.

예를 들어, map 함수를 사용하여 제곱값을 생성하는 제너레이터를 만들 수 있습니다.

```python
def square(x):
    return x * x

numbers = [1, 2, 3, 4, 5]
squares = map(square, numbers)  # 제너레이터 생성

for square_value in squares:  # 필요한 시점에 값을 생성
    print(square_value)
```
이처럼 지연 평가를 활용하면 메모리 사용량을 줄이고, 계산 시간을 최적화할 수 있습니다. 함수형 프로그래밍에서는 지연 평가를 사용하여 효율적인 코드를 작성하는 것이 중요한 개념 중 하나입니다.
<hr>
함수형 프로그래밍은 Haskell, Lisp, Erlang, Scala, F# 등의 언어에서 주로 사용되지만, 다른 프로그래밍 언어에서도 함수형 프로그래밍의 개념을 적용할 수 있습니다.
