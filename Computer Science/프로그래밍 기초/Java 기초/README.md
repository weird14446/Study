# 자바

자바(Java)는 1995년에 썬 마이크로시스템즈(Sun Microsystems, 현재 Oracle Corporation에 인수됨)에서 개발한 객체지향 프로그래밍 언어입니다. 자바는 플랫폼 독립적이며, 네트워크와 웹 개발에 특화되어 있어 인기가 높습니다.

자바의 주요 특징은 다음과 같습니다:

1. 플랫폼 독립적: 자바로 작성된 프로그램은 Java Virtual Machine(JVM) 위에서 실행되기 때문에, 다양한 운영체제에서 동일한 코드를 실행할 수 있습니다. 이를 "Write Once, Run Anywhere"라고 표현하기도 합니다.
2. 객체지향: 자바는 클래스와 객체를 사용하여 모듈화 및 추상화를 지원하는 완전한 객체지향 프로그래밍 언어입니다. 이는 코드의 재사용성과 유지 보수성을 향상시키며, 개발자들이 더 쉽게 복잡한 문제를 해결할 수 있게 도와줍니다.
3. 강력한 메모리 관리: 자바는 가비지 컬렉터(Garbage Collector)를 통해 메모리를 자동으로 관리하며, 개발자가 메모리 관리에 신경 쓰지 않아도 됩니다. 이는 메모리 누수와 관련된 문제를 최소화하는 데 도움이 됩니다.
4. 거대한 표준 라이브러리: 자바는 방대한 표준 라이브러리를 제공하여 다양한 기능을 쉽게 구현할 수 있습니다. 라이브러리에는 데이터 구조, 알고리즘, 네트워크, 입출력, 그래픽 등 다양한 기능이 포함되어 있습니다.
5. 다중 스레드 지원: 자바는 다중 스레드를 쉽게 구현할 수 있는 기능을 제공합니다. 이를 통해 개발자들은 동시성을 적용하여 프로그램의 효율성을 높일 수 있습니다.

자바는 웹 애플리케이션, 모바일 애플리케이션, 데스크톱 애플리케이션, 서버 애플리케이션 등 다양한 분야에서 널리 사용되며, 현재 가장 인기 있는 프로그래밍 언어 중 하나입니다.

코드는 기본적으로 다음과 같이 작성합니다.

```java
public class Main // 클래스의 이름은 파일 이름과 같다. 여기서는 파일 이름이 Main
{
    public static void main(String[] args) {
        //여기에서 작업을 시작합니다.
    }
}
```
자바에서 **`System.out.println`** 함수는 표준 출력(일반적으로 콘솔 창)에 텍스트를 출력하고 줄 바꿈을 수행하는 데 사용됩니다. 이 함수는 자바 프로그램을 작성하고 실행할 때 결과를 확인하기 위한 도구로 자주 사용됩니다.

**`System.out.println`** 함수의 간단한 설명:

- **`System`**: 자바에서 기본 제공되는 클래스로, 표준 입출력과 관련된 기능을 제공합니다.
- **`out`**: **`System`** 클래스의 정적(static) 필드로, **`PrintStream`** 객체를 참조합니다. 이 객체는 표준 출력 스트림을 나타냅니다.
- **`println`**: **`PrintStream`** 클래스의 메서드로, 전달된 인자를 콘솔에 출력한 후 줄 바꿈을 수행합니다.

간단한 사용 예제:

```java
public class Main {
    public static void main(String[] args) {
        System.out.println("Hello, World!");
    }
}
```

위 코드를 실행하면 콘솔에 "Hello, World!"가 출력되고 줄 바꿈이 수행됩니다. **`System.out.println`** 함수는 문자열, 숫자, 불리언 값 등 다양한 데이터 타입을 인자로 받아 출력할 수 있습니다.

## 목차
0. 개발 환경 구축
1. [자료형과 변수](https://github.com/weird14446/Study/blob/main/Computer%20Science/%ED%94%84%EB%A1%9C%EA%B7%B8%EB%9E%98%EB%B0%8D%20%EA%B8%B0%EC%B4%88/Java%20%EA%B8%B0%EC%B4%88/Data%20Type%20and%20Variable.md)
2. [연산자](https://github.com/weird14446/Study/blob/main/Computer%20Science/%ED%94%84%EB%A1%9C%EA%B7%B8%EB%9E%98%EB%B0%8D%20%EA%B8%B0%EC%B4%88/Java%20%EA%B8%B0%EC%B4%88/Operator.md)
3. [문자열](https://github.com/weird14446/Study/blob/main/Computer%20Science/%ED%94%84%EB%A1%9C%EA%B7%B8%EB%9E%98%EB%B0%8D%20%EA%B8%B0%EC%B4%88/Java%20%EA%B8%B0%EC%B4%88/String.md)
4. [제어문]()
5. [배열]()
6. [메소드]()
7. [클래스]()
8. [추상 클래스와 인터페이스]()
9. [제네릭스]()
10. [익명 클래스, 람다와 스트림]()
11. [예외처리]()
12. [입출력과 파일]()