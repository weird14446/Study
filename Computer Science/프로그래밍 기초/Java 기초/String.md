# String

자바(Java)에서 문자열(String)은 일련의 문자들로 이루어진 데이터 형태를 나타냅니다. 자바에서 문자열을 다루기 위해 **`String`**이라는 클래스를 사용합니다. **`String`** 클래스는 문자열 데이터를 저장하고, 문자열 관련 작업을 수행할 수 있는 다양한 메소드를 제공합니다.

문자열을 생성하고 사용하는 방법은 다음과 같습니다.

## 문자열 기초

1. 문자열 리터럴을 사용하여 문자열 생성하기:

```java
String example = "Hello, World!";
```

이 방식은 문자열 리터럴을 직접 사용하여 **`String`** 객체를 생성합니다. 이 경우, 자바는 동일한 문자열 리터럴을 가진 **`String`** 객체를 공유하여 메모리 사용을 최적화합니다.

2. **`String`** 클래스의 생성자를 사용하여 문자열 생성하기:

```java
String example = new String("Hello, World!");
```

이 방식은 **`new`** 키워드와 함께 **`String`** 생성자를 사용하여 새로운 **`String`** 객체를 생성합니다. 이 경우, 각 객체는 별도의 메모리 공간에 저장됩니다.

**`String`** 클래스는 불변(immutable)입니다. 즉, 한 번 생성된 문자열은 변경할 수 없습니다. 문자열에 대한 수정 작업이 필요한 경우, **`StringBuilder`** 또는 **`StringBuffer`** 와 같은 가변(mutable) 문자열 클래스를 사용할 수 있습니다.

자바의 **`String`** 클래스는 문자열을 조작하고 처리하는 데 필요한 다양한 메소드를 제공합니다. 예를 들어, **`length()`**, **`charAt()`**, **`substring()`**, **`indexOf()`**, **`startsWith()`**, **`endsWith()`**, **`equals()`**, **`equalsIgnoreCase()`**, **`replace()`**, **`toLowerCase()`**, **`toUpperCase()`** 등이 있습니다.

다음은 자바에서 문자열을 사용하는 간단한 예제입니다:

```java
public class Main {
    public static void main(String[] args) {
        String hello = "Hello, ";
        String world = "World!";

        // 문자열 결합
        String message = hello + world;
        System.out.println(message); // 출력: Hello, World!

        // 문자열 길이
        int length = message.length();
        System.out.println("Length: " + length); // 출력: Length: 13

        // 부분 문자열 추출
        String substring = message.substring(0, 5);
        System.out.println(substring); // 출력: Hello
    }
	}
```

이 예제에서는 문자열을 생성하고, 결합하고, 길이를 구하고, 부분 문자열을 추출하는 방법을 보여줍니다. 

## 문자열 변환

**`String`** 클래스는 문자열을 소문자로 변환하는 **`toLowerCase()`** 메소드와 대문자로 변환하는 **`toUpperCase()`** 메소드를 제공합니다.

다음은 소문자와 대문자 변환 메소드를 사용하는 예제입니다:

```java
public class Main {
    public static void main(String[] args) {
        String example = "Hello, World!";

        // 대문자로 변환
        String upperCaseExample = example.toUpperCase();
        System.out.println(upperCaseExample); // 출력: HELLO, WORLD!

        // 소문자로 변환
        String lowerCaseExample = example.toLowerCase();
        System.out.println(lowerCaseExample); // 출력: hello, world!
    }
}
```

이 예제에서는 **`toUpperCase()`** 메소드를 사용하여 문자열을 대문자로 변환하고, **`toLowerCase()`** 메소드를 사용하여 문자열을 소문자로 변환합니다. 변환된 문자열은 원래 문자열과 다른 메모리 공간에 저장되며, 원래 문자열은 변경되지 않습니다. 이는 **`String`** 클래스가 불변(immutable)이기 때문입니다.

이러한 메소드를 사용하여 자바에서 소문자와 대문자 변환 작업을 쉽게 수행할 수 있습니다. 필요한 경우 두 메소드를 조합하여 복잡한 문자열 처리 작업을 수행할 수도 있습니다.

## 문자열 포함 관계

문자열의 포함 관계는 한 문자열이 다른 문자열 내에 포함되어 있는지를 확인하는 것입니다. 자바에서는 **`String`** 클래스의 **`contains()`** 메소드나 **`indexOf()`** 메소드를 사용하여 문자열의 포함 관계를 확인할 수 있습니다.

1. **`contains()`** 메소드를 사용한 문자열 포함 관계 확인:

**`contains()`** 메소드는 문자열에 특정 문자열이 포함되어 있는지 확인합니다. 이 메소드는 찾으려는 문자열이 포함되어 있다면 **`true`** 를 반환하고, 그렇지 않으면 **`false`** 를 반환합니다.

예제:

```java
public class Main {
    public static void main(String[] args) {
        String example = "Hello, World!";
        String search = "World";

        boolean contains = example.contains(search);
        System.out.println(contains); // 출력: true
    }
}
```

2. **`indexOf()`** 메소드를 사용한 문자열 포함 관계 확인:

