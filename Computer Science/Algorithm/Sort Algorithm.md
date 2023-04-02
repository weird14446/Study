<h1>정렬 알고리즘</h1>
정렬 알고리즘(Sorting Algorithm)이란 데이터를 일정한 순서(오름차순, 내림차순 등)로 정렬하는 과정을 수행하는 알고리즘입니다. 정렬 알고리즘은 데이터 분석, 검색, 처리 등 다양한 애플리케이션에서 필수적으로 사용되며, 여러 가지 종류의 정렬 알고리즘이 있습니다.
<h2>버블 정렬(Bubble Sort)</h2>
인접한 두 원소를 비교하여 큰 값을 오른쪽으로 이동시키는 과정을 반복하여 정렬하는 알고리즘입니다. 시간 복잡도는 O(n^2)입니다.

```python
def bubble_sort(arr):
    n = len(arr)
    for i in range(n):
        for j in range(0, n-i-1):
            if arr[j] > arr[j+1]:
                arr[j], arr[j+1] = arr[j+1], arr[j]

```

<h2>선택 정렬(Selection Sort)</h2>
리스트에서 최솟값을 찾아 맨 앞에 위치한 값과 교환하는 과정을 반복하여 정렬하는 알고리즘입니다. 시간 복잡도는 O(n^2)입니다.

```python
def selection_sort(arr):
    n = len(arr)
    for i in range(n):
        min_idx = i
        for j in range(i+1, n):
            if arr[j] < arr[min_idx]:
                min_idx = j
        arr[i], arr[min_idx] = arr[min_idx], arr[i]

```

<h2>삽입 정렬(Insertion Sort)</h2>
정렬된 부분과 정렬되지 않은 부분으로 나누고, 정렬되지 않은 부분의 첫 번째 원소를 정렬된 부분에 적절한 위치에 삽입하는 과정을 반복하여 정렬하는 알고리즘입니다. 시간 복잡도는 O(n^2)입니다.

```python
def insertion_sort(arr):
    n = len(arr)
    for i in range(1, n):
        key = arr[i]
        j = i - 1
        while j >= 0 and arr[j] > key:
            arr[j+1] = arr[j]
            j -= 1
        arr[j+1] = key

```

<h2>퀵 정렬(Quick Sort)</h2>
피벗(pivot)을 선택하고 피벗보다 작은 값은 왼쪽으로, 큰 값은 오른쪽으로 분할한 후 각 영역에 대해 재귀적으로 정렬하는 알고리즘입니다. 평균 시간 복잡도는 O(n*log(n))이지만, 최악의 경우 시간 복잡도는 O(n^2)입니다.

```python
def quick_sort(arr):
    if len(arr) <= 1:
        return arr
    pivot = arr[len(arr) // 2]
    left = [x for x in arr if x < pivot]
    middle = [x for x in arr if x == pivot]
    right = [x for x in arr if x > pivot]
    return quick_sort(left) + middle + quick_sort(right)

```
<h2>병합 정렬(Merge Sort)</h2>
리스트를 반으로 나누어 정렬된 두 부분을 합병하는 과정을 재귀적으로 반복하여 정렬하는 알고리즘입니다. 시간 복잡도는 O(n*log(n))입니다.

```python
def merge_sort(arr):
    if len(arr) <= 1:
        return arr

    mid = len(arr) // 2
    left = arr[:mid]
    right = arr[mid:]

    left = merge_sort(left)
    right = merge_sort(right)

    return merge(left, right)

def merge(left, right):
    result = []
    i = j = 0

    while i < len(left) and j < len(right):
        if left[i] < right[j]:
            result.append(left[i])
            i += 1
        else:
            result.append(right[j])
            j += 1

    result.extend(left[i:])
    result.extend(right[j:])

    return result

```

병합 정렬은 입력 리스트를 반으로 나누어 각 부분을 재귀적으로 정렬하고, 정렬된 두 부분을 병합하는 과정을 통해 정렬됩니다. 병합 과정에서 두 부분 리스트의 원소를 순서대로 비교하며 결과 리스트에 추가합니다. 병합 정렬은 안정 정렬(Stable Sort)이며, 분할 정복(Divide and Conquer) 전략을 사용한 정렬 알고리즘입니다.
<hr>
각 정렬 알고리즘은 특징과 성능이 다르기 때문에, 상황에 따라 적절한 정렬 알고리즘을 선택하여 사용해야 합니다. 이 외에도 힙 정렬(Heap Sort), 기수 정렬(Radix Sort), 쉘 정렬(Shell Sort) 등 다양한 정렬 알고리즘이 있습니다.
