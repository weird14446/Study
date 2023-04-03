<h1>Dijkstra Algorithm</h1>
다익스트라(Dijkstra) 알고리즘은 음이 아닌 가중치를 가진 그래프에서 시작 정점부터 다른 모든 정점까지의 최단 경로를 찾는 알고리즘입니다. 다익스트라 알고리즘은 우선순위 큐를 사용하여 그래프의 정점을 순회하며 최단 경로를 계산합니다.

다익스트라 알고리즘의 기본적인 동작 과정은 다음과 같습니다.
<ol>
<li>시작 정점의 거리를 0으로 초기화하고, 나머지 정점의 거리를 무한대로 초기화합니다.
<li>우선순위 큐에 시작 정점을 추가합니다.
<li>우선순위 큐에서 가장 거리가 짧은 정점을 꺼냅니다.
<li>꺼낸 정점의 인접 정점들의 거리를 갱신합니다. 이 때, 현재 정점을 거쳐서 가는 거리가 기존 거리보다 짧으면 거리 값을 갱신하고 우선순위 큐에 추가합니다.
<li>우선순위 큐가 빌 때까지 3~4 단계를 반복합니다.
</ol>
이렇게 다익스트라 알고리즘을 수행하면 시작 정점부터 다른 모든 정점까지의 최단 경로를 구할 수 있습니다.

다음은 파이썬으로 작성한 다익스트라 알고리즘 예제입니다.

```python
def dijkstra(graph, start):
    distances = {node: float('inf') for node in graph}
    distances[start] = 0
    queue = []

    heapq.heappush(queue, (0, start))

    while queue:
        current_distance, current_node = heapq.heappop(queue)

        if distances[current_node] < current_distance:
            continue

        for neighbor, weight in graph[current_node].items():
            distance = current_distance + weight

            if distance < distances[neighbor]:
                distances[neighbor] = distance
                heapq.heappush(queue, (distance, neighbor))

    return distances

graph = {
    'A': {'B': 1, 'C': 4},
    'B': {'A': 1, 'C': 2, 'D': 5, 'E': 8},
    'C': {'A': 4, 'B': 2, 'E': 1},
    'D': {'B': 5, 'E': 2},
    'E': {'B': 8, 'C': 1, 'D': 2}
}

print(dijkstra(graph, 'A'))

```

위 코드에서는 그래프를 딕셔너리로 표현하였으며, 시작 정점으로부터 다른 모든 정점까지의 최단 경로를 구합니다. 이를 위해 **`heapq`** 라이브러리를 사용하여 우선순위 큐를 구현하였습니다. 이 알고리즘은 시작 정점으로부터 가장 가까운 정점부터 순서대로 최단 경로를 계산하고, 우선순위 큐를 사용하여 방문하지 않은 정점 중 가장 거리가 짧은 정점을 선택합니다.
