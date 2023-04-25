## 자료형

자료형(Data Type)은 프로그래밍 언어에서 변수나 상수에 할당되는 값의 종류를 나타냅니다. 자료형은 프로그래머가 작성한 코드를 컴퓨터가 올바르게 처리하고 이해할 수 있게 돕습니다. 각 프로그래밍 언어마다 지원하는 자료형이 다양하게 있지만, 일반적으로 몇 가지 기본 자료형이 존재합니다.

1. 정수(Integer): 정수 자료형은 소수점이 없는 정수 값을 저장하는 데 사용됩니다. 예를 들어, -3, 0, 42와 같은 숫자를 저장할 때 사용합니다.
2. 실수(Floating-point): 실수 자료형은 소수점이 있는 숫자 값을 저장하는 데 사용됩니다. 예를 들어, 3.14, -0.001, 1.0과 같은 숫자를 저장할 때 사용합니다. 주로 float와 double 등의 형태로 사용됩니다.
3. 문자(Character): 문자 자료형은 개별 문자를 저장하는 데 사용됩니다. 예를 들어, 'A', 'b', '9'와 같은 하나의 문자를 저장할 때 사용합니다.
4. 문자열(String): 문자열 자료형은 문자의 시퀀스를 저장하는 데 사용됩니다. 예를 들어, "Hello, world!", "John Doe"와 같은 여러 개의 문자로 이루어진 값을 저장할 때 사용합니다.
5. 불(Boolean): 불 자료형은 참(True)과 거짓(False) 두 가지 값 중 하나를 저장하는 데 사용됩니다. 조건문과 논리 연산에서 주로 사용됩니다. (이에 대한 이해를 돕기 위해 수학 폴더에서 집합론 첫 번째 강의를 보시는 것이 도움이 될겁니다.)
6. 배열(Array) 및 리스트(List): 배열과 리스트 자료형은 동일한 자료형의 여러 값을 순차적으로 저장하는 데 사용됩니다. 배열은 고정된 크기를 가지며, 리스트는 가변적인 크기를 가집니다.
7. 구조체(Structure), 클래스(Class), 객체(Object): 이러한 자료형들은 개발자가 사용자 정의 자료형을 생성하는 데 사용됩니다. 구조체와 클래스는 데이터와 관련된 함수를 그룹화하여 복잡한 자료형을 정의할 수 있게 해주며, 객체는 이러한 클래스의 인스턴스를 나타냅니다.

각 프로그래밍 언어는 이러한 기본 자료형 외에도 고유한 자료형을 제공할 수 있으며, 언어마다 자료형의 표현 방식과 사용 방법이 다를 수 있습니다.
우선 5번 자료형까지 외워주시길 바랍니다.
6번과 7번 자료형에 대해서는 추후에 자세하게 설명하겠습니다.

## 변수

자바(Java)에서 변수는 데이터를 저장하고 참조하기 위한 기본 단위로 사용되며, 자료형과 함께 선언되어야 합니다. 자바에서 변수를 선언하고 사용하는 방법은 다음과 같습니다.

1. 변수 선언: 자바에서 변수를 선언하려면 먼저 해당 변수의 자료형을 명시한 후 변수의 이름을 지정해야 합니다. 예를 들어, 정수를 저장하는 변수를 선언하려면 다음과 같이 작성합니다.

```java
int myInteger;
```

이 경우, **`myInteger`** 라는 이름의 정수형 변수가 선언되었습니다.

2. 변수 초기화: 변수를 사용하기 전에 초기값을 할당해야 합니다. 자바에서 변수를 초기화하는 방법은 선언과 동시에 값을 할당하거나, 나중에 값을 할당하는 것입니다.

```java
public class Main {
    public static void main(String[] args) {
        int myInteger = 10; // 선언과 동시에 초기화

        int myInteger; // 선언
        myInteger = 10; // 초기화
    }
}
```

3. 변수 사용: 변수를 사용하여 값을 읽거나 수정할 수 있습니다.

```java
public class Main {
    public static void main(String[] args) {
        int myInteger = 10;
        int anotherInteger = myInteger + 5; // 값 읽기

        myInteger = 20; // 값 수정
    }
}
```

## 주석

자바(Java)에서 주석(Comment)은 코드에 대한 설명, 정보 제공, 코드 비활성화 등의 목적으로 사용되며, 컴파일 과정에서 무시됩니다. 주석을 사용하면 코드를 이해하기 쉽게 만들고, 나중에 코드를 수정하거나 디버깅할 때 도움이 됩니다. 자바에서 주로 사용되는 두 가지 주석 스타일은 다음과 같습니다.

