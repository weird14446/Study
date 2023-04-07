<h1>Queue</h1>
큐(Queue) 자료구조는 컴퓨터 과학에서 매우 유용한 선형 자료구조입니다. 큐는 가장 먼저 들어온 항목이 가장 먼저 나오는 (FIFO, First In First Out) 원칙을 따릅니다. 큐에는 주로 두 가지 주요 작업이 있습니다: 삽입(Enqueue)과 삭제(Dequeue).
<h2>리스트를 사용한 큐 구현</h2>
리스트를 사용하여 큐를 구현하려면 다음과 같이 간단한 클래스를 작성할 수 있습니다. enqueue 메서드를 사용하여 항목을 추가하고, dequeue 메서드를 사용하여 항목을 제거합니다. 이 방법은 간단하고 이해하기 쉽지만, 큐의 크기가 커질수록 성능이 떨어질 수 있습니다.

```python
class Queue:
    def __init__(self):
        self.items = []

    def is_empty(self):
        return len(self.items) == 0

    def enqueue(self, item):
        self.items.append(item)

    def dequeue(self):
        if self.is_empty():
            raise Exception("Queue is empty!")
        return self.items.pop(0)

    def size(self):
        return len(self.items)
 ```
 <h2>queue 모듈을 사용한 구현</h2>
 Python의 queue 모듈을 사용하여 큐를 구현하는 것은 매우 간단합니다. Queue 클래스를 사용하여 새로운 큐 객체를 생성하고, put() 메서드로 항목을 추가(Enqueue)하며, get() 메서드로 항목을 제거(Dequeue)할 수 있습니다.

다음은 queue 모듈을 사용한 예제입니다:

```python
import queue

# 큐 객체 생성
my_queue = queue.Queue()

# 항목 추가 (Enqueue)
my_queue.put("Apple")
my_queue.put("Banana")
my_queue.put("Cherry")

# 항목 제거 (Dequeue)
first_item = my_queue.get()
print("First item:", first_item)  # Output: First item: Apple

# 큐의 크기 확인
queue_size = my_queue.qsize()
print("Queue size:", queue_size)  # Output: Queue size: 2
```
이 방법은 리스트를 사용하는 것보다 더 효율적이며, 스레드 간 동기화를 지원하기 때문에 다중 스레드 환경에서도 사용할 수 있습니다.

<h2>수학적 엄밀화</h2>
