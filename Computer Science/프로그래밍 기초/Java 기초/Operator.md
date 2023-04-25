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