**`indexOf()`** 메소드는 찾으려는 문자열이 주어진 문자열 내에서 처음 등장하는 인덱스를 반환합니다. 찾는 문자열이 없으면 **`-1`** 을 반환합니다. 이를 통해 문자열이 다른 문자열에 포함되어 있는지 확인할 수 있습니다.

예제:

```java
public class Main {
    public static void main(String[] args) {
        String example = "Hello, World!";
        String search = "World";

        int index = example.indexOf(search);
        if (index != -1) {
            System.out.println("Found at index: " + index); // 출력: Found at index: 7
        } else {
            System.out.println("Not found");
        }
    }
}
```

이러한 메소드를 사용하여 문자열의 포함 관계를 확인할 수 있습니다. 필요에 따라 이 메소드들을 사용하여 문자열을 처리하고 분석하는 복잡한 작업을 수행할 수도 있습니다.

## 문자열 비교

자바에서 문자열을 비교하는 방법은 주로 두 가지입니다: **`equals()`** 메소드와 **`compareTo()`** 메소드를 사용하는 방법입니다.

1. **`equals()`** 메소드를 사용한 문자열 비교:

**`equals()`** 메소드는 두 문자열이 동일한지를 확인합니다. 이 메소드는 두 문자열이 정확히 같은 문자로 구성되어 있다면 **`true`** 를 반환하고, 그렇지 않으면 **`false`** 를 반환합니다. 이 메소드를 사용하면 대소문자를 구분하여 문자열을 비교할 수 있습니다.

예제:

```java
public class Main {
    public static void main(String[] args) {
        String str1 = "Hello, World!";
        String str2 = "Hello, World!";
        String str3 = "hello, world!";

        boolean isEqual1 = str1.equals(str2);
        System.out.println(isEqual1); // 출력: true

        boolean isEqual2 = str1.equals(str3);
        System.out.println(isEqual2); // 출력: false
    }
}
```

또한 **`equalsIgnoreCase()`** 메소드를 사용하면 대소문자를 무시하고 문자열을 비교할 수 있습니다.

2. **`compareTo()`** 메소드를 사용한 문자열 비교:

**`compareTo()`** 메소드는 두 문자열을 사전식(사전 순서)으로 비교합니다. 이 메소드는 첫 번째 문자열이 두 번째 문자열보다 사전적으로 앞에 있으면 음수를, 동일하면 0을, 뒤에 있으면 양수를 반환합니다. 이 메소드를 사용하면 문자열의 순서를 비교할 수 있습니다.

예제:

```java
public class Main {
    public static void main(String[] args) {
        String str1 = "apple";
        String str2 = "banana";
        String str3 = "apple";

        int result1 = str1.compareTo(str2);
        System.out.println(result1); // 출력: 음수 (apple이 banana보다 사전적으로 앞에 있음)

        int result2 = str1.compareTo(str3);
        System.out.println(result2); // 출력: 0 (두 문자열이 동일함)
    }
}
```

**`compareToIgnoreCase()`** 메소드를 사용하면 대소문자를 무시하고 사전식 순서로 문자열을 비교할 수 있습니다.

이러한 메소드들을 사용하여 자바에서 문자열을 비교할 수 있습니다. 필요에 따라 이 메소드들을 사용하여 문자열을 처리하고 분석하는 복잡한 작업을 수행할 수도 있습니다.

## Escape character

자바에서 탈출 문자(escape character)는 특수한 문자를 문자열 내에 삽입하거나 표현할 때 사용하는 문자입니다. 탈출 문자는 백슬래시 **`\`**로 시작하며, 이후에 특정 문자가 옵니다. 탈출 문자를 사용하면 일반적으로 문자열에서 인식되지 않는 특수 문자를 표현할 수 있습니다.

자바에서 주로 사용되는 탈출 문자는 다음과 같습니다:

1. **`\"`**: 큰따옴표를 문자열 내에 포함할 때 사용합니다.
2. **`\'`**: 작은따옴표를 문자열 내에 포함할 때 사용합니다.
3. **`\\`**: 백슬래시를 문자열 내에 포함할 때 사용합니다.
4. **`\n`**: 줄 바꿈(newline) 문자를 표현할 때 사용합니다.
5. **`\r`**: 캐리지 리턴(carriage return) 문자를 표현할 때 사용합니다.
6. **`\t`**: 탭(tab) 문자를 표현할 때 사용합니다.
7. **`\b`**: 백스페이스(backspace)를 할 때 사용합니다. (한 글자 삭제)

다음은 자바에서 탈출 문자를 사용하는 예제입니다:

```java
public class Main {
    public static void main(String[] args) {
        // 큰따옴표를 포함한 문자열
        String quote = "She said, \"Hello, World!\"";
        System.out.println(quote); // 출력: She said, "Hello, World!"

        // 줄 바꿈과 탭 문자를 포함한 문자열
        String text = "This is the first line.\n\tThis is the second line with a tab.";
        System.out.println(text);
        // 출력:
        // This is the first line.
        //     This is the second line with a tab.
    }
}
```

탈출 문자를 사용하면 자바에서 특수한 문자를 문자열 내에 삽입하거나 표현할 수 있습니다. 이를 통해 문자열을 처리하고 표시하는 데 필요한 다양한 작업을 수행할 수 있습니다.