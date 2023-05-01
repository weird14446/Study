# 연산자

연산자(Operator)와 피연산자(Operand)는 프로그래밍에서 연산을 수행하기 위해 사용되는 요소들입니다.

1. 연산자(Operator):
연산자는 수학적이나 논리적 연산을 수행하는 기호나 키워드입니다. 프로그래밍 언어마다 다양한 연산자가 존재하며, 일반적으로 산술, 비교, 논리, 비트 등의 연산자가 있습니다. 예를 들어, 덧셈(+), 뺄셈(-), 곱셈(*), 나눗셈(/), 나머지(%), 등호(==), 부등호(!=), 논리곱(&&), 논리합(||) 등이 연산자에 해당합니다.
2. 피연산자(Operand):
피연산자는 연산자에 의해 연산되는 값이나 변수입니다. 연산자의 좌우에 위치하여 연산의 대상이 됩니다. 예를 들어, **`a + b`** 라는 수식에서 a와 b는 피연산자입니다. 이 경우, a와 b의 값을 더하는 연산이 수행됩니다.

연산자와 피연산자를 사용하여 다양한 연산을 수행할 수 있습니다. 연산자는 연산의 종류를 결정하고, 피연산자는 연산의 대상이 되는 값을 결정합니다. 이렇게 연산자와 피연산자를 조합하여 프로그램 내에서 데이터를 처리하고 원하는 결과를 얻을 수 있습니다.

## 산술 연산자

자바(Java)에서 산술 연산자(Arithmetic Operators)는 수학적인 계산을 수행하는 데 사용되는 연산자입니다. 자바에서 사용되는 기본 산술 연산자는 다음과 같습니다.

1. 덧셈(+): 두 피연산자의 합을 계산합니다.

```java
public class Main {
    public static void main(String[] args) {
        int a = 10;
        int b = 20;
        int sum = a + b; // 결과: 30
    }
}
```

2. 뺄셈(-): 첫 번째 피연산자에서 두 번째 피연산자를 뺍니다.

```java
public class Main {
    public static void main(String[] args) {
        int a = 10;
        int b = 20;
        int difference = a - b; // 결과: -10
    }
}
```

3. 곱셈(*): 두 피연산자의 곱을 계산합니다.

```java
public class Main {
    public static void main(String[] args) {
        int a = 10;
        int b = 20;
        int product = a * b; // 결과: 200
    }
}
```

4. 나눗셈(/): 첫 번째 피연산자를 두 번째 피연산자로 나눈 몫을 계산합니다. (정수를 나누면 몫이 정수로 반환되며, 실수를 나누면 몫이 실수로 반환됩니다)

```java
public class Main {
    public static void main(String[] args) {
        int a = 10;
        int b = 20;
        int quotient = a / b; // 결과: 0 (정수 나눗셈)
        double c = 10.0;
        double d = 20.0;
        double quotient2 = c / d; // 결과: 0.5 (실수 나눗셈)
    }
}
```

5. 나머지(%): 첫 번째 피연산자를 두 번째 피연산자로 나눈 나머지를 계산합니다.

```java
public class Main {
    public static void main(String[] args) {
        int a = 10;
        int b = 3;
        int remainder = a % b; // 결과: 1
    }
}
```

이렇게 자바에서 산술 연산자를 사용하여 덧셈, 뺄셈, 곱셈, 나눗셈 및 나머지 계산을 수행할 수 있습니다. 이러한 산술 연산자는 프로그램에서 기본적인 수학적 계산을 수행하는 데 사용됩니다.

## 대입 연산자

대입 연산자(Assignment Operator)는 프로그래밍 언어에서 변수에 값을 할당하는 데 사용되는 연산자입니다. 대부분의 프로그래밍 언어에서 등호 기호(=)를 대입 연산자로 사용합니다. 대입 연산자는 변수에 값을 저장할 때 사용되며, 변수를 선언하고 값을 초기화하는 데에도 사용됩니다.

예를 들어:

```java
public class Main {
    public static void main(String[] args) {
        int a; // 변수 'a'를 선언
        a = 10; // 대입 연산자를 사용하여 변수 'a'에 값 10을 할당
    }
}
```

대입 연산자는 또한 다양한 산술 연산자와 결합하여 복합 대입 연산자(Compound Assignment Operator)를 형성할 수 있습니다. 이를 사용하면 코드를 더 간결하게 작성할 수 있습니다. 복합 대입 연산자의 예시는 다음과 같습니다.

1. += : 왼쪽 피연산자에 오른쪽 피연산자를 더한 후 결과를 왼쪽 피연산자에 할당합니다.

