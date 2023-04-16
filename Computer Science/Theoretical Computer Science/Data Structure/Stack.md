# Stack

스택(Stack)은 컴퓨터 과학에서 사용되는 추상적인 자료 구조입니다. 스택은 데이터를 저장하고 접근하는 순서가 후입선출(LIFO, Last In First Out) 방식을 따릅니다. 즉, 가장 마지막에 들어간 데이터가 가장 먼저 나오게 되는 구조를 가집니다.

스택은 두 가지 주요 연산을 지원합니다.

1. Push: 스택의 맨 위에 새로운 데이터를 추가합니다.
2. Pop: 스택의 맨 위에 있는 데이터를 제거하고 반환합니다.

스택은 다양한 프로그래밍 상황에서 사용됩니다. 예를 들어, 함수 호출과 실행을 관리하는데 사용되는 프로그램의 "호출 스택(Call Stack)"은 스택 자료 구조의 한 예입니다. 또한, 괄호 짝 맞추기, 문자열 역순 출력, 수식의 후위 표기법 변환 등 다양한 알고리즘 문제를 해결하는 데에도 스택이 사용됩니다.

스택은 배열이나 연결 리스트와 같은 기본 자료 구조를 이용하여 구현할 수 있으며, 각각의 구현 방법에 따라 성능과 메모리 사용 특성이 달라질 수 있습니다.

파이썬에서 스택을 사용하려면, 기본적으로 제공되는 리스트(List) 자료형을 활용할 수 있습니다. 리스트는 동적 배열로 구현되어 있어서 스택의 Push와 Pop 연산을 효율적으로 지원합니다. 아래는 파이썬에서 리스트를 이용하여 스택을 구현하는 예입니다.

```python

stack = []

# 스택에 데이터를 추가 (Push)
stack.append(1)
stack.append(2)
stack.append(3)
print(stack)  # 출력: [1, 2, 3]

# 스택에서 데이터를 제거하고 반환 (Pop)
last_element = stack.pop()
print(last_element)  # 출력: 3
print(stack)  # 출력: [1, 2]

```

위 예제에서, **`append`** 메서드를 사용하여 스택에 데이터를 추가(Push)하고, **`pop`** 메서드를 사용하여 스택의 맨 위에 있는 데이터를 제거하고 반환(Pop)합니다.

하지만 파이썬의 리스트를 스택으로 사용할 때 주의할 점은, 리스트의 앞쪽에서 데이터를 추가하거나 제거하면 성능이 저하되기 때문에, 항상 리스트의 뒷쪽에서 Push와 Pop 연산을 수행해야 한다는 것입니다. 이렇게 하면 상수 시간에(즉, O(1) 복잡도로) 데이터를 추가하거나 제거할 수 있습니다.

## 수학적 정의


<img src="https://i.upmath.me/svg/%5C%5B%5Cbegin%7Btikzcd%7D%0A%09%5Ctextcolor%7Bwhite%7D%7BS_A%5Cotimes%20A%7D%20%26%26%20%5Ctextcolor%7Bwhite%7D%7BS_A%5Cotimes%20A%2BI%7D%20%5C%5C%0A%09%26%20%5Ctextcolor%7Bwhite%7D%7BS_A%7D%20%26%26%20%5Ctextcolor%7Bwhite%7D%7BS_A%2BI%7D%0A%09%5Carrow%5B%22%7Bpush_A%7D%22'%2C%20color%3Dwhite%2C%20from%3D1-1%2C%20to%3D2-2%5D%0A%09%5Carrow%5B%22%7Bpop_A%7D%22'%2C%20color%3Dwhite%2C%20from%3D2-2%2C%20to%3D1-3%5D%0A%09%5Carrow%5B%22%7Bpush_A%2Bid_I%7D%22%2C%20color%3Dwhite%2C%20from%3D1-3%2C%20to%3D2-4%5D%0A%09%5Carrow%5B%22%7B%5Ciota_%7BS_A%5Cotimes%20A%2CI%7D%7D%22%2C%20color%3Dwhite%2C%20from%3D1-1%2C%20to%3D1-3%5D%0A%09%5Carrow%5B%22%7B%5Ciota_%7BS_A%5Cotimes%20A%2CI%7D%7D%22'%2C%20color%3Dwhite%2C%20from%3D2-2%2C%20to%3D2-4%5D%0A%5Cend%7Btikzcd%7D%5C%5D" alt="\[\begin{tikzcd}
	\textcolor{white}{S_A\otimes A} &amp;&amp; \textcolor{white}{S_A\otimes A+I} \\
	&amp; \textcolor{white}{S_A} &amp;&amp; \textcolor{white}{S_A+I}
	\arrow[&quot;{push_A}&quot;', color=white, from=1-1, to=2-2]
	\arrow[&quot;{pop_A}&quot;', color=white, from=2-2, to=1-3]
	\arrow[&quot;{push_A+id_I}&quot;, color=white, from=1-3, to=2-4]
	\arrow[&quot;{\iota_{S_A\otimes A,I}}&quot;, color=white, from=1-1, to=1-3]
	\arrow[&quot;{\iota_{S_A\otimes A,I}}&quot;', color=white, from=2-2, to=2-4]
\end{tikzcd}\]" />


위 이미지와 같이 범주론의 맥락에서 스택을 정의할 수 있습니다.


$$
push_A:S_A\otimes A\rightarrow S_A
$$


$$
pop_A:S_A→S_A⊗A+I
$$

위 두 사상은 각각 push 함수와 pop 함수를 의미합니다.
