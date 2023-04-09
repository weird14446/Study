<h1>Polymorphism</h1>

다형성은 객체 지향 프로그래밍의 핵심 원칙 중 하나로, 하나의 인터페이스나 클래스를 여러 개의 다른 형태로 구현하는 기능입니다. 파이썬에서 다형성은 동적 타이핑의 특성을 활용해 구현할 수 있습니다. 이를 통해 유연한 코드 작성이 가능하며, 클래스 간의 결합도를 낮춰 유지 보수와 확장성을 높입니다.

앞서 상속 예제에서 사용한 **`Animal`**, **`Dog`**, **`Cat`** 클래스를 사용하여 다형성을 설명하겠습니다. 다형성을 활용하여 동물들이 소리를 내는 함수를 작성해봅시다.

```python

def make_animals_speak(animals):
    for animal in animals:
        animal.make_sound()

```

이 함수는 **`Animal`** 클래스와 그 하위 클래스의 객체를 인자로 받아 소리를 내게 할 수 있습니다.

```python

dog = Dog("Buddy")
cat = Cat("Mittens")
bird = Animal("Tweety", "Bird")

animals = [dog, cat, bird]

make_animals_speak(animals)

```

위 코드를 실행하면 다음과 같은 결과를 얻습니다.

```

Woof!
Meow!
Some generic animal sound

```

**`make_animals_speak`** 함수는 인자로 주어진 객체의 타입이나 내부 구현에 관계없이 **`make_sound()`** 메서드를 호출할 수 있습니다. 이를 통해 코드가 유연하게 동작하며, 새로운 하위 클래스가 추가되더라도 기존 코드를 수정하지 않고도 해당 클래스의 객체를 처리할 수 있습니다.

이처럼 파이썬에서 다형성을 이용하면 객체의 실제 타입에 상관없이 메서드를 호출할 수 있어, 코드의 유연성과 확장성이 향상됩니다.
