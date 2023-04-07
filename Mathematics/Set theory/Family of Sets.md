<h1>Family of Sets</h1>
집합족(Collection of sets, Family of sets)은 집합들의 집합을 의미합니다. 다시 말해, 집합족은 원소들이 모두 집합인 집합입니다. 이러한 집합족은 수학적 구조를 연구하거나 문제를 해결하는 데 유용한 도구로 사용됩니다.

집합족의 예시로는 다음과 같은 것들이 있습니다:

1. 집합 A, B, C가 주어졌을 때, 이 집합들로 이루어진 집합족 {A, B, C}가 있습니다.
2. 실수 전체 집합을 포함하는 구간들의 집합, 즉 {[a, b] | a, b ∈ ℝ, a ≤ b}는 집합족입니다.
3. 모든 유한 집합들로 이루어진 집합족은 또 다른 예시입니다.

집합족에 적용되는 연산 및 개념들은 일반 집합에 적용되는 것들과 유사합니다. 집합족에 대해 합집합, 교집합, 차집합 등의 연산을 수행할 수 있으며, 부분 집합과 전력집합 개념도 적용할 수 있습니다.

집합족이 첨수(번호)가 부여된 집합들로 이루어졌다면, 그 집합족을 첨수족이라 합니다.
예를 들어, 

$$
F=\\{ A_1, A_2, A_3... \\}
$$

와 같이 이루어져 있다면, 그 집합족을 첨수족이라 합니다.

<h2>집합족의 연산</h2>


1. 합집합 : 

$$
\bigcup F = \bigcup_{A\in F}A = A_1 \cup A_2\cup A_3...= \\{ x:\exists A\in F, \ x \in A \\}
$$

2. 교집합 : 

$$
\bigcap F = \bigcap_{A\in F}A = A_1 \cap A_2\cap A_3...= \\{ x:\forall A\in F, \ x \in A \\} 
$$

<h2>드모르간 법칙</h2>

1.

$$
( \bigcup _{i\in I}A_i ) ^c=\bigcap _{i\in I}{A_i}^c
$$

2.

$$
( \bigcap _{i\in I}A_i ) ^c=\bigcup _{i\in I}{A_i}^c
$$

1번 드모르간 법칙의 증명


$$
x\in ( \bigcup _{i\in I}A_i ) ^c ⇔ \neg (x\in\bigcup _{i\in I}A_i )\\
$$

$$
⇔ \neg (\exists i \in I, \ x\in A_i) \\
$$

$$
⇔ \forall i \in I, \ x \notin A_i \ \\
$$

$$
⇔ \forall i \in I, \ x \in A_i \ ^c
$$

$$
\\ ⇔ x \in \bigcap _{i \in I} A_i \ ^c
$$

$$
\therefore ( \bigcup _{i\in I}A_i ) ^c=\bigcap _{i\in I}{A_i}^c \ \ \ \ \ \blacksquare
$$

2번 드모르간 법칙의 증명

$$
x\in ( \bigcap _{i\in I}A_i ) ^c ⇔ \neg (x\in\bigcap _{i\in I}A_i )\\
$$

$$
⇔ \neg (\forall i \in I, \ x\in A_i) \\ 
$$

$$
⇔ \exists i \in I, \ x \notin A_i \ \\
$$

$$
⇔ \exists i \in I, \ x \in A_i \ ^c
$$

$$
\\ ⇔ x \in \bigcup _{i \in I} A_i \ ^c
$$

$$
\therefore ( \bigcap _{i\in I}A_i ) ^c=\bigcup _{i\in I}{A_i}^c \ \ \ \ \ \blacksquare
$$

<h2>분배법칙</h2>

1.

$$
A \cap (\bigcup _{B\in F}B)=(\bigcup _{B\in F}A \cap B)
$$

2.

$$
A \cup (\bigcap _{B\in F}B)=(\bigcap _{B\in F}A \cup B)
$$

1번 분배법칙의 증명

$$
x\in A \cap (\bigcup _{B\in F}B)⇔ x \in A \land (x\in \bigcup _{B\in F}B)
$$

$$
⇔ x\in A \land \exists B \in F, \ x\in B
$$

$$
⇔ \exists B\in F, \ x\in A \land x\in B
$$

$$
⇔ \exists B \in F, \ x\in (A\cap B)
$$

$$
⇔ x\in \bigcup _{B\in F}(A\cap B)
$$

$$
\therefore A \cap (\bigcup _{B\in F}B)=(\bigcup _{B\in F}A \cap B) \ \ \ \ \ \blacksquare
$$

2번 분배법칙의 증명

$$
x\in A \cup (\bigcap _{B\in F}B)
⇔ x \in A \lor (x\in \bigcap _{B\in F}B)
$$

$$
⇔ x\in A \lor \forall B \in F, \ x\in B
$$

$$
⇔ \forall B\in F, \ x\in A \lor x\in B
$$

$$
⇔ \forall B \in F, \ x\in (A\cup B)
$$

$$
⇔ x\in \bigcap _{B\in F}(A\cup B)
$$

$$
\therefore A \cup (\bigcap _{B\in F}B)=(\bigcap _{B\in F}A \cup B) \ \ \ \ \ \blacksquare
$$
