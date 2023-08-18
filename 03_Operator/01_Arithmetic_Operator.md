# 산술 연산자

## 연산자
- 자바에서는 여러 종류의 연산을 수행하기 위한 다양한 연산자를 제공합니다
- 대표적인 연산자는 다음과 같습니다
- 1. 산술 연산자
- 2. 대입 연산자
- 3. 증감 연산자
- 4. 비교 연산자
- 5. 논리 연산자
- 6. 비트 연산자
- 7. 삼항 연산자
- 8. instanceof 연산자

<br>

---

<br>

## 산술 연산자
- 사칙 연산을 다루는 연산자입니다
- 두 개의 피연산자를 가지는 이항 연산자이며, 피연산자들의 **결합 방향은 왼쪽에서 오른쪽**입니다.
- 항이란 해당 연산의 실행이 가능하기 위해 필요한 값이나 변수를 의미합니다
- 따라서 이항 연산자란 해당 연산의 실행을 위해서 두 개의 값이나 변수가 필요한 연산자를 의미합니다

<br>

|산술 연산자|설명|
|-----------|----|
|\+|왼쪽의 피연산자에 오른쪽의 피연산자를 더함|
|\-|왼쪽의 피연산자에서 오른쪽의 피연산자를 뺌|
|\*|왼쪽의 피연산자에 오른쪽의 피연산자를 곱함|
|\/|왼쪽의 피연산자를 오른쪽의 피연산자로 나눔|
|\%|왼쪽의 피연산자를 오른쪽의 피연산자로 나눈 후, 그 나머지를 반환함|

<br>

```java
int	num1 = 8, num2 = 4;

System.out.println("+ 연산자에 의한 결과:" + (num1 + num2)); //12
System.out.println("- 연산자에 의한 결과:" + (num1 - num2)); //4
System.out.println("* 연산자에 의한 결과:" + (num1 * num2)); //32
System.out.println("/ 연산자에 의한 결과:" + (num1 / num2)); //2
System.out.println("% 연산자에 의한 결과:" + (num1 % num2)); //0
```

<br>

---

<br>

## 연산자의 우선순위와 결합 방향
- 연산자 우선순위
	- 수식 내에 여러 연산자가 함께 등장할 때 어느 연산자가 먼저 처리될 것인가를 결정합니다
	- 다음 그림은 가장 높은 우선순위를 가지고 있는 괄호 연산자를 사용하여 연산자의 처리 순서를 변경하는 것을 보여줍니다

<br>

![image](https://github.com/Milky0929/TIL_Java/assets/138620137/abf8c008-dba2-43d7-b705-c3d71e2f3934)

<br>

- 연산자의 결합방향
	- 수식 내에 우선순위가 같은 연산자가 둘 이상 있을 때, 먼저 어느 연산을 수행할 것인가를 결정합니다

<br>

![image](https://github.com/Milky0929/TIL_Java/assets/138620137/dd01e7f6-165f-48be-99eb-be7b2cff0c84) 

<br>

---

<br>

## 자바 연산자의 우선순위표

- 연산자의 우선순위와 결합 방향은 다음과 같습니다
- 아래의 표에 나온 순서대로 우선순위가 빠른 연산자가 가장 먼저 실행됩니다
- 같은 우선 순위를 가진 연산자가 둘 이상 있을 때에는 결합 순서에 따라 실행 순서가 결정됩니다

<br>

|우선순위|연산자|설명|결합 방향|
|--------|------|----|---------|
|1|\[\]|첨자 연산자|왼쪽에서 오른쪽으로|
| |\.|멤버 연산자|왼쪽에서 오른쪽으로|
|2|\+\+|후위 증가 연산자|왼쪽에서 오른쪽으로|
| |\-\-|후위 감소 연산자|왼쪽에서 오른쪽으로|
|3|\!|논리 NOT 연산자|오른쪽에서 왼쪽으로|
| |~|비트 NOT 연산자|오른쪽에서 왼쪽으로|
| |\+|양의 부호 (단항 연산자)|오른쪽에서 왼쪽으로|
| |\-|음의 부호 (단항 연산자)|오른쪽에서 왼쪽으로|
| |\+\+|전위 증가 연산자|오른쪽에서 왼쪽으로|
| |\-\-|전위 감소 연산자|오른쪽에서 왼쪽으로|
| |(타입)|타입 캐스트 연산자|오른쪽에서 왼쪽으로|
|4|\*|곱셈 연산자|왼쪽에서 오른쪽으로|
| |/|나눗셈 연산자|왼쪽에서 오른쪽으로|
| |%|나머지 연산자|왼쪽에서 오른쪽으로|
|5|\+|덧셈 연산자 (이항 연산자)|왼쪽에서 오른쪽으로|
| |\-|뺄셈 연산자 (이항 연산자)|왼쪽에서 오른쪽으로|
|6|\<\<|비트 왼쪽 시프트 연산자|왼쪽에서 오른쪽으로|
| |\>\>|부호 비트를 확장하면서 비트 오른쪽 시프트|왼쪽에서 오른쪽으로|
| |\>\>\>|부호 비트까지 모두 비트 오른쪽 시프트|왼쪽에서 오른쪽으로|
|7|\<|관계 연산자(보다 작은)|왼쪽에서 오른쪽으로|
| |\<=|관계 연산자(보다 작거나 같은)|왼쪽에서 오른쪽으로|
| |\>|관계 연산자(보다 큰)|왼쪽에서 오른쪽으로|
| |\>=|관계 연산자(보다 크거나 같은)|왼쪽에서 오른쪽으로|
| |instanceof|인스턴스의 실제 타입 반환|왼쪽에서 오른쪽으로|
|8|==|관계 연산자(와 같은)|왼쪽에서 오른쪽으로|
| |\!=|관계 연산자(와 같지 않은)|왼쪽에서 오른쪽으로|
|9|&|비트 AND 연산자|왼쪽에서 오른쪽으로|
|10|^|비트 XOR 연산자|왼쪽에서 오른쪽으로|
|11|\||비트 OR 연산자|왼쪽에서 오른쪽으로|
|12|&&|논리 AND 연산자|왼쪽에서 오른쪽으로|
|13|\|\||논리 OR 연산자|왼쪽에서 오른쪽으로|
|14|? :|삼항 조건 연산자|오른쪽에서 왼쪽으로|
|15|=|대입 연산자 및 복합 대입 연산자|오른쪽에서 왼쪽으로|
