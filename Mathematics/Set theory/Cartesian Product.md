곱집합(Cartesian product)은 집합 이론에서 두 집합의 모든 가능한 순서쌍을 포함하는 새로운 집합을 구성하는 연산입니다. 두 집합 A와 B의 곱집합은 A × B로 표현되며, 결과 집합은 A의 각 원소와 B의 각 원소로 이루어진 순서쌍을 포함합니다.

곱집합의 정의는 다음과 같습니다:

A × B = {(a, b) | a ∈ A, b ∈ B}

순서쌍은 다음과 같이 정의됩니다.

(a, b)={{a},{a, b}}

예를 들어, 집합 A = {1, 2}와 집합 B = {a, b}의 곱집합을 구하면 다음과 같습니다:

A × B = {(1, a), (1, b), (2, a), (2, b)}

곱집합은 여러 집합에 대해 일반화될 수 있으며, n개의 집합의 곱집합은 n-tuple을 포함하는 집합이 됩니다.
n개의 집합의 곱집합의 정의는 다음과 같습니다.

$$
\prod _{i\in I}X_i= \begin{Bmatrix}
(x_i)_{i\in I}:\forall i\in I, \ x_i\in X_i \end{Bmatrix}
$$

곱집합은 여러 분야에서 중요한 개념으로 활용되며, 수학, 확률론, 이산수학, 그래프 이론 등에서 자주 사용됩니다.
<h2>관계</h2>
관계(relation)는 두 집합의 원소들 사이에 성립하는 일종의 규칙 또는 연결입니다. 보다 구체적으로는, 관계는 한 집합의 원소와 다른 집합의 원소를 순서쌍 형태로 묶어 주는 것입니다. 이 때, 관계는 그 집합들의 곱집합에서 얻어진 부분집합으로 표현됩니다.

$$
\prod _{i\in I}X_i= \begin{Bmatrix}
(x_i)_{i\in I}:\forall i\in I, \ x_i\in X_i \end{Bmatrix}
$$

$$
G \subset \prod _{i=1}^n X_i
$$

에서 관계 R은 (n+1)튜플

$$
R=(X_1,X_2,X_3,...,X_n,G)
$$

로 정의되며, G는 관계 R의 그래프라고 부릅니다.

순서쌍들의 관계(n=2일 때의 관계)에서

$$
(x,y)\in G
$$

인 경우

$$
xRy
$$

로 표현됩니다.

이항 관계에서 관계 R의 정의역은 다음과 같이 정의됩니다.

$$
Dom \ R = \begin{Bmatrix} x \in X : \exists y\in Y,\ xRy \in G \end{Bmatrix}
$$

치역은 다음과 같이 정의됩니다.

$$
Im \ R = \begin{Bmatrix} y \in Y : \exists x\in X,\ xRy \in G \end{Bmatrix}
$$

관계의 성질들은 다음과 같습니다.

1. 반사성

$$
\forall x \in X : xRx
$$

2. 대칭성

$$
\forall x, y\in X: xRy \rightarrow yRx
$$

3. 비대칭성

$$
\forall x, y \in X:xRy \rightarrow \neg yRx
$$

4. 반대칭성

$$
\forall x, y\in X:(xRy\land yRx)\rightarrow (x=y)
$$

5. 전이성

$$
\forall x, y, z\in X:(xRy\land yRz)\rightarrow (xRz)
$$

6. 동치관계 : R이 반사성, 대칭성, 전이성을 모두 만족시키는 경우에 성립합니다.
7. 부분순서관계 : R이 반사성, 반대칭성, 전이성을 모두 만족시키는 경우에 성립합니다.
