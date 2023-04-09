<h1>Encapsulation</h1>

캡슐화는 객체 지향 프로그래밍의 핵심 원칙 중 하나로, 객체의 속성(데이터)과 행위(메서드)를 하나의 단위로 묶는 과정입니다. 이를 통해 객체의 내부 구현을 숨기고, 외부에서는 해당 객체와 상호작용하기 위한 인터페이스만 제공합니다. 파이썬에서는 클래스를 사용하여 캡슐화를 구현할 수 있습니다.

예를 들어, 은행 계좌를 클래스로 나타낼 수 있습니다.

```python

class BankAccount:
    def __init__(self, balance):
        self._balance = balance

    def deposit(self, amount):
        self._balance += amount

    def withdraw(self, amount):
        if self._balance >= amount:
            self._balance -= amount
        else:
            print("Insufficient funds")

    def get_balance(self):
        return self._balance

```

위의 코드에서 **`BankAccount`** 클래스는 **`_balance`** 속성(데이터)과 **`deposit`**, **`withdraw`**, **`get_balance`** 메서드(행위)를 캡슐화합니다. **`_balance`** 앞에 있는 언더스코어(_)는 속성이 private임을 나타내는 파이썬의 관례입니다. 이렇게 함으로써, 계좌의 잔액에 직접 접근하여 변경하는 대신, **`deposit`**과 **`withdraw`** 메서드를 사용하여 상호작용합니다.

```python

# 객체 생성
my_account = BankAccount(1000)

# 메서드를 사용하여 잔액 확인, 입금, 출금
print(my_account.get_balance())  # 1000
my_account.deposit(500)
print(my_account.get_balance())  # 1500
my_account.withdraw(200)
print(my_account.get_balance())  # 1300

```

이 예제에서, 캡슐화를 통해 **`_balance`** 속성에 대한 접근을 제한하고, 메서드를 통해 해당 속성을 안전하게 조작할 수 있습니다. 이를 통해 코드의 가독성과 유지 보수성이 향상됩니다.
