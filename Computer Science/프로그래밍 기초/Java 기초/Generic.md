# 제네릭

자바의 제네릭(Generic)은 클래스나 메소드에서 사용할 내부 데이터 타입을 컴파일 시에 미리 지정하는 방법입니다. 이는 타입 안정성을 보장하고 불필요한 타입 변환을 줄여주므로 코드를 더 안전하고 명확하게 작성할 수 있게 합니다.

제네릭은 대괄호 **`< >`** 안에 타입 매개변수를 넣어 표현합니다. 예를 들어, **`List`** 인터페이스를 사용할 때 제네릭을 사용하면 다음과 같습니다:

```java
List<String> list = new ArrayList<String>();
list.add("hello");
String str = list.get(0);  // 형변환 불필요
```

여기서 **`List<String>`** 은 "String 객체들의 리스트"를 의미합니다. **`list.get(0)`** 은 리스트의 첫 번째 요소를 가져오며, 이는 String 타입이므로 별도의 형변환을 하지 않아도 됩니다.

클래스나 인터페이스를 정의할 때도 제네릭을 사용할 수 있습니다:

```java
public class Pair<K, V> {
    private K key;
    private V value;

    public Pair(K key, V value) {
        this.key = key;
        this.value = value;
    }

    public void setKey(K key) { this.key = key; }
    public void setValue(V value) { this.value = value; }
    public K getKey() { return key; }
    public V getValue() { return value; }
}
```

위의 **`Pair`** 클래스는 두 종류의 타입 파라미터 **`K`** 와 **`V`** 를 사용합니다. 이를 통해 어떤 타입의 쌍이라도 저장할 수 있는 범용 쌍 클래스를 만들 수 있습니다. 이처럼 제네릭은 코드의 재사용성을 높이는 데도 유용합니다.

제네릭은 컴파일 시점에 타입 체크를 수행하기 때문에, 타입 오류를 런타임이 아닌 컴파일 시점에서 잡아낼 수 있는 장점이 있습니다. 그러나 제네릭 코드는 조금 복잡해질 수 있으며, 이해하고 사용하는 데 약간의 학습 곡선이 필요합니다.

제네릭 메서드는 메서드의 선언에 하나 이상의 타입 매개변수가 포함된 메서드를 말합니다. 이 타입 매개변수들은 메서드의 반환 타입과 매개변수 타입을 정의하는 데 사용됩니다. 제네릭 메서드는 다양한 데이터 타입에 대해 동작을 수행할 수 있어, 재사용성을 높이는 데 도움이 됩니다.

제네릭 메서드는 다음과 같이 선언됩니다:

```java
public <T> void myMethod(T param) {
  // ...
}
```

여기서 **`<T>`** 는 타입 매개변수를 나타냅니다. 이 **`T`** 는 메서드 내에서 마치 실제 클래스처럼 사용될 수 있습니다.

다음은 제네릭 메서드의 예시입니다:

```java
public class GenericMethodExample {
    // 제네릭 메서드 선언
    public static <T> void printArray(T[] array) {
        for (T element : array) {
            System.out.println(element);
        }
    }

    public static void main(String[] args) {
        // Integer 배열 사용
        Integer[] intArray = {1, 2, 3, 4, 5};
        printArray(intArray);

        // Double 배열 사용
        Double[] doubleArray = {1.1, 2.2, 3.3, 4.4};
        printArray(doubleArray);

        // Character 배열 사용
        Character[] charArray = {'H', 'E', 'L', 'L', 'O'};
        printArray(charArray);
    }
}
```

위의 예시에서 **`printArray`** 메서드는 어떤 타입의 배열이든 받아서 각 요소를 출력할 수 있습니다. 이처럼 제네릭 메서드를 사용하면 유연하고 재사용 가능한 코드를 작성할 수 있습니다.

자바의 제네릭(Generic)은 클래스, 인터페이스, 메서드에서 사용할 내부 데이터 타입을 컴파일 시에 미리 지정하는 방법입니다. 제네릭을 사용하면 코드의 타입 안정성을 확보하고 불필요한 타입 변환을 줄일 수 있습니다.

