<h1>First Order Logic</h1>
1차 술어 논리(First-order predicate logic, First-order logic, FOL)는 수학, 철학, 컴퓨터 과학 등에서 널리 사용되는 논리 체계입니다.

<h2>1. 명제 논리</h2>

명제 논리(Propositional Logic)는 참이나 거짓으로 판별할 수 있는 명제들 간의 논리적인 관계를 다루는 논리 체계입니다. 명제 논리는 논리 연산자를 사용하여 명제들을 결합하거나 변형하여 새로운 명제를 생성하는 방식으로 작동합니다. 명제 논리는 간단한 추론과 증명에 사용되며, 논리 회로 설계 및 컴퓨터 프로그래밍에서도 중요한 역할을 합니다.

<h3>1-1. 논리합</h3>

논리합(Disjunction)은 명제 논리에서 사용되는 논리 연산자 중 하나로, 두 명제 중 적어도 하나가 참일 때 결과 명제가 참이 되는 연산자입니다. 논리합은 기호 '∨'로 표현되며, "또는"이라는 의미를 가집니다.

예를 들어, 명제 P와 Q가 주어졌다고 가정해봅시다. 이때 논리합 P ∨ Q는 다음과 같은 조건을 나타냅니다.

1. P가 참이고 Q가 참일 때, P ∨ Q는 참입니다.
2. P가 참이고 Q가 거짓일 때, P ∨ Q는 참입니다.
3. P가 거짓이고 Q가 참일 때, P ∨ Q는 참입니다.
4. P가 거짓이고 Q가 거짓일 때, P ∨ Q는 거짓입니다.

즉, 논리합 연산은 두 명제 중 적어도 하나가 참이면 결과 명제가 참이 되며, 두 명제가 모두 거짓인 경우에만 결과 명제가 거짓이 됩니다.

<h3>1-2. 논리곱</h3>
 
논리곱(Conjunction)은 명제 논리에서 사용되는 논리 연산자 중 하나로, 두 명제가 모두 참일 때 결과 명제가 참이 되는 연산자입니다. 논리곱은 기호 '∧'로 표현되며, "그리고" 또는 "와"라는 의미를 가집니다.

예를 들어, 명제 P와 Q가 주어졌다고 가정해봅시다. 이때 논리곱 P ∧ Q는 다음과 같은 조건을 나타냅니다.

1. P가 참이고 Q가 참일 때, P ∧ Q는 참입니다.
2. P가 참이고 Q가 거짓일 때, P ∧ Q는 거짓입니다.
3. P가 거짓이고 Q가 참일 때, P ∧ Q는 거짓입니다.
4. P가 거짓이고 Q가 거짓일 때, P ∧ Q는 거짓입니다.

즉, 논리곱 연산은 두 명제가 모두 참인 경우에만 결과 명제가 참이 되며, 두 명제 중 하나라도 거짓인 경우 결과 명제가 거짓이 됩니다.
 
<h3>1-3. 부정</h3>

부정(Negation)은 명제 논리에서 사용되는 논리 연산자 중 하나로, 주어진 명제의 참과 거짓을 반대로 바꾸는 연산자입니다. 부정은 기호 '¬' 또는 '~'로 표현되며, "아니다" 또는 "그렇지 않다"라는 의미를 가집니다.

예를 들어, 명제 P가 "오늘은 비가 온다"라고 가정해봅시다. 이때 부정 ¬P는 "오늘은 비가 오지 않는다"를 의미합니다. 부정 연산은 다음과 같은 조건을 나타냅니다:

1. P가 참일 때, ¬P는 거짓입니다.
2. P가 거짓일 때, ¬P는 참입니다.

즉, 부정 연산은 주어진 명제의 진리값을 반전시키는 역할을 합니다.

<h3>1-4. 조건부</h3>

조건부(Conditional)는 명제 논리에서 사용되는 논리 연산자 중 하나로, 한 명제가 참일 때 다른 명제가 참이 되도록 하는 연산자입니다. 조건부는 기호 '→'로 표현되며, "만약 ...라면" 또는 "이면"이라는 의미를 가집니다.

예를 들어, 명제 P와 Q가 주어졌다고 가정해봅시다. 이때 조건부 P → Q는 다음과 같은 조건을 나타냅니다.

1. P가 참이고 Q가 참일 때, P → Q는 참입니다.
2. P가 참이고 Q가 거짓일 때, P → Q는 거짓입니다.
3. P가 거짓이고 Q가 참일 때, P → Q는 참입니다.
4. P가 거짓이고 Q가 거짓일 때, P → Q는 참입니다.

즉, 조건부 연산은 주어진 명제 P가 참이고 명제 Q가 거짓인 경우에만 결과 명제가 거짓이 되며, 나머지 경우에는 결과 명제가 참이 됩니다.

<h3>1-5. 이중 조건부</h3>

이중 조건부(Biconditional)는 명제 논리에서 사용되는 논리 연산자 중 하나로, 두 명제가 서로 참이거나 거짓일 때 결과 명제가 참이 되는 연산자입니다. 이중 조건부는 기호 '↔'로 표현됩니다.

