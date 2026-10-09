# Lesson 3 — 형변환과 산술 연산

## 1. 핵심 문법

### 자료형 변환

```python
number = "100"

a = int(number)      # 문자열 → 정수
b = float(number)    # 문자열 → 실수
c = str(25)          # 정수 → 문자열
```

- `int()`: 정수로 변환
- `float()`: 실수로 변환
- `str()`: 문자열로 변환

변환할 수 없는 문자열에 `int()` 등을 사용하면
`ValueError`가 발생할 수 있다.

### input()과 형변환

```python
age = int(input("나이를 입력하세요: "))

print(age + 1)
```

`input()`은 문자열을 반환하므로,
숫자 계산이 필요하면 적절한 형변환을 해야 한다.

### 산술 연산자

```python
a = 17
b = 5

print(a + b)   # 22: 덧셈
print(a - b)   # 12: 뺄셈
print(a * b)   # 85: 곱셈
print(a / b)   # 3.4: 나눗셈
print(a // b)  # 3: 몫
print(a % b)   # 2: 나머지
print(a ** 2)  # 289: 거듭제곱
```

### 복합 대입 연산자

```python
total = 10

total += 5  # total = total + 5
total -= 2  # total = total - 2
total *= 3  # total = total * 3
```

## 2. 코드 구조와 실행 흐름

### 입력 → 변환 → 계산 → 출력

```python
a = int(input("첫 번째 숫자: "))
b = int(input("두 번째 숫자: "))

total = a + b

print(f"합계: {total}")
```

프로그램은 다음 순서로 실행된다.

1. 사용자의 입력을 받는다.
2. 문자열을 숫자로 변환한다.
3. 변환한 값으로 계산한다.
4. 결과를 출력한다.

### 연산 순서

```python
result = (10 + 5) * 2
print(result)  # 30
```

괄호 안의 연산이 먼저 수행된다.

### 몫과 나머지의 활용

```python
minutes = 125

hours = minutes // 60
remaining = minutes % 60

print(hours)      # 2
print(remaining)  # 5
```

몫과 나머지는 시간 계산이나
특정 주기마다 반복되는 값을 처리할 때 유용하다.

## 3. 기억할 핵심

- `input()`의 결과는 문자열이다.
- 숫자 계산 전에 자료형을 확인한다.
- `/`는 일반 나눗셈, `//`는 몫을 구하는 연산이다.
- `%`는 나머지를 구하는 연산이다.
- 연산자의 우선순위와 괄호 사용에 주의한다.
- `//`는 채팅에서 쓰는 설명 기호와 달리 Python의 실제 연산자다.

## 4. 복습 문제와 풀이

> 추후 복습 문제를 풀면서 작성

## 5. 실수와 디버깅 기록

> 추후 작성
