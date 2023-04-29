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