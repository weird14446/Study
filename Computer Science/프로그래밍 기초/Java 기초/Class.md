# 클래스

**클래스(Class)** 는 객체 지향 프로그래밍에서 중요한 개념으로, 객체를 생성하기 위한 틀 또는 설계도로 생각할 수 있습니다. 클래스는 상태(속성 또는 필드라고 함)와 행동(메소드)을 정의합니다.

자바에서 클래스는 다음과 같은 형식으로 선언됩니다:

```java
class ClassName {
    // fields
    // methods
}
```

예를 들어, 'Dog'라는 클래스를 생성하고자 한다면 다음과 같이 작성할 수 있습니다:

```java
class Dog {
    // 필드(상태)
    String breed;
    String color;
    int age;

    // 메소드(행동)
    void bark() {
        System.out.println("Woof-Woof");
    }

    void sleep() {
        System.out.println("Zzz");
    }
}
```

위의 **`Dog`** 클래스에는 **`breed`**, **`color`**, **`age`** 라는 세 가지 필드와 **`bark()`**, **`sleep()`** 라는 두 가지 메소드가 있습니다. 이 클래스는 개의 특징(품종, 색상, 나이)과 행동(짖음, 잠)을 모델링합니다.

이렇게 정의한 클래스를 바탕으로 개 객체를 생성하려면 **`new`** 키워드를 사용합니다:

```java
public class Main {
    public static void main(String[] args) {
        Dog myDog = new Dog();  // Dog 클래스의 인스턴스 생성

        // 필드에 값 할당
        myDog.breed = "Labrador";
        myDog.color = "Yellow";
        myDog.age = 3;

        // 메소드 호출
        myDog.bark();
        myDog.sleep();
    }
}
```

위의 코드에서 **`myDog`** 는 **`Dog`** 클래스의 인스턴스(또는 객체)입니다. 이 객체의 필드에 값을 할당하고, 메소드를 호출하여 개가 짖고 잠을 자는 행동을 시뮬레이션합니다.

## public class와 class의 차이

public class의 경우 클래스의 이름이 파일명과 일치해야 한다는 규칙 외에는 큰 차이점은 없습니다.

## 메소드

함수는 특정 작업을 수행하기 위한 코드 블록입니다. 함수는 입력을 받아서 처리하고, 그 결과를 출력(반환)할 수 있습니다.

이제 함수와 연관된 개념으로서 자바의 메소드를 이해해 봅시다.

메소드는 Java에서 매우 중요한 개념입니다. 메소드는 클래스 내부에 정의된 일련의 코드 블록으로, 특정 작업을 수행하거나 값을 반환합니다. 메소드는 객체의 행동을 정의하며, 클래스로부터 생성된 객체(인스턴스)가 사용할 수 있는 기능을 제공합니다.

메소드의 기본 구조는 다음과 같습니다:

```java
access_modifier return_type method_name(parameter_list) {
    // 메소드 본문
    // 작업 수행
    return value; // 반환형이 void가 아닌 경우
}
```

예를 들어, 두 숫자를 더하는 메소드를 정의하면 다음과 같이 됩니다:

```java
public class Addition {
    public int addNumbers(int a, int b) {
        int sum = a + b;
        return sum;
    }
}
```

이 메소드를 설명하자면:

- **`public`**: 접근 지정자입니다. 이 메소드는 공용으로 사용할 수 있음을 나타냅니다. 다른 클래스에서 이 메소드를 호출할 수 있습니다.
- **`int`**: 반환 타입입니다. 이 메소드가 호출된 후 반환하는 값의 데이터 타입을 나타냅니다. 이 경우에는 정수를 반환하므로 'int'입니다.
- **`addNumbers`**: 메소드의 이름입니다.
- **`(int a, int b)`**: 매개변수 목록입니다. 이 메소드는 두 개의 정수를 입력으로 받습니다.

메소드를 호출하려면 먼저 해당 메소드를 포함하는 클래스의 객체를 생성해야 합니다. 그리고 그 객체를 통해 메소드를 호출할 수 있습니다.

```java
public class Main {
    public static void main(String[] args) {
        Addition addition = new Addition(); // 객체 생성
        int result = addition.addNumbers(10, 20); // 메소드 호출
        System.out.println(result); // 결과 출력
    }
}
```