```java
public class Main {
    public static void main(String[] args) {
        int a = 10;
        a += 5; // a = a + 5와 동일한 표현, 결과: a = 15
    }
}
```

1. -= : 왼쪽 피연산자에서 오른쪽 피연산자를 뺀 후 결과를 왼쪽 피연산자에 할당합니다.

```java
public class Main {
    public static void main(String[] args) {
        int a = 10;
        a -= 5; // a = a - 5와 동일한 표현, 결과: a = 5
    }
}
```

1. *= : 왼쪽 피연산자에 오른쪽 피연산자를 곱한 후 결과를 왼쪽 피연산자에 할당합니다.

```java
public class Main {
    public static void main(String[] args) {
        int a = 10;
        a *= 2; // a = a * 2와 동일한 표현, 결과: a = 20
    }
}
```

1. /= : 왼쪽 피연산자를 오른쪽 피연산자로 나눈 후 결과를 왼쪽 피연산자에 할당합니다.

```java
public class Main {
    public static void main(String[] args) {
        int a = 10;
        a /= 2; // a = a / 2와 동일한 표현, 결과: a = 5
    }
}
```

1. %= : 왼쪽 피연산자를 오른쪽 피연산자로 나눈 나머지를 왼쪽 피연산자에 할당합니다.

```java
public class Main {
    public static void main(String[] args) {
        int a = 10;
        a %= 3; // a = a % 3와 동일한 표현, 결과: a = 1
    }
}
```

이러한 대입 연산자와 복합 대입 연산자는 프로그래밍에서 변수의 값을 할당하거나 업데이트하는 데 사용됩니다.

## 비교 연산자

자바에서 비교 연산자(Comparison Operators)는 두 개의 피연산자를 비교하는데 사용되는 연산자입니다. 비교 연산자는 참(true) 또는 거짓(false)의 불리언 값으로 결과를 반환합니다. 자바에서 사용되는 주요 비교 연산자는 다음과 같습니다.

1. 동등 연산자(==): 두 피연산자가 같은지 비교합니다.

```java
public class Main {
	public static void main(String[] args) {
		int a = 10;
		int b = 20;
		boolean isEqual = (a == b); // 결과: false
	}
}
```

1. 부등 연산자(!=): 두 피연산자가 다른지 비교합니다.

```java
public class Main {
    public static void main(String[] args) {
        int a = 10;
        int b = 20;
        boolean isNotEqual = (a != b); // 결과: true
    }
}
```

1. 크다 연산자(>): 왼쪽 피연산자가 오른쪽 피연산자보다 큰지 비교합니다.

```java
public class Main {
    public static void main(String[] args) {
        int a = 10;
        int b = 20;
        boolean isGreater = (a > b); // 결과: false
    }
}
```

1. 작다 연산자(<): 왼쪽 피연산자가 오른쪽 피연산자보다 작은지 비교합니다.

```java
public class Main {
    public static void main(String[] args) {
        int a = 10;
        int b = 20;
        boolean isLess = (a < b); // 결과: true
    }
}
```

1. 크거나 같다 연산자(>=): 왼쪽 피연산자가 오른쪽 피연산자보다 크거나 같은지 비교합니다.

```java
public class Main {
    public static void main(String[] args) {
        int a = 10;
        int b = 20;
        boolean isGreaterOrEqual = (a >= b); // 결과: false
    }
}
```

1. 작거나 같다 연산자(<=): 왼쪽 피연산자가 오른쪽 피연산자보다 작거나 같은지 비교합니다.

```java
public class Main {
    public static void main(String[] args) {
        int a = 10;
        int b = 20;
        boolean isLessOrEqual = (a <= b); // 결과: true
    }
}
```

이러한 비교 연산자는 조건문(예: if, while, for) 및 논리 연산자와 함께 사용되어 프로그램의 흐름을 제어하는 데 사용됩니다.

## 논리 연산자

자바에서 논리 연산자(logical operators)는 주로 불린(boolean) 값(true 또는 false)을 가지는 피연산자를 대상으로 연산을 수행합니다. 논리 연산자는 조건문과 반복문에서 특히 유용하게 사용됩니다. 자바에서 사용되는 주요 논리 연산자는 다음과 같습니다:

1. AND 연산자 (&&): 두 피연산자가 모두 참일 경우에만 참을 반환합니다. 그렇지 않으면 거짓을 반환합니다.

```java
public class Main {
    public static void main(String[] args) {
        boolean result = true && false; // result는 false가 됩니다.
    }
}
```

