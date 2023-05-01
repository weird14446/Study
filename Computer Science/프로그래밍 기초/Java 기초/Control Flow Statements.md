# 제어문

제어문(control statement)은 프로그램의 흐름을 제어하는 문장을 말합니다. 자바에서는 주로 조건문과 반복문이 사용됩니다.

## 조건문 (if, switch)

자바에서는 주로 두 가지의 조건문을 사용합니다: **`if`** 문과 **`switch`** 문입니다.

1. **if 문**: **`if`** 문은 주어진 조건이 참(**`true`**)일 때만 해당 코드 블록을 실행합니다. **`else if`** 와 **`else`** 를 이용해 더 복잡한 조건 체인을 만들 수도 있습니다.

```java
if (condition1) {
    // condition1이 참일 때 실행되는 코드
} else if (condition2) {
    // condition1이 거짓이고 condition2가 참일 때 실행되는 코드
} else {
    // condition1과 condition2 모두 거짓일 때 실행되는 코드
}
```

위의 조건문에서 **`condition1`** 과 **`condition2`** 는 boolean 타입의 표현식입니다.

1. **switch 문**: **`switch`** 문은 변수의 값에 따라 여러 개의 코드 블록 중 하나를 실행합니다.

```java
switch (variable) {
    case value1:
        // variable이 value1일 때 실행되는 코드
        break;
    case value2:
        // variable이 value2일 때 실행되는 코드
        break;
    default:
        // variable이 어떤 case에도 해당하지 않을 때 실행되는 코드
}
```

**`switch`** 문에서는 **`break`** 문을 사용해 각 case에서 코드 실행을 중단하고 **`switch`** 문을 빠져나옵니다. **`default`** 는 선택적으로 사용하며, **`variable`** 이 어떤 case에도 해당하지 않을 때 실행됩니다.

이러한 조건문을 통해 프로그램의 흐름을 조절하고, 주어진 조건에 따라 다른 동작을 수행할 수 있습니다.

1. **if 문 예제**

```java
public class Main {
    public static void main(String[] args) {
        int age = 15;

        if (age < 13) {
            System.out.println("You are a child.");
        } else if (age < 20) {
            System.out.println("You are a teenager.");
        } else {
            System.out.println("You are an adult.");
        }
    }
}
```

이 코드는 **`age`** 라는 변수의 값에 따라 다른 메시지를 출력합니다. 만약 **`age`** 가 13 미만이면 "You are a child."가 출력되고, **`age`** 가 13 이상 20 미만이면 "You are a teenager."가 출력되며, 그 외의 경우에는 "You are an adult."가 출력됩니다.

2. **switch 문 예제**

```java
public class Main  {
    public static void main(String[] args) {
        char grade = 'B';

        switch (grade) {
            case 'A':
                System.out.println("Excellent!");
                break;
            case 'B':
                System.out.println("Good job!");
                break;
            case 'C':
                System.out.println("Well done");
                break;
            default:
                System.out.println("Invalid grade");
        }
    }
}
```

이 코드는 **`grade`** 라는 변수의 값에 따라 다른 메시지를 출력합니다. 만약 **`grade`** 가 'A'이면 "Excellent!"가 출력되고, 'B'이면 "Good job!"이 출력되며, 'C'이면 "Well done"이 출력됩니다. **`grade`** 가 'A', 'B', 'C' 중 어느 것도 아닌 경우에는 "Invalid grade"가 출력됩니다.

## 반복문 (for, while, do-while)
1. **for 반복문**: **`for`** 반복문은 주로 정해진 횟수만큼 반복을 해야 할 때 사용합니다. **`for`** 반복문의 기본 구조는 다음과 같습니다:

```java
for(초기화; 조건식; 증감식) {
    // 반복적으로 실행할 코드
}
```

- **초기화**: 반복문이 시작될 때 한 번만 실행됩니다. 주로 반복문의 제어 변수를 초기화하는 데 사용됩니다.
- **조건식**: 각 반복이 시작되기 전에 평가됩니다. 조건식이 **`true`** 일 때만 코드 블록이 실행됩니다. 조건식이 **`false`** 이면 반복문이 종료됩니다.
- **증감식**: 코드 블록의 실행이 끝날 때마다 실행됩니다. 주로 제어 변수를 증가시키거나 감소시키는 데 사용됩니다.
1. **while 반복문**: **`while`** 반복문은 특정 조건이 만족되는 동안 코드 블록을 계속해서 실행합니다. **`while`** 반복문의 기본 구조는 다음과 같습니다:

```java
while(조건식) {
    // 반복적으로 실행할 코드
}
```

- **조건식**: 각 반복이 시작되기 전에 평가됩니다. 조건식이 **`true`** 일 때만 코드 블록이 실행됩니다. 조건식이 **`false`** 이면 반복문이 종료됩니다.
1. **do-while 반복문**: **`do-while`** 반복문은 **`while`** 반복문과 유사하지만, 조건식이 코드 블록의 실행 이후에 평가된다는 점이 다릅니다. 따라서 **`do-while`** 반복문은 코드 블록이 최소한 한 번은 실행된다는 것을 보장합니다. **`do-while`** 반복문의 기본 구조는 다음과 같습니다:

```java
do {
    // 반복적으로 실행할 코드
} while(조건식);
```

- **조건식**: 코드 블록의 실행이 끝난 후에 평가됩니다. 조건식이 **`true`** 일 경우 다시 코드 블록이 실행됩니다. 조건식이 **`false`** 이면 반복문이 종료됩니다.