이 예제에서는 **`Addition`** 클래스의 객체 **`addition`** 을 생성하고, **`addNumbers`** 메소드를 호출하여 두 숫자(10과 20)를 더한 결과를 반환받아 출력합니다.

## void 타입

**`void`** 는 Java와 같은 여러 프로그래밍 언어에서 사용되는 특별한 키워드입니다. **`void`** 는 "값이 없음" 또는 "반환할 것이 없음"을 의미합니다.

메소드에서 **`void`** 는 해당 메소드가 어떠한 값을 반환하지 않는다는 것을 나타냅니다. 메소드는 종종 값을 계산하고 그 결과를 반환하는데 사용되지만, 모든 메소드가 값을 반환하는 것은 아닙니다. 어떤 메소드는 단지 어떤 작업을 수행하고, 결과를 반환하지 않습니다.

예를 들어, 메소드가 화면에 메시지를 출력하기만 하고, 어떤 값도 반환하지 않는다면 그 메소드의 반환 타입은 **`void`** 가 될 것입니다. 아래에 **`void`** 를 반환 타입으로 가지는 메소드의 예시를 보여드리겠습니다.

```java
public class HelloWorld {
    public void printMessage() {
        System.out.println("Hello, World!");
    }
}
```

이 예시에서 **`printMessage`** 메소드는 어떤 값을 반환하지 않습니다. 이 메소드의 목적은 단지 "Hello, World!"라는 메시지를 화면에 출력하는 것뿐입니다. 따라서 이 메소드의 반환 타입은 **`void`** 입니다.

## 메소드 오버로딩

메소드 오버로딩은 객체 지향 프로그래밍에서 중요한 특징 중 하나로, 같은 이름의 메소드를 여러 개 가질 수 있게 하는 기능입니다. 이런 메소드들은 매개변수의 타입, 개수, 순서 등이 다르며, 이를 통해 다양한 타입의 입력에 대응할 수 있습니다.

메소드 오버로딩의 주요 이점 중 하나는 코드의 가독성을 향상시키는 것입니다. 동일한 기능을 수행하지만 다양한 타입의 매개변수를 받는 메소드들에 대해 같은 이름을 사용함으로써, 프로그램의 일관성과 가독성이 향상됩니다.

Java에서 메소드 오버로딩의 예는 다음과 같습니다:

```java
public class OverloadExample {
    public void display(int a) {
        System.out.println("Arguments: " + a);
    }

    public void display(int a, int b) {
        System.out.println("Arguments: " + a + " and " + b);
    }

    public void display(String str) {
        System.out.println("Arguments: " + str);
    }
}
```

이 클래스에는 세 개의 **`display`** 메소드가 있지만, 각 메소드는 다른 타입이나 개수의 매개변수를 받습니다. 이것이 바로 메소드 오버로딩의 예입니다.

이러한 메소드들은 다음과 같이 호출할 수 있습니다:

```java
public class Main {
    public static void main(String[] args) {
        OverloadExample example = new OverloadExample();
        example.display(5);            // "Arguments: 5" 출력
        example.display(5, 10);        // "Arguments: 5 and 10" 출력
        example.display("Hello");      // "Arguments: Hello" 출력
    }
}
```

각 **`display`** 메소드 호출은 매개변수의 타입과 개수에 따라 적절한 메소드를 선택하여 실행합니다. 이것이 메소드 오버로딩의 주요 기능입니다.

## static 키워드

Java에서 **`static`** 키워드는 특정 멤버(필드나 메소드)가 클래스 수준에서 공유되어야 함을 나타냅니다. 즉, **`static`** 멤버는 특정 객체의 속성이 아니라 클래스의 속성이며, 이 클래스의 모든 객체에서 공유됩니다.

1. **Static 변수**: **`static`** 키워드가 붙은 변수는 클래스 변수라고도 부르며, 모든 객체가 공유하는 변수입니다. 클래스 변수는 객체가 생성되기 전에 초기화되며, 클래스가 로드될 때 한 번만 메모리를 할당받습니다.

예를 들어, 다음과 같은 **`Student`** 클래스를 생각해봅시다:

```java
public class Student {
    static int studentCount = 0;
    String name;

    public Student(String name) {
        this.name = name;
        studentCount++;
    }
}
```