1. 한 줄 주석(Single-line Comment): 두 개의 슬래시(**`//`**)로 시작하는 주석으로, 주석 시작부터 해당 줄의 끝까지의 내용을 주석으로 처리합니다.

```java
public class Main {
    public static void main(String[] args) {
        int myInteger = 10; // 이것은 한 줄 주석입니다.
    }
}
```

2. 여러 줄 주석(Multi-line Comment): 슬래시와 별표(**`/*`**)로 시작하고, 별표와 슬래시(**`/`**)로 끝나는 주석으로, 주석 시작부터 주석 끝까지의 내용을 주석으로 처리합니다. 여러 줄 주석은 여러 줄의 내용을 주석으로 처리할 때 사용됩니다.

```java
public class Main {
    public static void main(String[] args) {
        /*
        * 이것은 여러 줄 주석입니다.
        * 이 주석은 여러 줄에 걸쳐 작성할 수 있습니다.
        */
        int myInteger = 10;
    }
}
```

이렇게 자바에서 주석을 사용하여 코드에 대한 설명을 작성하거나, 필요한 경우 일부 코드를 비활성화할 수 있습니다. 주석을 통해 코드의 가독성과 유지 보수성을 높일 수 있습니다.

## 형 변환

자바(Java)에서 형 변환(Type Casting)은 한 자료형의 값을 다른 자료형으로 변환하는 과정입니다. 형 변환은 프로그램에서 데이터를 처리하거나 연산을 수행할 때 필요한 경우 사용됩니다. 자바에서 형 변환은 두 가지 방법으로 구분됩니다.

1. 암시적 형 변환(Implicit Type Casting): 자동으로 이루어지는 형 변환으로, 작은 자료형에서 큰 자료형으로 변환할 때 발생합니다. 이 과정에서 데이터 손실의 위험이 없기 때문에 자바 컴파일러가 자동으로 처리해 줍니다.

```java
public class Main {
    public static void main(String[] args) {
        int myInt = 10;
        double myDouble = myInt; // int에서 double로 암시적 형 변환

        System.out.println(myDouble); // 출력: 10.0
    }
}
```

2. 명시적 형 변환(Explicit Type Casting): 프로그래머가 직접 변환하려는 자료형을 명시하는 형 변환으로, 큰 자료형에서 작은 자료형으로 변환할 때 사용됩니다. 이 과정에서 데이터 손실의 위험이 있으므로 프로그래머가 변환할 자료형을 명시해야 합니다.

```java
public class Main {
    public static void main(String[] args) {
        double myDouble = 10.5;
        int myInt = (int) myDouble; // double에서 int로 명시적 형 변환

        System.out.println(myInt); // 출력: 10 (소수점 이하 값이 손실됨)
    }
}
```

명시적 형 변환을 사용할 때 주의해야 할 점은 데이터 손실이 발생할 수 있다는 것입니다. 예를 들어, 실수형 값을 정수형으로 변환할 때 소수점 이하의 값이 손실되며, 큰 정수 값을 작은 정수 자료형으로 변환할 때도 데이터 손실이 발생할 수 있습니다. 따라서 명시적 형 변환을 사용할 때 데이터 손실에 대한 고려가 필요합니다.

자바에서 문자열(String)과 다른 기본 자료형(정수, 실수 등) 간의 형 변환을 수행하는 방법은 다음과 같습니다.

1. 정수에서 문자열로 형 변환:

```java
public class Main {
    public static void main(String[] args) {
        int myInt = 10;
        String myString = Integer.toString(myInt);
        // 또는
        String myString = String.valueOf(myInt);
    }
}
```

2. 실수형에서 문자열로 형 변환:

```java
public class Main {
    public static void main(String[] args) {
        double myDouble = 10.5;
        String myString = Double.toString(myDouble);
        // 또는
        String myString = String.valueOf(myDouble);
    }
}
```

3. 문자열에서 정수로 형 변환:

```java
public class Main {
    public static void main(String[] args) {
        String myString = "10";
        int myInt = Integer.parseInt(myString);
    }
}
```

4. 문자열에서 실수로 형 변환:

```java
public class Main {
    public static void main(String[] args) {
        String myString = "10.5";
        double myDouble = Double.parseDouble(myString);
    }
}
```

이렇게 자바에서 문자열과 다른 기본 자료형 간의 형 변환을 수행할 수 있습니다. 이를 통해 문자열을 숫자로 변환하여 계산을 수행하거나, 숫자를 문자열로 변환하여 출력 등의 작업을 수행할 수 있습니다.