1. OR 연산자 (||): 두 피연산자 중 하나 이상이 참일 경우 참을 반환합니다. 그렇지 않으면 거짓을 반환합니다.

```java
public class Main {
    public static void main(String[] args) {
        boolean result = true || false; // result는 true가 됩니다.
    }
}
```

1. NOT 연산자 (!): 피연산자의 논리 값을 반전시킵니다. 즉, 참이면 거짓을 반환하고, 거짓이면 참을 반환합니다.

```java
public class Main {
    public static void main(String[] args) {
        boolean result = !true; // result는 false가 됩니다.
    }
}
```

이러한 논리 연산자를 사용하여 복잡한 조건을 표현할 수 있습니다.
자세한 내용은 집합론 강의를 참고해주시길 바랍니다.

## 삼항 연산자

자바에서 삼항 연산자(ternary operator)는 간단한 if-else 구문을 축약하여 사용할 수 있는 조건 연산자입니다. 삼항 연산자는 '?'와 ':' 기호를 사용하며, 다음과 같은 형식으로 사용됩니다.

```java
condition ? expression1 : expression2;
```

삼항 연산자는 먼저 조건(condition)을 평가합니다. 조건이 참인 경우 expression1을 반환하고, 거짓인 경우 expression2를 반환합니다. 이렇게 삼항 연산자를 사용하면 간단한 조건문을 간결하게 표현할 수 있습니다.

예를 들어, 두 수 중에서 큰 수를 찾는 예제를 삼항 연산자를 사용하여 다음과 같이 작성할 수 있습니다.

```java
public class Main {
    public static void main(String[] args) {
        int a = 10;
        int b = 20;
        int max = (a > b) ? a : b;
        System.out.println("The maximum value is " + max);
    }
}
```

위 코드에서 삼항 연산자는 (a > b) 조건을 평가하고, 이 조건이 참이면 a를 반환하고 거짓이면 b를 반환합니다. 이 예제에서는 b가 더 크므로 max 변수에는 20이 저장되고, "The maximum value is 20"이 출력됩니다.

## 증감 연산자

증감식은 반복문에서 반복을 제어하는 데 중요한 역할을 합니다. 자바에서는 주로 **`++`** (증가 연산자)와 **`--`** (감소 연산자)를 사용해 증감식을 표현합니다.

1. **증가 연산자 (`++`)**: 변수의 값을 1 증가시킵니다. 이 연산자는 변수 앞에 오거나 뒤에 올 수 있습니다.
- 전위 증가 연산자 (예: **`++i`**): 먼저 변수의 값을 증가시킨 후, 그 값을 사용합니다.
- 후위 증가 연산자 (예: **`i++`**): 먼저 변수의 값을 사용한 후, 그 값을 증가시킵니다.

예시:

```java
public class main {
    public static void main(String[] args) {
        int i = 0;
        System.out.println(++i);  // 출력: 1 (i의 값을 먼저 증가시킨 후 출력)
        System.out.println(i++);  // 출력: 1 (i의 현재 값을 출력한 후 증가시킴, i는 이제 2)
        System.out.println(i);    // 출력: 2 (이전 줄에서 i값이 증가했음)
    }
}
```

1. **감소 연산자 (`--`)**: 변수의 값을 1 감소시킵니다. 이 연산자도 변수 앞에 오거나 뒤에 올 수 있습니다.
- 전위 감소 연산자 (예: **`--i`**): 먼저 변수의 값을 감소시킨 후, 그 값을 사용합니다.
- 후위 감소 연산자 (예: **`i--`**): 먼저 변수의 값을 사용한 후, 그 값을 감소시킵니다.

예시:

```java
public class Main {
    public static void main(String[] args) {
        int i = 2;
        System.out.println(--i);  // 출력: 1 (i의 값을 먼저 감소시킨 후 출력)
        System.out.println(i--);  // 출력: 1 (i의 현재 값을 출력한 후 감소시킴, i는 이제 0)
        System.out.println(i);    // 출력: 0 (이전 줄에서 i값이 감소했음)
    }
}
```

증감식은 **`for`** 반복문 등에서 반복 횟수를 제어하는 데 사용됩니다. 예를 들어, **`for(int i = 0; i < 10; i++) {...}`** 에서 **`i++`** 는 증감식으로, 반복마다 **`i`** 의 값이 1씩 증가하도록 합니다. 이렇게 해서 반복문은 정확히 10번 실행되고, **`i`** 의 값은 0부터 9까지 변화하게 됩니다.