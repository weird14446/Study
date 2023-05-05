# 추상 클래스

추상 클래스(abstract class)는 Java와 같은 객체 지향 프로그래밍 언어에서 중요한 개념입니다. 추상 클래스는 하나 이상의 추상 메소드(즉, 선언만 있고 구현이 없는 메소드)를 포함하는 클래스를 말합니다.

추상 클래스는 '미완성' 또는 '일반적인' 클래스라고 생각할 수 있으며, 다른 클래스가 상속을 통해 이를 '완성'하도록 설계되어 있습니다. 추상 클래스는 직접 인스턴스화 할 수 없습니다. 즉, 추상 클래스의 객체를 직접 생성할 수 없습니다.

추상 클래스는 **`abstract`** 키워드를 사용하여 선언됩니다. 아래에 추상 클래스의 예시를 보여드리겠습니다.

```java
public abstract class Animal {
    public abstract void makeSound();
}
```

여기서 **`Animal`** 은 추상 클래스이며, **`makeSound`** 는 추상 메소드입니다. **`makeSound`** 메소드는 선언만 있고 구현이 없습니다. 이 메소드의 구현은 **`Animal`** 클래스를 상속하는 하위 클래스에서 제공되어야 합니다.

예를 들어, **`Dog`** 와 **`Cat`** 클래스가 **`Animal`** 클래스를 상속하고, **`makeSound`** 메소드를 각각 구현하면 다음과 같습니다:

```java
public class Dog extends Animal {
    public void makeSound() {
        System.out.println("Woof");
    }
}

public class Cat extends Animal {
    public void makeSound() {
        System.out.println("Meow");
    }
}
```

각 하위 클래스는 **`makeSound`** 메소드를 자신의 방식으로 구현합니다. 이처럼 추상 클래스를 통해 공통의 특성과 메소드를 정의하고, 각 하위 클래스가 이를 자신의 방식으로 구현하도록 할 수 있습니다. 이는 코드의 재사용성을 높이고, 다형성을 지원하며, 유지보수를 용이하게 합니다.

## 인터페이스

인터페이스는 Java와 같은 객체 지향 프로그래밍 언어에서 중요한 개념입니다. 인터페이스는 메소드와 상수만을 포함할 수 있는 참조 타입입니다. 인터페이스는 메소드의 시그니처(즉, 메소드의 이름, 매개변수의 타입, 반환 타입)만을 정의하며, 이 메소드들의 구현은 인터페이스를 구현하는 클래스에서 제공됩니다.

인터페이스는 **`interface`** 키워드를 사용하여 정의됩니다. 예를 들어, 다음은 **`Animal`** 이라는 인터페이스를 정의하는 코드입니다:

```java
public interface Animal {
    void makeSound();
}
```

이 인터페이스에는 **`makeSound`** 라는 메소드가 정의되어 있지만, 메소드의 구현은 제공되지 않습니다. 이 메소드의 구현은 **`Animal`** 인터페이스를 구현하는 클래스에서 제공되어야 합니다.

```java
public class Dog implements Animal {
    public void makeSound() {
        System.out.println("Woof");
    }
}

public class Cat implements Animal {
    public void makeSound() {
        System.out.println("Meow");
    }
}
```

여기서 **`Dog`** 클래스와 **`Cat`** 클래스는 **`Animal`** 인터페이스를 구현하며, **`makeSound`** 메소드를 각자의 방식으로 구현합니다.

인터페이스는 다음과 같은 상황에서 주로 사용됩니다:

- 여러 클래스가 동일한 방식으로 동작하도록 강제하려는 경우
- 클래스와 독립적으로 메소드를 정의하려는 경우
- 여러 클래스 사이에서 메소드를 공유하려는 경우

인터페이스를 사용함으로써, 우리는 클래스의 행동을 정의하는 '계약'을 만들고, 이 '계약'을 따르는 클래스를 작성할 수 있습니다. 이는 코드의 일관성을 유지하고, 다형성을 지원하는 데 유용합니다.

인터페이스는 상수를 정의할 수 있습니다. 인터페이스의 필드는 자동으로 **`public`**, **`static`**, **`final`** 이 됩니다.

```java
public interface Constants {
    /*public static final*/ double PI = 3.14159;
}
```

인터페이스는 클래스와 객체의 설계를 위한 중요한 도구입니다. 클래스가 인터페이스를 구현함으로써, 해당 클래스가 어떤 메서드를 반드시 포함해야 하는지 정의할 수 있습니다. 이는 다형성을 지원하며, 특히 다른 개발자들이 코드를 사용하거나 유지 보수할 때 유용합니다.

## 내부 클래스

자바에서 내부 클래스(inner class)는 클래스 내부에 선언된 클래스입니다. 내부 클래스를 사용하면 코드의 복잡성을 줄이고, 캡슐화를 강화할 수 있습니다. 내부 클래스는 크게 4가지 종류가 있습니다.

1. **멤버 내부 클래스(member inner class):** 이는 일반 클래스 내부에 선언된 클래스로, 클래스의 멤버처럼 동작합니다. 멤버 내부 클래스는 외부 클래스의 모든 멤버(필드, 메서드)에 접근할 수 있습니다.

```java
class Outer {
    private int outerVariable = 10;

    class Inner {
        void print() {
            System.out.println("Outer variable: " + outerVariable);
        }
    }
}
```

2. **정적 내부 클래스(static inner class):** 멤버 내부 클래스에서 **`static`** 키워드를 사용한 클래스입니다. 정적 내부 클래스는 외부 클래스의 인스턴스에 종속되지 않고 독립적으로 동작합니다. 따라서 외부 클래스의 인스턴스 멤버에 접근할 수 없고, 오직 정적 멤버에만 접근할 수 있습니다.

```java
class Outer {
    private static int staticOuterVariable = 20;

    static class StaticInner {
        void print() {
            System.out.println("Static outer variable: " + staticOuterVariable);
        }
    }
}
```

3. **지역 내부 클래스(local inner class):** 메서드 내부에서 선언된 클래스입니다. 지역 내부 클래스는 메서드 내에서만 사용할 수 있으며, 메서드 내의 로컬 변수를 참조할 수 있지만, 로컬 변수는 **`final`** 또는 사실상 **`final`** 이어야 합니다.

```java
class Outer {
    void outerMethod() {
        int localVariable = 30;

        class LocalInner {
            void print() {
                System.out.println("Local variable: " + localVariable);
            }
        }

        LocalInner inner = new LocalInner();
        inner.print();
    }
}
```

4. **익명 내부 클래스(anonymous inner class):** 이름이 없는 클래스로, 클래스 선언과 객체 생성을 동시에 수행합니다. 주로 추상 클래스를 상속하거나 인터페이스를 구현할 때 사용되며, 주로 이벤트 리스너와 같은 작업에서 사용됩니다.

```java
interface Printable {
    void print();
}

class Outer {
    void createAnonymousInner() {
        Printable printable = new Printable() {
            @Override
            public void print() {
                System.out.println("Anonymous inner class");
            }
        };

        printable.print();
    }
}
```

이와 같이 내부 클래스는 코드의 가독성과 캡슐화를 향상시키는데 도움이 됩니다. 각 내부 클래스의 종류에 따라 다양한 상황에서 사용할 수 있습니다.