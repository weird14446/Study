<h1>List</h1>

리스트는 다양한 프로그래밍 언어에서 사용되는 동적 배열(dynamic array)과 유사한 개념으로, 여러 가지 특징을 갖고 있습니다. 일반적인 리스트의 특징은 다음과 같습니다.

1. 순서가 있음: 리스트의 원소들은 순서가 있으며, 인덱스를 통해 특정 위치의 원소에 접근할 수 있습니다.
2. 가변성(mutable): 리스트의 원소는 변경이 가능합니다. 즉, 새로운 원소를 추가하거나 삭제하거나 기존 원소를 수정할 수 있습니다.
3. 중복 허용: 리스트는 동일한 값의 원소를 여러 개 포함할 수 있습니다.
4. 동적 크기: 리스트의 크기는 동적으로 변경될 수 있습니다. 원소를 추가하거나 삭제할 때, 리스트의 크기는 자동으로 조절됩니다.
5. 다양한 데이터 타입: 대부분의 프로그래밍 언어에서 리스트는 여러 가지 데이터 타입의 원소를 동시에 저장할 수 있습니다. 예를 들어, 파이썬에서는 정수, 실수, 문자열, 다른 리스트 등을 한 리스트에 저장할 수 있습니다.
6. 연산 지원: 리스트는 여러 가지 연산을 지원합니다. 일반적으로 원소의 추가, 삭제, 조회, 수정, 크기 확인 등의 연산이 지원됩니다. 또한 일부 프로그래밍 언어에서는 슬라이싱, 정렬, 역순, 합치기 등의 추가적인 연산도 지원할 수 있습니다.

리스트는 이러한 특징 덕분에 데이터를 저장하고 처리할 때 유용하게 사용되며, 다양한 알고리즘과 프로그램에서 활용됩니다.

파이썬에서 리스트는 매우 유용한 자료구조로, 다양한 기능을 제공합니다. 리스트를 생성하고 조작하는 방법에 대해 간단한 예제를 통해 설명하겠습니다.

1. 리스트 생성:
파이썬에서 리스트를 생성하려면 대괄호([])를 사용하거나 **`list()`** 함수를 사용할 수 있습니다. 예를 들어:

```python

empty_list = []
number_list = [1, 2, 3, 4, 5]
mixed_list = [1, "apple", 3.14, [6, 7, 8]]

```

2. 리스트 원소에 접근:
인덱스를 사용하여 리스트의 원소에 접근할 수 있습니다. 인덱스는 0부터 시작합니다.

```python
number_list = [1, 2, 3, 4, 5]
print(number_list[0])  # 출력: 1
print(number_list[2])  # 출력: 3

```

3. 리스트 슬라이싱:
리스트의 일부분을 선택하려면 슬라이싱을 사용할 수 있습니다.

```python

number_list = [1, 2, 3, 4, 5]
print(number_list[1:4])  # 출력: [2, 3, 4]

```

4. 리스트에 원소 추가:
리스트에 원소를 추가하려면 **`append()`** 메서드를 사용합니다.

```python

number_list = [1, 2, 3, 4, 5]
number_list.append(6)
print(number_list)  # 출력: [1, 2, 3, 4, 5, 6]

```

5. 리스트에서 원소 삭제:
리스트에서 원소를 삭제하려면 **`remove()`** 메서드를 사용하거나 **`del`** 키워드를 사용할 수 있습니다.

```python

number_list = [1, 2, 3, 4, 5]
number_list.remove(3)
print(number_list)  # 출력: [1, 2, 4, 5]

del number_list[1]
print(number_list)  # 출력: [1, 4, 5]

```

6. 리스트 크기 확인:
리스트의 크기를 확인하려면 **`len()`** 함수를 사용합니다.

```python

number_list = [1, 2, 3, 4, 5]
print(len(number_list))  # 출력: 5

```

7. 리스트 정렬:
리스트를 정렬하려면 **`sort()`** 메서드를 사용하거나 **`sorted()`** 함수를 사용할 수 있습니다.

```python

number_list = [5, 3, 1, 4, 2]
number_list.sort()
print(number_list)  # 출력: [1, 2, 3, 4, 5]

number_list = [5, 3, 1, 4, 2]
sorted_list = sorted(number_list)
print(sorted_list)  # 출력: [1, 2, 3, 4, 5]

```

8. 리스트 뒤집기:
리스트의 원소를 역순으로 뒤집으려면 **`reverse()`** 메서드를 사용할 수 있습니다.

```python

number_list = [1, 2, 3, 4, 5]
number_list.reverse()
print(number_list)  # 출력: [5, 4, 3, 2, 1]

```

9. 리스트에서 원소의 인덱스 찾기:
특정 원소의 인덱스를 찾으려면 **`index()`** 메서드를 사용합니다.

```python

number_list = [1, 2, 3, 4, 5]
index_of_3 = number_list.index(3)
print(index_of_3)  # 출력: 2

```

10. 리스트에서 특정 값의 개수 세기:
리스트 내에서 특정 값이 몇 개 있는지 세려면 **`count()`** 메서드를 사용합니다.

```python

number_list = [1, 2, 2, 3, 4, 4, 4, 5, 5]
count_of_4 = number_list.count(4)
print(count_of_4)  # 출력: 3

```

11. 리스트 확장하기:
한 리스트의 모든 원소를 다른 리스트에 추가하려면 **`extend()`** 메서드를 사용합니다.

