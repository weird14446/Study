# Polymorphism

다형성(polymorphism)은 객체 지향 프로그래밍(OOP)의 핵심 원칙 중 하나로, 여러 다른 유형의 객체가 동일한 인터페이스나 추상 기본 클래스를 구현하거나 상속함으로써 동일한 이름의 메서드를 호출해도 다양한 행동을 보일 수 있게 하는 개념입니다.

다형성의 목적은 코드의 유연성과 재사용성을 높이는 것입니다. 다형성을 사용하면 하나의 인터페이스나 기본 클래스를 사용하여 다양한 객체 유형을 처리할 수 있으며, 새로운 객체 유형을 추가할 때 기존 코드를 변경하지 않고도 쉽게 적용할 수 있습니다.

다음은 파이썬에서 다형성을 구현하는 예시입니다:

```python
class Animal:
    def make_sound(self):
        pass

class Dog(Animal):
    def make_sound(self):
        return "Woof!"

class Cat(Animal):
    def make_sound(self):
        return "Meow!"

def play_sound(animal):
    print(animal.make_sound())

dog = Dog()
cat = Cat()

play_sound(dog)  # 출력: Woof!
play_sound(cat)  # 출력: Meow!
```
위 예시에서 Animal 클래스는 make_sound라는 메서드를 정의하고 있습니다. Dog와 Cat 클래스는 Animal 클래스를 상속받아 make_sound 메서드를 오버라이딩하여 각각의 동물들이 내는 소리를 반환합니다.

play_sound 함수는 Animal 타입의 객체를 매개변수로 받아 해당 객체의 make_sound 메서드를 호출합니다. 이렇게 하면 다양한 동물 객체를 전달하여 해당 동물의 소리를 출력할 수 있습니다. 이러한 다형성은 코드의 유연성을 높여주고 새로운 동물 클래스가 추가되더라도 기존 코드를 변경하지 않고 적용할 수 있습니다.