각 반복문은 조건과 반복되는 부분에 따라 적합한 상황이 다릅니다. 반복의 횟수가 정해진 경우 **`for`** 반복문을, 조건에 따라 반복을 결정해야 하는 경우 **`while`** 또는 **`do-while`** 반복문을 사용할 수 있습니다.

1. **for 반복문**: 1부터 10까지의 숫자를 출력하는 **`for`** 반복문 예제입니다.

```java
public class Main {
    public static void main(String[] args) {
        for(int i = 1; i <= 10; i++) {
            System.out.println(i);
        }
    }
}
```

1. **while 반복문**: 1부터 10까지의 숫자를 출력하는 **`while`** 반복문 예제입니다.

```java
public class Main {
    public static void main(String[] args) {
        int i = 1;
        while(i <= 10) {
            System.out.println(i);
            i++;
        }
    }
}
```

1. **do-while 반복문**: 1부터 10까지의 숫자를 출력하는 **`do-while`** 반복문 예제입니다.

```java
public class Main {
    public static void main(String[] args) {
        int i = 1;
        do {
            System.out.println(i);
            i++;
        } while(i <= 10);
            }
}
```

이렇게 각 반복문은 조건과 반복되는 부분에 따라 적합한 상황이 다릅니다. **`for`** 반복문은 초기화, 조건, 그리고 반복 후 작업을 한 줄에 작성하여 특정 횟수만큼의 반복을 명확히 표현하고, **`while`** 반복문은 조건이 참인 동안 계속해서 코드 블록을 실행하며, **`do-while`** 반복문은 조건에 상관없이 먼저 코드 블록을 실행하고, 그 다음에 조건을 검사하여 반복을 계속할지 결정합니다.

## break, continue

**`break`** 와 **`continue`** 는 자바에서 반복문의 흐름을 제어하는 데 사용되는 키워드입니다.

1. **break**: **`break`** 는 현재의 반복문을 완전히 종료하고, 반복문 바깥의 코드를 실행합니다. **`break`** 는 가장 가까운 반복문만을 종료합니다. 따라서 중첩된 반복문에서는 내부의 반복문만 종료하고, 외부의 반복문은 계속 실행됩니다. 하지만 라벨과 함께 사용하면 지정된 라벨의 반복문까지 종료시킬 수 있습니다.

```java
for(int i = 0; i < 10; i++) {
    if(i == 5) {
        break;
    }
    System.out.println(i);
}
// 출력: 0 1 2 3 4
```

위 코드에서 **`break`** 가 실행되는 순간 **`for`** 반복문은 종료되고, 이후의 코드가 실행됩니다.

1. **continue**: **`continue`** 는 현재의 반복을 즉시 종료하고, 반복문의 다음 반복을 시작합니다. **`continue`** 는 현재의 반복만 건너뛰고, 반복문 자체를 종료하지는 않습니다. **`continue`** 역시 라벨과 함께 사용하여 특정 반복문으로 건너뛸 수 있습니다.

```java
for(int i = 0; i < 10; i++) {
    if(i == 5) {
        continue;
    }
    System.out.println(i);
}
// 출력: 0 1 2 3 4 6 7 8 9
```

위 코드에서 **`continue`** 가 실행되는 순간 **`for`** 반복문의 현재 반복은 종료되고, 다음 반복이 시작됩니다. 따라서 **`i == 5`** 인 경우는 출력되지 않습니다.

이렇게 **`break`** 와 **`continue`** 를 사용하면 반복문의 흐름을 유연하게 제어할 수 있습니다. 하지만 이 두 키워드를 과도하게 사용하면 코드를 이해하기 어렵게 만들 수 있으므로, 적절히 사용해야 합니다.

## label

자바에서 라벨(label)은 특정 코드 블록에 이름을 붙여주는 역할을 합니다. 주로 반복문에서 사용되며, **`break`** 나 **`continue`** 와 함께 사용하여 특정 블록의 시작 또는 끝으로 제어를 이동시키는데 사용됩니다.

라벨은 다음과 같이 사용됩니다:

```java
labelName:
for(int i = 0; i < 5; i++) {
    // 반복문 코드
}
```

여기서 **`labelName:`** 이 라벨입니다.

라벨은 중첩된 반복문에서 특정 반복문을 명시적으로 종료하거나 계속하는데 유용합니다. 예를 들어, 아래와 같은 코드에서는 **`outer`** 라는 라벨을 사용하여 외부 반복문을 종료합니다:

```java
outer:
for(int i = 0; i < 5; i++) {
    for(int j = 0; j < 5; j++) {
        if(i * j > 10) {
            break outer;
        }
    }
}
```

위 코드에서 **`break outer;`** 구문은 **`outer`** 라벨이 붙은 가장 가까운 반복문을 종료시킵니다. 따라서 이 경우 외부의 **`for`** 반복문이 종료됩니다.

비슷한 방식으로 **`continue`** 구문과 함께 라벨을 사용하면, 라벨이 붙은 가장 가까운 반복문의 다음 반복으로 제어를 이동시킬 수 있습니다.

그러나 라벨을 사용하는 것은 코드를 이해하기 어렵게 만들 수 있으므로, 꼭 필요한 경우가 아니라면 사용을 자제하는 것이 좋습니다. 대부분의 경우 라벨 없이도 문제를 해결할 수 있는 방법이 있습니다.