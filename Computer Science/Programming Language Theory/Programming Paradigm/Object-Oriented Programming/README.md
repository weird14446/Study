<h1>Object-Oriented Programming.</h1>

객체지향 프로그래밍(Object-Oriented Programming, OOP)은 프로그래밍 패러다임 중 하나로, 소프트웨어 개발에서 객체라는 개념을 중심으로 하는 방법론입니다. 객체지향 프로그래밍의 주요 목표는 코드의 재사용성, 확장성 및 유지 보수의 용이성을 높이는 것입니다. 이를 위해 객체지향 프로그래밍은 다음과 같은 원칙과 특성을 가집니다.

1. [캡슐화](https://github.com/weird14446/Study/blob/main/Computer%20Science/Programming%20Language%20Theory/Programming%20Paradigm/Object-Oriented%20Programming/Encapsulation.md)(Encapsulation): 객체의 속성(데이터)과 행위(메서드)를 하나의 단위로 묶는 과정입니다. 이를 통해 객체의 내부 구현을 숨기고, 외부에서는 해당 객체와 상호작용하기 위한 인터페이스만 제공합니다. 캡슐화는 데이터와 메서드를 함께 묶어 관리할 수 있게 하여 코드의 가독성과 유지 보수를 용이하게 합니다.
2. [상속](https://github.com/weird14446/Study/blob/main/Computer%20Science/Programming%20Language%20Theory/Programming%20Paradigm/Object-Oriented%20Programming/Inheritance.md)(Inheritance): 기존 클래스의 속성과 메서드를 새로운 클래스에서 재사용할 수 있게 하는 기능입니다. 상속을 통해 기존 코드를 확장하거나 수정할 수 있어 중복 코드를 줄이고 재사용성을 높입니다.
3. [다형성](https://github.com/weird14446/Study/blob/main/Computer%20Science/Programming%20Language%20Theory/Programming%20Paradigm/Object-Oriented%20Programming/Polymorphism.md)(Polymorphism): 하나의 인터페이스나 클래스를 여러 개의 다른 형태로 구현하는 기능입니다. 다형성을 통해 유연한 코드 작성이 가능하며, 클래스 간의 결합도를 낮춰 유지 보수와 확장성을 높입니다.
4. [추상화](https://github.com/weird14446/Study/blob/main/Computer%20Science/Programming%20Language%20Theory/Programming%20Paradigm/Object-Oriented%20Programming/Abstraction.md)(Abstraction): 복잡한 시스템을 단순한 개념으로 표현하는 과정입니다. 객체지향 프로그래밍에서 추상화는 인터페이스, 추상 클래스 등의 형태로 나타납니다. 추상화를 통해 개발자는 세부 구현에 신경 쓰지 않고 전체 시스템의 구조와 흐름에 집중할 수 있습니다.

객체지향 프로그래밍은 여러 가지 언어에서 지원되며, 대표적인 객체지향 프로그래밍 언어로는 Java, C++, C#, Python, Ruby 등이 있습니다. 객체지향 프로그래밍은 이러한 원칙과 특성을 바탕으로 소프트웨어 개발 과정에서 코드의 재사용성, 유지 보수성 및 확장성을 향상시키는 데 도움이 됩니다.

## SOLID 원칙

SOLID 원칙은 객체지향에서 지켜야할 원칙 5가지 원칙을 말합니다. 5가지 원칙은 다음과 같습니다.

1. Single Responsibility Principle(단일 책임 원칙, SRP) : 객체는 오직 하나의 책임을 가져야 한다는 원칙입니다.
2. Open Closed Principle(개방 폐쇄 원칙, OCP) : 객체는 확장에 대해서는 개방적이고 수정에 대해서는 폐쇄적이여야 한다는 원칙입니다.
3. Liskov Substitution Principle(리스코프 치환 원칙, LSP) : 자식 클래스는 언제나 부모 클래스를 대체할 수 있다는 원칙입니다. 상속의 본질적인 원칙입니다.
4. Interface Segregation Principle(인터페이스 분리 원칙, ISP) : 하나의 일반적인 인터페이스보다는 여러개의 구체적인 인터페이스가 낫다는 원칙입니다.
5. Dependency Inversion Principle(의존관계 역전 원칙, DIP) : 구체화에 의존하지 않고, 추상화에 의존해야 한다는 원칙입니다.