여기서 **`studentCount`** 는 **`static`** 변수로서, **`Student`** 클래스의 모든 인스턴스에서 공유됩니다. 새로운 **`Student`** 객체를 생성할 때마다 **`studentCount`** 가 증가하여, 현재까지 생성된 **`Student`** 객체의 수를 추적합니다.

2. **Static 메소드**: **`static`** 키워드가 붙은 메소드는 클래스 메소드라고 부르며, 객체를 생성하지 않고도 호출할 수 있습니다. 클래스 메소드는 **`static`** 변수에만 접근할 수 있으며, **`this`** 키워드를 사용할 수 없습니다.

예를 들어, Java의 **`Math`** 클래스에 있는 **`sqrt`**, **`abs`** 등의 메소드는 모두 **`static`** 메소드입니다. 이 메소드들은 객체를 생성하지 않고도 바로 호출할 수 있습니다:

```java
double result = Math.sqrt(16);  // 객체 생성 없이 메소드 호출
```

또한, **`static`** 메소드는 주로 유틸리티나 헬퍼 함수를 작성하는 데 사용됩니다.

3. **Static 블록**: **`static`** 블록(또는 static 초기화 블록)은 클래스가 로드될 때 한 번만 실행되는 블록입니다. **`static`** 변수를 복잡한 방식으로 초기화해야 하는 경우에 주로 사용됩니다.

```java
public class MyClass {
    static int myVariable;

    static {
        // 복잡한 초기화 코드...
        myVariable = calculateInitialValue();
    }

    private static int calculateInitialValue() {
        // 복잡한 계산...
        return 42;
    }
}
```

4. **Static 클래스**: **`static`** 키워드는 내부 클래스에도 사용될 수 있습니다. **`static`** 내부 클래스는 외부 클래스의 인스턴스에 대한 참조를 가지지 않으며, 독립적으로 사용될 수 있습니다.

## main 메소드

Java에서 **`main`** 메소드는 프로그램의 진입점(entry point)입니다. 즉, Java 애플리케이션이 실행될 때 가장 먼저 호출되는 메소드입니다.

**`main`** 메소드의 선언은 다음과 같습니다:

```java
public static void main(String[] args) {
    // 프로그램 코드
}
```

이 선언에서 주요한 부분을 간단히 설명하면 다음과 같습니다:

- **`public`**: 이는 접근 지정자로, 메소드가 공개적으로 접근 가능함을 나타냅니다. **`main`** 메소드는 JVM(Java Virtual Machine)에서 애플리케이션을 시작할 때 호출되므로, 이 메소드는 반드시 **`public`** 으로 선언해야 합니다.
- **`static`**: 이 키워드는 **`main`** 메소드가 클래스의 인스턴스 없이 호출될 수 있음을 나타냅니다. 애플리케이션 시작 시점에 아직 어떤 객체도 생성되지 않았으므로, JVM은 **`static`** 메소드만 호출할 수 있습니다.
- **`void`**: 이는 메소드가 어떤 값을 반환하지 않음을 나타냅니다. **`main`** 메소드는 애플리케이션의 실행을 시작하는 용도로 사용되며, 특별히 반환할 값이 없습니다.
- **`main`**: 이는 메소드의 이름입니다. JVM은 **`main`** 이라는 이름의 메소드를 애플리케이션의 시작점으로 사용합니다.
- **`String[] args`**: 이는 메소드의 매개변수입니다. **`args`** 배열은 명령줄에서 전달된 인수를 포함합니다. 이를 통해 사용자는 애플리케이션을 시작할 때 추가적인 정보를 제공할 수 있습니다.

## 생성자와 소멸자

생성자(Constructor)는 Java에서 특별한 유형의 메소드로, 객체가 생성될 때 자동으로 호출되며, 객체의 초기 상태를 설정하는 데 사용됩니다. 생성자의 이름은 클래스의 이름과 같아야 하며, 반환 타입이 없습니다.

Java에서 객체를 생성할 때 **`new`** 키워드를 사용하는데, **`new`** 키워드 다음에 오는 것이 바로 생성자입니다.

예를 들어, 다음과 같은 **`Dog`** 클래스가 있다고 가정해봅시다.

```java
public class Dog {
    String name;
    String breed;
    int age;

    // 생성자
    public Dog(String name, String breed, int age) {
        this.name = name;
        this.breed = breed;
        this.age = age;
    }
}
```

