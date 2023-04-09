<h1>Abstraction</h1>

추상화는 객체 지향 프로그래밍의 핵심 원칙 중 하나로, 복잡한 시스템을 간단한 인터페이스로 표현하는 것을 의미합니다. 파이썬에서는 추상 클래스와 추상 메서드를 사용하여 추상화를 구현할 수 있습니다.

추상 클래스는 인스턴스화되지 않은 채로 다른 클래스에서 상속받아 구현되어야 하는 메서드를 정의하는 틀 역할을 합니다. 파이썬에서 추상 클래스를 사용하려면 **`abc`** 모듈의 **`ABC`** 클래스와 **`abstractmethod`** 데코레이터를 활용합니다.

예를 들어, 도형의 기본 특성과 행동을 나타내는 추상 클래스를 만들고, 이를 상속받아 특정 도형을 나타내는 클래스를 만들 수 있습니다.

먼저, 추상 클래스인 **`Shape`** 를 작성합니다.

```python

from abc import ABC, abstractmethod

class Shape(ABC):
    @abstractmethod
    def area(self):
        pass

    @abstractmethod
    def perimeter(self):
        pass

```

이제 **`Rectangle`** 와 **`Circle`** 클래스를 만들어 **`Shape`** 추상 클래스를 상속받습니다.

```python

class Rectangle(Shape):
    def __init__(self, width, height):
        self.width = width
        self.height = height

    def area(self):
        return self.width * self.height

    def perimeter(self):
        return 2 * (self.width + self.height)

class Circle(Shape):
    def __init__(self, radius):
        self.radius = radius

    def area(self):
        return 3.141592 * (self.radius ** 2)

    def perimeter(self):
        return 2 * 3.141592 * self.radius

```

여기서 **`Rectangle`** 와 **`Circle`** 클래스는 **`Shape`** 추상 클래스를 상속받아 **`area`** 와 **`perimeter`** 메서드를 구현합니다.

이제 **`Rectangle`** 와 **`Circle`** 객체를 생성하고 메서드를 사용해 봅시다.

```python

rect = Rectangle(4, 5)
print(rect.area())  # 20
print(rect.perimeter())  # 18

circle = Circle(3)
print(circle.area())  # 28.274328...
print(circle.perimeter())  # 18.849552...

```

추상화를 사용하면 공통 인터페이스를 정의하여 구체적인 구현을 감추고, 간단한 인터페이스를 통해 상호작용할 수 있습니다. 이를 통해 코드의 가독성과 유지 보수성을 높일 수 있습니다.
