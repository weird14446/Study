<h1>Search Algorithm</h1>
탐색 알고리즘(Search Algorithm)은 데이터 집합에서 원하는 값을 찾기 위한 알고리즘입니다. 여기 대표적인 탐색 알고리즘과 이를 Python 코드로 구현한 예시를 제공합니다.

<h2>선형 탐색(Linear Search)</h2>
데이터 집합의 처음부터 끝까지 차례대로 원하는 값을 찾는 가장 단순한 탐색 알고리즘입니다. 시간 복잡도는 O(n)입니다.

```python
def linear_search(arr, target):
    for i, value in enumerate(arr):
        if value == target:
            return i
    return -1

```

<h2>이진 탐색(Binary Search)</h2>
정렬된 데이터 집합에서 효율적으로 원하는 값을 찾는 탐색 알고리즘입니다. 중간 값을 기준으로 탐색 범위를 절반씩 줄여나가며 원하는 값을 찾습니다. 시간 복잡도는 O(log(n))입니다.
<ul>
<li>반복문을 사용한 이진 탐색:

```python
def binary_search_iterative(arr, target):
    left, right = 0, len(arr) - 1

    while left <= right:
        mid = (left + right) // 2
        mid_value = arr[mid]

        if mid_value == target:
            return mid
        elif mid_value < target:
            left = mid + 1
        else:
            right = mid - 1

    return -1

```

<li>재귀 함수를 사용한 이진 탐색:

```python

def binary_search_recursive(arr, target, left, right):
    if left > right:
        return -1

    mid = (left + right) // 2
    mid_value = arr[mid]

    if mid_value == target:
        return mid
    elif mid_value < target:
        return binary_search_recursive(arr, target, mid + 1, right)
    else:
        return binary_search_recursive(arr, target, left, mid - 1)

```
</ul>

이 외에도 해시 테이블(Hash Table)을 사용한 탐색, 그래프 탐색 알고리즘(깊이 우선 탐색: DFS, 너비 우선 탐색: BFS) 등 다양한 탐색 알고리즘이 있습니다. 상황과 데이터의 특성에 따라 적절한 탐색 알고리즘을 선택하여 사용해야 합니다.
