<h1>Singleton Pattern</h1>
싱글톤 패턴(Singleton Pattern)은 객체 지향 프로그래밍에서 특정 클래스의 인스턴스가 오직 하나만 존재하도록 보장하는 디자인 패턴입니다. 이 패턴은 전역 변수를 사용하지 않고 전역적으로 접근 가능한 유일한 인스턴스를 제공하며, 이 인스턴스는 필요할 때마다 반복해서 사용할 수 있습니다. 싱글톤 패턴은 로깅, 데이터베이스 연결, 설정 관리 등의 상황에서 사용됩니다.

Python에서 싱글톤 패턴을 구현하는 방법은 여러 가지가 있습니다. 여기서는 메타클래스를 사용하는 방법을 소개하겠습니다.

```python
class Singleton(type):
    _instances = {}

    def __call__(cls, *args, **kwargs):
        if cls not in cls._instances:
            cls._instances[cls] = super(Singleton, cls).__call__(*args, **kwargs)
        return cls._instances[cls]

class MyClass(metaclass=Singleton):
    def __init__(self):
        self.value = 42

# 사용 예제
instance1 = MyClass()
instance2 = MyClass()

print(instance1 is instance2)  # True를 출력합니다. 두 인스턴스가 동일한 것을 확인할 수 있습니다.
print(instance1.value)  # 42를 출력합니다.
print(instance2.value)  # 42를 출력합니다.

```

위 예제에서 **`Singleton`** 메타클래스는 인스턴스화가 시도될 때 호출되는 **`__call__`** 메소드를 오버라이드하여 싱글톤 패턴을 구현합니다. **`_instances`** 딕셔너리를 사용하여 클래스별로 인스턴스를 저장하고, 필요할 때마다 동일한 인스턴스를 반환합니다. **`MyClass`**는 **`Singleton`** 메타클래스를 사용하여 싱글톤 패턴을 적용합니다.

이 방식을 사용하면, **`MyClass`**의 인스턴스를 여러 번 생성하려고 해도 항상 동일한 인스턴스가 반환되어 싱글톤 패턴이 유지됩니다.
