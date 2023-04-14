<h1>BFS Algorithm</h1>
너비 우선 탐색(Breadth-First Search, BFS)은 그래프 탐색 알고리즘 중 하나로, 시작 정점에서 출발하여 가까운 정점부터 차례대로 방문하는 알고리즘입니다. BFS는 레벨(Level)별로 그래프의 모든 정점을 방문하며, 큐(Queue)를 사용하여 방문할 정점을 저장하고 처리합니다.

BFS 알고리즘의 동작 과정은 다음과 같습니다.

1. 시작 정점을 큐에 넣고, 방문 처리를 합니다.
2. 큐에서 정점을 꺼냅니다. (큐에서 꺼낸 정점을 현재 정점으로 간주합니다.)
3. 현재 정점의 인접 정점들을 확인합니다.
    - 인접 정점이 방문하지 않은 상태라면, 해당 정점을 큐에 넣고 방문 처리합니다.
4. 큐가 빌 때까지 2~3 단계를 반복합니다.

아래에는 Python으로 구현한 BFS 알고리즘 예시가 있습니다.

```python
from collections import deque

graph = {
    'A': ['B', 'C'],
    'B': ['A', 'D', 'E'],
    'C': ['A', 'F'],
    'D': ['B'],
    'E': ['B', 'F'],
    'F': ['C', 'E']
}

visited = set()

def bfs(graph, start, visited):
    queue = deque([start])

    while queue:
        node = queue.popleft()
        if node not in visited:
            print(node, end=' ')
            visited.add(node)
            queue.extend(neighbor for neighbor in graph[node])

bfs(graph, 'A', visited)

```

위 코드에서는 그래프를 딕셔너리로 표현하였으며, **`visited`** 집합을 사용하여 방문한 정점을 기록합니다. 큐에 정점을 추가하고, 방문할 정점이 없을 때까지 큐에서 정점을 꺼내 인접한 정점들을 확인하고 방문합니다. 이렇게 BFS를 사용하면 시작 정점으로부터 가장 가까운 정점부터 순서대로 방문하게 됩니다.