위의 **`Dog`** 클래스에서, **`Dog(String name, String breed, int age)`** 는 생성자입니다. 이 생성자는 **`Dog`** 객체가 생성될 때 호출되며, **`name`**, **`breed`**, **`age`** 필드를 초기화합니다.

객체를 생성하려면 다음과 같이 생성자를 호출해야 합니다.

```java
Dog myDog = new Dog("Rover", "Labrador", 3);
```

위의 코드에서, **`new Dog("Rover", "Labrador", 3);`** 부분이 **`Dog`** 클래스의 생성자를 호출하고 있습니다. 이 호출로 인해 **`Dog`** 객체가 생성되고, 그 필드는 주어진 인수로 초기화됩니다.

만약 클래스에 생성자를 명시적으로 정의하지 않으면, Java 컴파일러는 아무 인수도 받지 않고 아무 것도 하지 않는 기본 생성자(Default Constructor)를 자동으로 추가합니다. 그러나 클래스에 한 개 이상의 생성자를 명시적으로 정의하면, 컴파일러는 기본 생성자를 추가하지 않습니다. 이 경우 필요하다면 직접 기본 생성자를 정의해야 합니다.

Java에서는 "소멸자"라는 개념이 직접적으로 존재하지 않습니다. C++와 같은 언어에서는 객체가 소멸될 때 소멸자(destructor)가 호출되어 객체의 리소스를 해제하는 역할을 합니다. 그러나 Java는 가비지 컬렉터(Garbage Collector)라는 메모리 관리 시스템을 가지고 있어, 개발자가 명시적으로 메모리를 해제할 필요가 없습니다.

가비지 컬렉터는 자동으로 동작하며, 더 이상 참조되지 않는 객체를 찾아 메모리를 해제합니다. 이 과정은 Java 런타임 시스템에서 자동으로 수행되므로, Java 개발자는 일반적으로 소멸자에 대해 걱정할 필요가 없습니다.

그러나 Java에서는 finalize() 메소드라는 것이 존재합니다. 이 메소드는 객체가 가비지 컬렉션을 위해 선택될 때 JVM(Java Virtual Machine)에 의해 호출됩니다. 이를 일종의 "소멸자"로 간주할 수 있지만, finalize() 메소드의 사용은 권장되지 않습니다. 왜냐하면 finalize() 메소드의 실행 시점과 실행 여부는 JVM에 의해 결정되므로 예측할 수 없기 때문입니다. 따라서, 보다 명확한 리소스 해제가 필요한 경우, try-with-resources나 finally 블록을 이용해 명시적으로 리소스를 해제하는 것이 좋습니다.

## 상속

상속은 객체 지향 프로그래밍에서 중요한 개념 중 하나입니다. 상속은 한 클래스가 다른 클래스의 속성과 메소드를 물려받는 메커니즘을 말합니다. 이를 통해 코드의 재사용성을 높이고, 구조화된 코드를 작성하는데 도움을 줍니다.

Java에서, 클래스의 상속은 **`extends`** 키워드를 사용하여 이루어집니다. 예를 들어, 우리는 **`Animal`** 이라는 기본 클래스(base class 또는 superclass)가 있고, 이를 상속받는 **`Dog`** 라는 파생 클래스(derived class 또는 subclass)를 만들 수 있습니다.

```java
public class Animal {
    public void eat() {
        System.out.println("This animal eats food.");
    }
}

public class Dog extends Animal {
    public void bark() {
        System.out.println("The dog barks.");
    }
}
```

여기서 **`Dog`** 클래스는 **`Animal`** 클래스를 상속하므로, **`Dog`** 클래스는 **`Animal`** 클래스의 모든 메소드(여기서는 **`eat`** 메소드)를 사용할 수 있습니다.

```java
public class Main {
    public static void main(String[] args) {
        Dog myDog = new Dog();
        myDog.eat();  // "This animal eats food." 출력
        myDog.bark(); // "The dog barks." 출력
    }
}
```

이 예제에서 **`Dog`** 객체는 **`Dog`** 클래스의 **`bark`** 메소드와 **`Animal`** 클래스로부터 상속받은 **`eat`** 메소드 모두를 사용할 수 있습니다.

