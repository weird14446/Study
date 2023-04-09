<h1>Inheritance</h1>

상속은 객체 지향 프로그래밍의 핵심 원칙 중 하나로, 기존 클래스의 속성과 메서드를 새로운 클래스에서 재사용할 수 있게 하는 기능입니다. 파이썬에서는 상속을 사용하여 코드를 간결하게 작성하고, 중복을 줄일 수 있습니다.

예를 들어, 동물의 기본 특성과 행동을 나타내는 클래스를 만들고, 이를 상속받아 특정 동물 종류를 나타내는 클래스를 만들 수 있습니다.

먼저, 기본 클래스인 **`Animal`** 을 작성합니다.

```python

class Animal:
    def __init__(self, name, species):
        self.name = name
        self.species = species

    def make_sound(self):
        print("Some generic animal sound")

    def __str__(self):
        return f"{self.name} is a {self.species}"

```

이제 **`Dog`** 와 **`Cat`** 클래스를 만들어 **`Animal`** 클래스를 상속받습니다.

```python

class Dog(Animal):
    def __init__(self, name):
        super().__init__(name, "Dog")

    def make_sound(self):
        print("Woof!")

class Cat(Animal):
    def __init__(self, name):
        super().__init__(name, "Cat")

    def make_sound(self):
        print("Meow!")

```

여기서 **`Dog`** 와 **`Cat`** 클래스는 **`Animal`** 클래스를 상속받아 **`name`** 과 **`species`** 속성, 그리고 **`make_sound`** 메서드를 재사용하고 있습니다. **`super().__init__(name, "Dog")`** 와 같은 구문은 기본 클래스의 생성자를 호출하는 데 사용됩니다.

이제 **`Dog`** 와 **`Cat`** 객체를 생성하고 메서드를 사용해 봅시다.

```python

dog = Dog("Buddy")
cat = Cat("Mittens")

print(dog)  # Buddy is a Dog
print(cat)  # Mittens is a Cat

dog.make_sound()  # Woof!
cat.make_sound()  # Meow!

```

상속을 사용하면 기본 클래스의 속성과 메서드를 쉽게 확장하거나 수정할 수 있어 코드의 재사용성을 높이고 유지 보수를 용이하게 합니다.
