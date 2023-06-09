프로그래밍 언어 구현의 종류는 크게 컴파일러와 인터프리터 두 가지로 나뉩니다.

1. [컴파일러](https://github.com/weird14446/Study/blob/main/Computer%20Science/Programming%20Language%20Theory/Programming%20Language%20Implementation/Compiler.md) : 컴파일러는 소스 코드를 목적 코드로 변환하는 프로그램으로, 소스 코드 전체를 먼저 컴파일 한 후에 목적 코드를 생성합니다. 이후 생성된 목적 코드는 컴퓨터에서 직접 실행됩니다. 대표적인 컴파일러 언어로는 C, C++, Java, Go 등이 있습니다.

2. [인터프리터](https://github.com/weird14446/Study/blob/main/Computer%20Science/Programming%20Language%20Theory/Programming%20Language%20Implementation/Interpreter.md) : 인터프리터는 소스 코드를 한 줄씩 읽어서 즉시 실행하는 프로그램으로, 소스 코드를 먼저 컴파일하지 않고 바로 실행합니다. 따라서 소스 코드의 수정이 즉시 반영됩니다. 대표적인 인터프리터 언어로는 Python, Ruby, JavaScript, PHP 등이 있습니다.

또한, 최근에는 JIT 컴파일러라는 개념도 등장하였습니다. JIT 컴파일러는 인터프리터와 컴파일러의 장점을 결합한 것으로, 실행 시점에 인터프리터로 실행하다가 일정 조건이 충족되면 컴파일러를 사용하여 목적 코드를 생성하고 이후에는 컴파일된 코드를 실행합니다. 대표적인 JIT 컴파일러 언어로는 Java, C# 등이 있습니다.