상속은 "is-a" 관계를 표현합니다. 예를 들어, **`Dog`**은 **`Animal`**입니다. 이를 통해 우리는 보다 일반적인 클래스(**`Animal`**)에서 특화된 클래스(**`Dog`**)로 코드를 구조화하고, 코드를 재사용하며, 유지 관리를 용이하게 할 수 있습니다.

## 클래스-객체-인스턴스

1. **클래스(Class)**: 클래스는 객체를 생성하기 위한 템플릿 또는 청사진입니다. 클래스는 객체의 상태를 나타내는 필드(변수)와 객체의 행동을 나타내는 메소드(함수)를 정의합니다. 예를 들어, "Dog"라는 클래스를 생각해봅시다. "Dog" 클래스는 "name", "breed", "age"와 같은 필드와 "bark", "eat", "sleep"와 같은 메소드를 가질 수 있습니다.

```java
public class Dog {
    // 필드
    String name;
    String breed;
    int age;

    // 메소드
    public void bark() {
        System.out.println("Woof!");
    }

    public void eat() {
        // ...
    }

    public void sleep() {
        // ...
    }
}
```

2. **객체(Object)**: 객체(Object): 객체는 클래스에 정의된 대로 생성된 실체를 의미합니다. 객체는 클래스로부터 상속받은 속성과 메서드를 가집니다. 객체는 클래스의 인스턴스라고도 합니다.
3. **인스턴스(Instance)**: 인스턴스는 메모리 공간에 할당된 객체를 말합니다. '인스턴스화'는 클래스의 객체를 생성하는 과정을 의미하며, new 키워드를 통해 생성됩니다. 이 과정을 통해 클래스의 새로운 '인스턴스'가 만들어집니다. 객체와 인스턴스는 종종 동의어로 사용되지만, 보통은 객체가 클래스의 인스턴스임을 강조할 때 '인스턴스'라는 용어를 사용합니다.

```java
Dog myDog = new Dog();  // 'Dog' 클래스의 새로운 인스턴스 생성
```

여기서 **`myDog`** 는 **`Dog`** 클래스의 객체이며, **`Dog`** 클래스의 인스턴스입니다. 이 객체는 **`Dog`** 클래스의 상태와 행동을 가지며, 이는 **`Dog`** 클래스가 정의하는 대로입니다.

## this 키워드

Java에서 **`this`** 키워드는 현재 객체의 참조를 나타냅니다. **`this`** 는 주로 다음과 같은 상황에서 사용됩니다:

1. **필드와 지역 변수의 이름 충돌 해결**: 메소드 내에서 필드와 동일한 이름의 매개변수 또는 지역 변수가 있을 때, 필드와 지역 변수를 구별하기 위해 사용됩니다.

예를 들어, 다음과 같은 **`Person`** 클래스를 생각해봅시다.

```java
public class Person {
    String name;

    public void setName(String name) {
        this.name = name;
    }
}
```

여기서 **`setName`** 메소드의 매개변수 이름이 필드 **`name`** 과 같습니다. **`this.name`** 을 사용하여 현재 객체의 **`name`** 필드를 참조하고, 매개변수로 전달된 값을 설정합니다.

2. **현재 객체의 다른 메소드나 생성자를 호출**: **`this`** 를 사용하여 현재 객체 내의 다른 메소드나 생성자를 호출할 수 있습니다.

예를 들어, 다음과 같은 **`Student`** 클래스를 생각해봅시다.

```java
public class Student {
    String name;
    int age;

    public Student() {
        this("Unknown", 0); // 현재 객체의 다른 생성자 호출
    }

    public Student(String name, int age) {
        this.name = name;
        this.age = age;
    }

    public void printInfo() {
        System.out.println("Name: " + name + ", Age: " + age);
        this.printGreeting(); // 현재 객체의 다른 메소드 호출
    }

    public void printGreeting() {
        System.out.println("Hello, I am " + name);
    }
}
```

여기서 기본 생성자 **`Student()`** 에서 **`this("Unknown", 0)`** 을 사용하여 현재 객체의 다른 생성자를 호출하고 있습니다. 또한, **`printInfo`** 메소드에서 **`this.printGreeting()`** 을 사용하여 현재 객체의 다른 메소드를 호출하고 있습니다.

**`this`** 키워드는 현재 객체에 대한 참조를 제공하므로, 객체의 필드나 메소드에 접근하는 데 유용하게 사용됩니다.