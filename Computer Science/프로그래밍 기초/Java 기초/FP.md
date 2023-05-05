# Functional Programming

자바에서의 함수형 프로그래밍은 Java 8부터 도입된 개념으로, 함수를 일급 객체로 취급하여 프로그래밍하는 방식을 말합니다. 함수형 프로그래밍은 순수 함수(pure functions)를 사용하고, 부작용(side effects)을 피하는 것을 목표로 합니다.

Java 8에서는 다음과 같은 주요 함수형 프로그래밍 기능이 도입되었습니다:

1. **람다 표현식(Lambda Expressions)**: 람다 표현식은 익명 함수를 생성하는 간결한 방법입니다. 람다는 함수형 인터페이스를 구현하는데 사용되며, 이는 오직 하나의 추상 메소드를 가진 인터페이스를 의미합니다. 예를 들어, **`(x, y) -> x + y`** 는 두 개의 인자를 받아서 그 합을 반환하는 람다 표현식입니다.
2. **메소드 참조(Method References)**: 메소드 참조는 특정 메소드를 참조하는 간단한 방법입니다. 이를 통해 코드의 재사용성을 높일 수 있습니다. 예를 들어, **`System.out::println`** 는 System.out.println 메소드를 참조합니다.
3. **스트림 API(Stream API)**: 스트림 API는 데이터의 흐름을 더 간결하게 처리할 수 있게 해주는 고차원 추상화 개념입니다. 스트림은 데이터 소스에서 데이터를 읽어 들이고, 이를 변환하거나 필터링하거나 집계하는 등의 연산을 수행할 수 있습니다.
4. **Optional 클래스**: 이 클래스는 null 값을 가질 수 있는 객체를 감싸는 래퍼 클래스입니다. 이를 통해 NullPointerException을 방지하고, null을 안전하게 처리할 수 있습니다.
5. **함수형 인터페이스(Functional Interfaces)**: 함수형 인터페이스는 오직 하나의 추상 메소드를 가진 인터페이스를 말합니다. 이 인터페이스는 람다 표현식이나 메소드 참조를 통해 구현될 수 있습니다. 자바 8은 Runnable, Callable, Comparator 등의 기존 인터페이스 외에도 Consumer, Function, Supplier, Predicate 등의 새로운 함수형 인터페이스를 제공합니다.

## Stream

자바에서 스트림(Stream)은 Java 8에서 도입된 기능으로, 데이터의 흐름을 더 간결하게 처리할 수 있는 고차원 추상화 개념입니다. 스트림은 데이터를 처리하는 데 사용되는 함수형 프로그래밍 기법 중 하나로, 컬렉션, 배열, I/O 채널 등 다양한 데이터 소스에서 데이터를 추출하고 변환, 필터링, 그룹화, 정렬, 집계 등 다양한 연산을 수행할 수 있습니다.

스트림 API는 두 가지 주요 구성 요소로 구성됩니다.

1. 스트림 소스 (Stream Source) : 스트림을 생성하는 데이터 소스입니다. 예를 들어, 컬렉션, 배열, I/O 채널 등이 스트림 소스가 될 수 있습니다.
2. 스트림 연산 (Stream Operations) : 스트림에 대해 수행할 수 있는 연산들입니다. 스트림 연산에는 중간 연산 (Intermediate Operations)과 최종 연산 (Terminal Operations)이 있습니다.
    
    중간 연산: 중간 연산은 스트림을 변환하는 데 사용되며, 필터링, 매핑, 정렬 등의 작업을 수행합니다. 중간 연산은 다른 중간 연산이나 최종 연산과 연결할 수 있는 새로운 스트림을 반환합니다.
    
    최종 연산: 최종 연산은 스트림 파이프라인의 결과를 생성하거나 소비하는 작업을 수행합니다. 예를 들어, 리스트로 변환, 배열로 변환, 최소/최대값 찾기, 합계 계산, 평균 계산 등이 최종 연산에 해당합니다.
    

스트림은 선언형 프로그래밍 스타일을 사용하며, 이를 통해 코드의 가독성을 향상시키고, 병렬처리를 쉽게 할 수 있게 됩니다. 이를 통해 개발자들은 데이터 처리에 집중할 수 있으며, 컴파일러와 런타임 시스템이 최적화를 자동으로 수행할 수 있습니다.

예를 들어, 정수 리스트에서 짝수만 필터링하고 각 값을 제곱한 후 결과를 리스트로 수집하는 코드는 다음과 같이 작성할 수 있습니다.

```java
import java.util.Arrays;
import java.util.List;
import java.util.stream.Collectors;

public class JavaStreamExample {
	public static void main(String[] args) {
		List<Integer> numbers = Arrays.asList(1, 2, 3, 4, 5, 6, 7, 8, 9, 10);    
		List<Integer> evenSquares = numbers.stream()
        .filter(n -> n % 2 == 0)
        .map(n -> n * n)
        .collect(Collectors.toList());

    System.out.println(evenSquares);
	}
}
```