예를 들어, 명제 P와 Q가 주어졌다고 가정해봅시다. 이때 이중 조건부 P ↔ Q는 다음과 같은 조건을 나타냅니다.

1. P가 참이고 Q가 참일 때, P ↔ Q는 참입니다.
2. P가 참이고 Q가 거짓일 때, P ↔ Q는 거짓입니다.
3. P가 거짓이고 Q가 참일 때, P ↔ Q는 거짓입니다.
4. P가 거짓이고 Q가 거짓일 때, P ↔ Q는 참입니다.

즉, 이중 조건부 연산은 두 명제가 동시에 참이거나 동시에 거짓인 경우에만 결과 명제가 참이 되며, 두 명제의 참과 거짓이 서로 다른 경우에는 결과 명제가 거짓이 됩니다.

<h3>1-6 명제 함수</h3>
명제 함수는 변수가 포함된 함수로서, 변수에 특정 값을 대입하면 그 결과가 참이거나 거짓인 값을 가지게 됩니다.

예를 들어, f(x) = "x는 짝수다"라는 명제 함수를 가정해봅시다. x에 특정 값을 대입하면 명제 함수의 결과는 참이거나 거짓이 됩니다. x가 4일 경우, f(4)는 "4는 짝수다"라는 명제가 되고, 이는 참입니다. 반면에, x가 3일 경우, f(3)은 "3은 짝수다"라는 명제가 되고, 이는 거짓입니다.

<h3>1-7. 항진 명제와 모순 명제</h3>

항진 명제(Tautology)는 명제 논리에서 항상 참인 명제를 의미합니다. 항진 명제는 논리 연산자와 명제 변수를 포함한 복합 명제 중, 명제 변수들의 모든 가능한 값에 대해 결과가 참이 되는 명제를 가리킵니다.

항진 명제의 예시는 다음과 같습니다.

1. P ∨ ¬P: 이 명제는 "P 또는 P가 아니다"라는 의미입니다. P가 참이든 거짓이든, 이 명제의 결과는 항상 참이 됩니다.
2. (P → Q) ∨ (Q → P): 이 명제는 "P가 Q를 함축하거나 Q가 P를 함축한다"라는 의미입니다. P와 Q의 모든 가능한 조합에 대해, 이 명제의 결과는 항상 참입니다.

모순 명제(Contradiction)는 명제 논리에서 항상 거짓인 명제를 의미합니다. 모순 명제는 논리 연산자와 명제 변수를 포함한 복합 명제 중, 명제 변수들의 모든 가능한 값에 대해 결과가 거짓이 되는 명제를 가리킵니다.

모순 명제의 예시는 다음과 같습니다.

1. P ∧ ¬P: 이 명제는 "P 그리고 P가 아니다"라는 의미입니다. P가 참이든 거짓이든, 이 명제의 결과는 항상 거짓이 됩니다.
2. (P → Q) ∧ (P ∧ ¬Q): 이 명제는 "P가 Q를 함축하고, P가 참이지만 Q는 거짓이다"라는 의미입니다. P와 Q의 모든 가능한 조합에 대해, 이 명제의 결과는 항상 거짓입니다.

<h3>1-8. 함의와 동치</h3>

항진인 조건부를 함의라 하며, 기호로 "⇒"로 표현됩니다.
예를 들어, 동물은 인간을 함의합니다. 따라서 "인간이면 동물이다"는 참입니다.
항진인 이중 조건부는 동치라 하며, 기호로 "⇔"로 표현됩니다.
예를 들어, "짝수는 2로 나누어 떨어진다"와 "짝수는 홀수가 아니다"라는 명제가 있을 때, 이 두 명제는 동치 관계에 있습니다.

<h2>2. 양화사</h2>
술어 논리에는 일반적으로 두 종류의 양화사가 있으며, 보편 양화사와 존재 양화사가 있습니다.

보편 양화사(Universal Quantifier)는 술어 논리(Predicate Logic)에서 사용되는 논리 연산자 중 하나로, 주어진 범위 내의 모든 개체에 대해 어떤 명제가 참임을 나타냅니다. 보편 양화사는 기호 '∀'(forall)로 표현되며, "모든"이라는 의미를 가집니다.

예를 들어, "모든 자연수는 0보다 크다"라는 명제를 술어 논리로 표현하면 다음과 같습니다.
∀x (x ∈ ℕ → x > 0)

여기서 'x ∈ ℕ'은 x가 자연수라는 조건을 나타내고, 'x > 0'은 x가 0보다 크다는 명제를 나타냅니다. 보편 양화사 '∀'는 이 두 조건이 주어진 범위 내 모든 개체에 대해 참임을 나타냅니다.

존재 양화사(Existential Quantification)는 주어진 범위 내에서 적어도 하나의 요소가 존재한다는 것을 나타냅니다. 예를 들어, "어떤 사람은 행복하지 않다"는 명제에서 "적어도 한 사람은 행복하지 않다"는 명제를 나타내기 위해 존재 양화사를 사용할 수 있습니다. 이 경우 이 명제를 수학적 표현으로 나타내면 ∃x(Person(x) ∧ ¬Happy(x))가 됩니다.
