# Lesson 3 — 형변환과 산술 연산

## 1. 핵심 문법

### 자료형 변환

```python
number = "100"

a = int(number)
b = float(number)
c = str(25)
```

- `int()`: 정수로 변환
- `float()`: 실수로 변환
- `str()`: 문자열로 변환

변환할 수 없는 문자열을 숫자로 변환하려 하면
`ValueError`가 발생할 수 있다.

### input()과 형변환

```python
age = int(input("나이를 입력하세요: "))

print(age + 1)
```

`input()`의 결과는 문자열이므로,
숫자 계산이 필요하면 형변환해야 한다.

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

total += 5
total -= 2
total *= 3
```

`total += 5`는 `total = total + 5`와 같은 의미다.

## 2. 코드 구조와 실행 흐름

### 입력 → 변환 → 계산 → 출력

```python
a = int(input("첫 번째 숫자: "))
b = int(input("두 번째 숫자: "))

total = a + b

print(f"합계: {total}")
```

실행 흐름:

1. 사용자의 입력을 받는다.
2. 문자열을 숫자로 변환한다.
3. 변환된 값으로 계산한다.
4. 결과를 출력한다.

### 연산 순서

```python
result = (10 + 5) * 2

print(result)  # 30
```

괄호 안의 연산이 먼저 수행된다.

### 몫과 나머지 활용

```python
minutes = 125

hours = minutes // 60
remaining = minutes % 60

print(hours)      # 2
print(remaining)  # 5
```

몫과 나머지는 시간 계산이나
반복되는 주기를 처리할 때 유용하다.

## 3. 기억할 핵심

- `input()`은 문자열을 반환한다.
- 숫자 계산 전에 자료형을 확인한다.
- `/`는 일반 나눗셈이다.
- `//`는 몫을 구한다.
- `%`는 나머지를 구한다.
- 연산 순서와 괄호 사용에 주의한다.
