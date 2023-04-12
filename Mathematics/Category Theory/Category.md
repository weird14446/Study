# Category

범주론에서 범주(category)는 수학적 구조를 추상화한 개념입니다. 범주는 다음 두 가지 구성 요소로 이루어져 있습니다.

객체(Object): 범주의 기본 구성 요소로, 대부분의 경우 수학적 대상을 나타냅니다. 예를 들어 집합의 범주에서 객체는 집합 자체가 되고, 벡터 공간의 범주에서 객체는 벡터 공간입니다.
화살표(Arrow) 또는 변환(Morphism): 객체 간의 관계를 나타내는 화살표입니다. 화살표는 한 객체에서 다른 객체로 가는 맵핑이며, 종종 함수, 변환, 작용소 등의 개념으로 실현됩니다. 예를 들어 집합의 범주에서 화살표는 집합 간의 함수가 되고, 벡터 공간의 범주에서 화살표는 선형 변환입니다.
범주는 다음 세 가지 공리(법칙)를 충족해야 합니다.

합성(Composition)의 존재: 두 화살표가 연결되어 있으면(즉, 한 화살표의 공역이 다른 화살표의 정의역과 일치하면), 그 두 화살표의 합성이라는 새로운 화살표가 존재해야 합니다. 합성은 일반적으로 연속된 함수의 조합, 선형 변환의 합성 등으로 나타납니다.
합성의 결합법칙(Associativity): 세 개 이상의 화살표를 합성할 때, 어떤 순서로 합성을 하더라도 결과가 동일해야 합니다. 수학적으로, (f∘g)∘h = f∘(g∘h)이어야 합니다.
항등원(Identity)의 존재: 각 객체에 대해, 그 객체에서 자신으로 가는 항등 화살표가 존재해야 합니다. 이 항등 화살표는 다른 화살표와 합성될 때 항상 그 화살표 자체를 반환합니다. 즉, 항등 화살표는 합성의 항등원입니다.
범주론은 여러 수학적 구조와 작동 원리를 일반화하는 강력한 프레임워크로, 대수학, 위상수학, 기하학 등 수학의 여러 분야에서 중요한 도구로 사용됩니다.

<img src="https://i.upmath.me/svg/%5C%5B%5Cbegin%7Btikzcd%7D%0A%09%5Ctextcolor%7Bwhite%7D%7BX%7D%20%26%20%5Ctextcolor%7Bwhite%7D%7BY%7D%20%5C%5C%0A%09%26%20%5Ctextcolor%7Bwhite%7D%7BZ%7D%0A%09%5Carrow%5B%22f%22%2C%20color%3Dwhite%2C%20from%3D1-1%2C%20to%3D1-2%5D%0A%09%5Carrow%5B%22g%22%2C%20color%3Dwhite%2C%20from%3D1-2%2C%20to%3D2-2%5D%0A%09%5Carrow%5B%22%7Bg%5Ccirc%20f%7D%22'%2C%20color%3Dwhite%2C%20from%3D1-1%2C%20to%3D2-2%5D%0A%5Cend%7Btikzcd%7D%5C%5D" alt="\[\begin{tikzcd}
	\textcolor{white}{X} &amp; \textcolor{white}{Y} \\
	&amp; \textcolor{white}{Z}
	\arrow[&quot;f&quot;, color=white, from=1-1, to=1-2]
	\arrow[&quot;g&quot;, color=white, from=1-2, to=2-2]
	\arrow[&quot;{g\circ f}&quot;', color=white, from=1-1, to=2-2]
\end{tikzcd}\]" />
