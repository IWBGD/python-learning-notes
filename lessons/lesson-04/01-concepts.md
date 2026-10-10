# Lesson 4 — 조건문과 논리 연산

## 1. 핵심 문법

### if / elif / else

조건에 따라 실행할 코드를 선택한다.

```python
score = 85

if score >= 90:
    print("A등급")
elif score >= 80:
    print("B등급")
else:
    print("C등급")
```

- `if`: 첫 번째 조건 검사
- `elif`: 앞선 조건이 거짓일 때 추가 검사
- `else`: 앞의 조건이 모두 거짓일 때 실행

### 비교 연산자

```python
a = 10
b = 5

print(a > b)   # True
print(a < b)   # False
print(a >= b)  # True
print(a <= b)  # False
print(a == b)  # False
print(a != b)  # True
```

비교 연산의 결과는 `True` 또는 `False`다.

### 논리 연산자

```python
age = 20
has_ticket = True

if age >= 18 and has_ticket:
    print("입장 가능")
```

- `and`: 양쪽 조건이 모두 참이어야 참
- `or`: 하나 이상 참이면 참
- `not`: 참과 거짓을 반대로 바꿈

### 중첩 조건문

```python
level = 15
hp = 80

if level >= 10:
    if hp > 0:
        print("던전 입장 가능")
    else:
        print("체력 부족")
else:
    print("레벨 부족")
```

## 2. 코드 구조와 실행 흐름

### 큰 상자 → 작은 상자

들여쓰기는 코드가 어떤 조건에 속하는지 나타낸다.

```python
if level >= 10:
    print("레벨 통과")

    if hp > 0:
        print("체력 통과")
```

안쪽 `if`는 바깥 조건이 참일 때만 검사된다.

### if와 elif의 차이

```python
score = 95

if score >= 90:
    print("90점 이상")

if score >= 80:
    print("80점 이상")
```

위 코드는 두 조건을 각각 검사하므로
두 문장이 모두 출력된다.

반면 `if / elif` 구조에서는
앞의 조건이 참이면 뒤의 `elif`를 검사하지 않는다.

### 조건의 순서

```python
score = 95

if score >= 80:
    print("B 이상")
elif score >= 90:
    print("A")
```

이 구조에서는 95점도 첫 조건에서 처리된다.

따라서 조건이 겹친다면
검사 순서가 중요하다.

### 논리 연산 우선순위

일반적으로 `not` → `and` → `or` 순서다.

복잡한 조건에서는 괄호를 사용해
의도를 명확히 표현한다.

## 3. 기억할 핵심

- 조건식은 참 또는 거짓으로 평가된다.
- `if / elif / else`는 실행 경로를 선택한다.
- 독립적인 `if`는 각각 조건을 검사한다.
- 들여쓰기는 코드의 소속을 결정한다.
- 중첩 조건문은 바깥 조건부터 검사한다.
- 조건의 순서가 결과에 영향을 줄 수 있다.
