# Asymptotic Notation

점근 표기법(asymptotic notation)은 컴퓨터 과학에서 알고리즘의 효율성을 설명하기 위해 사용되는 방법입니다. 알고리즘의 성능을 평가할 때 입력 크기가 무한대로 커지는 상황에서 알고리즘의 복잡도를 표현하기 위해 점근 표기법을 사용합니다. 점근 표기법에는 주로 다음 세 가지가 있습니다.

O-표기법 (Big O notation): 알고리즘의 최악의 경우 복잡도를 표현합니다. O-표기법은 알고리즘의 성능의 상한선(upper bound)을 나타내며, O(f(n))은 입력 크기 n에 대한 함수 f(n)의 상한선을 의미합니다. 예를 들어, O(n)은 선형 시간 복잡도를 나타내고, O(n^2)은 이차 시간 복잡도를 나타냅니다.

Ω-표기법 (Big Omega notation): 알고리즘의 최선의 경우 복잡도를 표현합니다. Ω-표기법은 알고리즘의 성능의 하한선(lower bound)을 나타내며, Ω(f(n))은 입력 크기 n에 대한 함수 f(n)의 하한선을 의미합니다. 예를 들어, Ω(n)은 알고리즘이 최선의 경우에도 선형 시간이 걸린다는 것을 나타냅니다.

Θ-표기법 (Big Theta notation): 알고리즘의 평균적인 경우 복잡도를 표현합니다. Θ-표기법은 알고리즘의 성능의 하한선과 상한선 사이를 나타내며, Θ(f(n))은 입력 크기 n에 대한 함수 f(n)의 평균적인 복잡도를 의미합니다. 예를 들어, Θ(n^2)은 알고리즘이 평균적으로 이차 시간 복잡도를 가진다는 것을 나타냅니다.

점근 표기법은 알고리즘의 복잡도를 쉽게 비교할 수 있게 해주며, 알고리즘의 성능을 평가하는 데 중요한 도구입니다. 이를 통해 프로그래머들은 입력 크기가 커질 때 알고리즘이 어떻게 작동할지 예측하고, 효율적인 코드를 작성할 수 있습니다.

## 수학적 정의

위에서 설명한 표기법들과 다른 표기법들은 다음과 같이 정의됩니다.

$$
f(n)\in O(g(n)) \Leftrightarrow \lim _{n\rightarrow \infty}\left\vert \frac{f(n)}{g(n)} \right\vert < \infty
$$

$$
f(n)\in o(g(n))\Leftrightarrow \lim_{n\rightarrow \infty}\frac{f(n)}{g(n)}=0
$$

$$
f(n)\in \Omega (g(n)) \Leftrightarrow \lim _{n\rightarrow \infty} \left\vert \frac{f(n)}{g(n)} \right\vert>0
$$

$$
f(n)\in \omega (g(n)) \Leftrightarrow \lim_{n\rightarrow \infty}\frac{f(n)}{g(n)}=\infty
$$

$$
f(n)\in \Theta(g(n)) \Leftrightarrow 0 < \lim_{n\rightarrow \infty}\left\vert \frac{f(n)}{g(n)} \right\vert < \infty
$$