```python

list1 = [1, 2, 3]
list2 = [4, 5, 6]
list1.extend(list2)
print(list1)  # 출력: [1, 2, 3, 4, 5, 6]

```

12. 리스트 결합하기:
두 리스트를 결합하여 새로운 리스트를 만들려면 **`+`** 연산자를 사용할 수 있습니다.

```python

list1 = [1, 2, 3]
list2 = [4, 5, 6]
combined_list = list1 + list2
print(combined_list)  # 출력: [1, 2, 3, 4, 5, 6]

```

이러한 기능들은 파이썬의 리스트를 유연하고 강력한 자료구조로 만들어주며, 다양한 상황에서 데이터를 저장하고 처리하는 데 도움이 됩니다.

<h1>수학적 정의</h1>
리스트 L은 다음 두 성질을 만족하는 자료구조입니다.


<img src="https://i.upmath.me/svg/%0A%5C%5B%5Cbegin%7Btikzcd%7D%0A%09%5Ctextcolor%7Bwhite%7D%7BL_A%5Cotimes%20A%7D%20%26%26%20%5Ctextcolor%7Bwhite%7D%7BL_A%5Cotimes%20A%2BI%7D%20%5C%5C%0A%09%26%20%5Ctextcolor%7Bwhite%7D%7BL_A%7D%20%26%26%20%5Ctextcolor%7Bwhite%7D%7BL_A%2BI%7D%0A%09%5Carrow%5B%22%7Bappend_A%7D%22'%2C%20color%3Dwhite%2C%20from%3D1-1%2C%20to%3D2-2%5D%0A%09%5Carrow%5B%22%7Bremove_A%7D%22'%2C%20color%3Dwhite%2C%20from%3D2-2%2C%20to%3D1-3%5D%0A%09%5Carrow%5B%22%7Bappend_L%2BA%7D%22%2C%20color%3Dwhite%2C%20from%3D1-3%2C%20to%3D2-4%5D%0A%09%5Carrow%5B%22%7B%CE%B9_%7BL_A%5Cotimes%20A%2CI%7D%7D%22%2C%20color%3Dwhite%2C%20from%3D1-1%2C%20to%3D1-3%5D%0A%09%5Carrow%5B%22%7B%CE%B9_%7BL_A%5Cotimes%20A%2CI%7D%7D%22'%2C%20color%3Dwhite%2C%20from%3D2-2%2C%20to%3D2-4%5D%0A%5Cend%7Btikzcd%7D%5C%5D%0A" alt="
\[\begin{tikzcd}
	\textcolor{white}{L_A\otimes A} &amp;&amp; \textcolor{white}{L_A\otimes A+I} \\
	&amp; \textcolor{white}{L_A} &amp;&amp; \textcolor{white}{L_A+I}
	\arrow[&quot;{append_A}&quot;', color=white, from=1-1, to=2-2]
	\arrow[&quot;{remove_A}&quot;', color=white, from=2-2, to=1-3]
	\arrow[&quot;{append_L+A}&quot;, color=white, from=1-3, to=2-4]
	\arrow[&quot;{ι_{L_A\otimes A,I}}&quot;, color=white, from=1-1, to=1-3]
	\arrow[&quot;{ι_{L_A\otimes A,I}}&quot;', color=white, from=2-2, to=2-4]
\end{tikzcd}\]
" />

<img src="https://i.upmath.me/svg/%0A%5C%5B%5Cbegin%7Btikzcd%7D%0A%09%26%20%5Ctextcolor%7Bwhite%7D%7BL%7D%20%5C%5C%0A%09%5Ctextcolor%7Bwhite%7D%7BY%7D%20%26%20%5Ctextcolor%7Bwhite%7D%7BL_i%7D%0A%09%5Carrow%5B%22f%22%2C%20color%3Dwhite%2C%20dashed%2C%20from%3D2-1%2C%20to%3D1-2%5D%0A%09%5Carrow%5B%22%7B%5Cpi%20_i%7D%22%2C%20color%3Dwhite%2C%20from%3D1-2%2C%20to%3D2-2%5D%0A%09%5Carrow%5B%22%7Bf_i%7D%22'%2C%20color%3Dwhite%2C%20from%3D2-1%2C%20to%3D2-2%5D%0A%5Cend%7Btikzcd%7D%5C%5D%0A" alt="
\[\begin{tikzcd}
	&amp; \textcolor{white}{L} \\
	\textcolor{white}{Y} &amp; \textcolor{white}{L_i}
	\arrow[&quot;f&quot;, color=white, dashed, from=2-1, to=1-2]
	\arrow[&quot;{\pi _i}&quot;, color=white, from=1-2, to=2-2]
	\arrow[&quot;{f_i}&quot;', color=white, from=2-1, to=2-2]
\end{tikzcd}\]
" />

여기서


$$
append_A:S_A\otimes A\rightarrow S_A
$$

$$
remove_A:S_A→S_A⊗A+I
$$

위 두 사상은 각각 append 함수와 remove 함수를 의미합니다.

L은 곱이라 부르며, 다음과 같습니다.

$$
L = ∏_{i∈I}L_i
$$

인덱싱은 다음과 같습니다.

$$
\pi _i:L \rightarrow L_i
$$

위 사상을 인덱싱으로 볼 수 있으며, 다음과 같습니다.

$$
\pi_i\(L) = L[i]
$$