제네릭은 다음과 같은 장점이 있습니다:

1. 타입 안정성: 컴파일 시점에 잘못된 타입 사용을 찾아낼 수 있습니다. 이를 통해 런타임에 발생할 수 있는 오류를 줄일 수 있습니다.
2. 코드 재사용: 제네릭을 사용하면 같은 코드를 다양한 타입에 대해 사용할 수 있으므로, 코드 중복을 줄이고 유지 보수성을 높일 수 있습니다.
3. 형변환 감소: 제네릭을 사용하면 명시된 타입에 대한 형변환이 자동으로 이루어져 별도의 형변환 코드를 작성할 필요가 없습니다.

**제네릭 클래스와 인터페이스**

제네릭 클래스나 인터페이스는 타입 매개변수를 사용하여 정의됩니다. 타입 매개변수는 일반적으로 대문자 알파벳 한 글자로 표현되며, 대괄호 **`< >`** 로 묶어 표시합니다.

```java
public class Box<T> {
    private T content;

    public void setContent(T content) {
        this.content = content;
    }

    public T getContent() {
        return content;
    }
}
```

위의 예시에서 **`Box`** 클래스는 타입 매개변수 **`T`**를 사용합니다. 이를 사용하면 **`Box`** 클래스는 다양한 타입의 객체를 저장할 수 있습니다.

**제네릭 메서드**

제네릭 메서드는 메서드 선언에 타입 매개변수를 포함한 메서드입니다.

```java
public <T> void printArray(T[] array) {
    for (T element : array) {
        System.out.println(element);
    }
}
```

위의 예시에서 **`printArray`** 메서드는 타입 매개변수 **`T`** 를 사용하여 다양한 타입의 배열을 인자로 받아 출력할 수 있습니다.

**와일드카드**

와일드카드는 제네릭 타입을 표현할 때, 모든 타입을 허용하고 싶을 때 사용하는 특별한 매개변수입니다. 와일드카드는 물음표 **`?`**로 표현합니다.

예를 들어, 아래와 같이 사용할 수 있습니다:

```java
List<?> list;
```

이 코드는 "어떠한 타입이든 올 수 있는 List"를 의미합니다. 즉, **`List<String>`**, **`List<Integer>`**, **`List<Object>`** 등 어떤 타입의 리스트든 변수 **`list`**에 할당될 수 있습니다.

와일드카드는 제한된 와일드카드(upper bounded wildcard)와 비제한 와일드카드(lower bounded wildcard) 두 가지 형태로 사용할 수 있습니다.

**제한된 와일드카드(upper bounded wildcard)**

제한된 와일드카드는 특정 타입 또는 그 타입의 하위 클래스만 허용하도록 제한합니다. 이를 위해 **`? extends T`** 구문을 사용합니다.

예를 들어, 아래와 같이 사용할 수 있습니다:

```java
List<? extends Number> numbers;
```

이 코드는 "Number 또는 그 하위 클래스 타입의 List"를 의미합니다. 즉, **`List<Integer>`**, **`List<Double>`** 등 Number의 하위 타입 리스트를 **`numbers`**에 할당할 수 있습니다.

**비제한 와일드카드(lower bounded wildcard)**

비제한 와일드카드는 특정 타입 또는 그 타입의 상위 클래스만 허용하도록 제한합니다. 이를 위해 **`? super T`** 구문을 사용합니다.

예를 들어, 아래와 같이 사용할 수 있습니다:

```java
List<? super Integer> numbers;
```

이 코드는 "Integer 또는 그 상위 클래스 타입의 List"를 의미합니다. 즉, **`List<Integer>`**, **`List<Number>`**, **`List<Object>`** 등 Integer의 상위 타입 리스트를 **`numbers`**에 할당할 수 있습니다.

제한된 와일드카드와 비제한 와일드카드는 제네릭의 유연성을 높여줍니다. 이를 통해 더 넓은 범위의 타입을 안전하게 처리할 수 있습니다.