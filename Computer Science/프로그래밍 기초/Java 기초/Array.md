# 배열

자바에서 배열은 동일한 타입의 여러 변수를 하나의 컬렉션으로 관리할 수 있게 해주는 데이터 구조입니다. 배열은 고정된 크기를 가지며, 배열에 속한 각각의 항목은 인덱스를 통해 접근할 수 있습니다.

배열을 선언하는 방법은 다음과 같습니다:

```java
type[] arrayName; // 예: int[] myArray;
```

배열을 생성하고 초기화하는 방법은 다음과 같습니다:

```java
int[] myArray = new int[5]; // 5개의 정수를 저장할 수 있는 배열 생성
```

위 코드는 길이가 5인 정수 배열을 생성합니다. 배열의 인덱스는 0부터 시작하므로, 이 배열의 각 요소는 **`myArray[0]`**, **`myArray[1]`**, **`myArray[2]`**, **`myArray[3]`**, **`myArray[4]`** 와 같이 접근할 수 있습니다.

배열을 선언과 동시에 초기화하는 방법도 있습니다:

```java
int[] myArray = {1, 2, 3, 4, 5}; // 초기화와 동시에 값을 할당
```

배열의 각 요소에는 다음과 같이 접근할 수 있습니다:

```java
int first = myArray[0]; // 첫 번째 요소
int second = myArray[1]; // 두 번째 요소
```

배열의 길이(요소의 개수)는 **`length`** 속성을 통해 알 수 있습니다:

```java
int length = myArray.length; // 배열의 길이
```

배열을 사용하면, 많은 수의 변수를 효과적으로 관리할 수 있습니다. 예를 들어, 100개의 정수를 저장하려면 100개의 정수 변수를 선언하지 않고, 단지 크기가 100인 배열 하나를 선언하면 됩니다. 이렇게 하면 코드가 간결해지고, 관리가 용이해집니다.

## 다차원 배열
다차원 배열은 이름에서도 알 수 있듯이 배열의 배열이라고 볼 수 있습니다. 다차원 배열은 행과 열을 가진 데이터, 예를 들면 행렬,를 표현하는 데 주로 사용됩니다.

자바에서 2차원 배열을 선언하고 초기화하는 방법은 다음과 같습니다:

```java
int[][] myArray = new int[3][3]; // 3x3 크기의 2차원 배열 생성
```

이는 3행 3열의 2차원 배열을 생성합니다. 이 배열의 각 요소에는 다음과 같이 접근할 수 있습니다:

```java
myArray[0][0] = 1; // 첫 번째 행의 첫 번째 열
myArray[0][1] = 2; // 첫 번째 행의 두 번째 열
myArray[1][0] = 3; // 두 번째 행의 첫 번째 열
```

배열을 선언과 동시에 초기화하는 방법도 있습니다:

```java
int[][] myArray = {
    {1, 2, 3},
    {4, 5, 6},
    {7, 8, 9}
}; // 3x3 크기의 2차원 배열을 생성하고 값을 할당
```

이와 같이 2차원 이상의 다차원 배열을 사용하면, 복잡한 데이터 구조를 표현할 수 있습니다. 예를 들어, 행렬 연산, 이미지 처리, 게임 보드 등을 구현할 때 다차원 배열이 유용하게 사용됩니다.

2차원 이상의 다차원 배열도 가능합니다. 예를 들어, 3차원 배열은 다음과 같이 선언할 수 있습니다:

```java
int[][][] my3DArray = new int[3][3][3]; // 3x3x3 크기의 3차원 배열 생성
```

그러나 다차원 배열은 이해하고 관리하기가 더 복잡하므로, 필요한 경우에만 사용하는 것이 좋습니다.

다음은 배열의 예제입니다.

1. 배열의 모든 요소를 순회하며 출력하기:

```java
for(int i = 0; i < numbers.length; i++) {
    System.out.println(numbers[i]);
}
```

1. 간단한 2차원 배열의 사용:

```java
int[][] matrix = {
    {1, 2, 3},
    {4, 5, 6},
    {7, 8, 9}
};

// 행렬의 모든 요소를 순회하며 출력
for(int i = 0; i < matrix.length; i++) {
    for(int j = 0; j < matrix[i].length; j++) {
        System.out.print(matrix[i][j] + " ");
    }
    System.out.println();
}
```

이와 같이 배열은 반복문과 함께 사용되면 특히 효율적입니다. 배열의 모든 요소를 순회하거나, 특정 조건을 만족하는 요소를 찾거나, 요소의 값을 변경하는 등의 작업을 쉽게 수행할 수 있습니다.