# Lesson 9 — 함수

## 1. 핵심 문법

### 함수란?

특정 작업을 수행하는 코드를 이름으로 묶은 것이다.

```python
def greet():
    print("안녕하세요!")

greet()
```

- `def`: 함수를 정의하는 키워드
- 함수 이름 뒤에 `()`를 작성한다.
- 함수 내부 코드는 들여쓰기한다.
- 정의한 함수는 호출해야 실행된다.

### 매개변수와 인자

```python
def greet(name):
    print(f"안녕하세요, {name}님!")

greet("승현")
```

- 매개변수(parameter): 함수 정의에서 값을 받을 이름
- 인자(argument): 호출할 때 전달하는 실제 값

### return

함수의 결과를 호출한 곳으로 반환한다.

```python
def add(a, b):
    return a + b

result = add(10, 20)

print(result)  # 30
```

`return`은 값을 반환하면서
현재 함수의 실행을 종료한다.

### print()와 return의 차이

```python
def show_number():
    print(10)

def get_number():
    return 10
```

- `print()`: 값을 화면에 출력한다.
- `return`: 값을 함수 호출 결과로 전달한다.

별도의 `return`이 없는 함수는
기본적으로 `None`을 반환한다.

### 조건문과 조기 반환

```python
def check_entry(level, hp):
    if hp <= 0:
        return "체력 부족"

    if level < 10:
        return "레벨 부족"

    return "입장 가능"
```

조건을 만족하면 즉시 반환하고
나머지 함수 코드는 실행하지 않는다.

### 지역변수와 전역변수

```python
number = 10

def test():
    number = 20
    print(number)

test()         # 20
print(number)  # 10
```

함수 안에서 만든 지역변수는
함수 바깥의 같은 이름 변수와 구분된다.

### 함수 재사용

```python
def double(number):
    return number * 2

def calculate(number):
    result = double(number)
    return result + 5

print(calculate(10))  # 25
```

하나의 함수에서 다른 함수를 호출할 수 있다.

## 2. 코드 구조와 실행 흐름

### 함수 정의와 호출

```python
def start_game():
    print("게임 시작!")

print("준비 중")
start_game()
print("게임 종료")
```

실행 흐름:

1. 함수 정의를 처리한다.
2. "준비 중"을 출력한다.
3. `start_game()`을 호출한다.
4. 함수 내부 코드를 실행한다.
5. 함수 실행이 끝나면 호출한 위치 다음으로 돌아온다.

### 함수의 데이터 흐름

```python
def multiply(a, b):
    result = a * b
    return result

answer = multiply(3, 4)
print(answer)
```

데이터 흐름:

1. 호출할 때 인자 3과 4를 전달한다.
2. 매개변수 `a`, `b`가 값을 받는다.
3. 함수 내부에서 계산한다.
4. `return`으로 결과를 반환한다.
5. 반환값을 `answer`에 저장한다.
6. 최종 결과를 출력한다.

### 함수 + 반복문 + 조건문

```python
def calculate_pass_total(scores):
    total = 0

    for score in scores:
        if score >= 70:
            total += score

    return total

scores = [85, 42, 77, 90]
print(calculate_pass_total(scores))
```

구조:

- 함수: 전체 작업을 묶는 큰 상자
- 반복문: 여러 값을 순서대로 처리
- 조건문: 필요한 값만 선택
- 누적 변수: 선택된 값의 합계를 저장
- return: 최종 결과를 함수 밖으로 전달

### return의 위치가 중요한 이유

```python
def total_numbers(numbers):
    total = 0

    for number in numbers:
        total += number

    return total
```

`return`이 반복문 밖에 있으므로
모든 숫자를 처리한 뒤 결과를 반환한다.

반대로 `return`을 반복문 안에 배치하면
첫 번째 반복에서 함수가 종료될 수 있다.

### 지역변수와 변경 가능한 데이터

```python
def add_item(items):
    items.append("포도")

fruits = ["사과"]
add_item(fruits)

print(fruits)  # ['사과', '포도']
```

리스트를 함수에 전달하면
함수 내부에서 같은 리스트 객체를 변경할 수 있다.

따라서 지역변수라는 이유만으로
원본 데이터가 항상 보호되는 것은 아니다.

## 3. 기억할 핵심

- 함수는 반복되는 작업을 재사용하기 위한 구조다.
- 함수는 정의와 호출을 구분해야 한다.
- 매개변수는 값을 받는 이름, 인자는 전달하는 값이다.
- `print()`와 `return`은 역할이 다르다.
- `return`은 현재 함수의 실행을 종료한다.
- `break`는 반복문을 종료하고 `return`은 함수를 종료한다.
- 함수 내부의 지역변수와 함수 밖의 전역변수는 구분된다.
- 변경 가능한 객체를 전달하면 원본이 수정될 수 있다.
- 함수의 입력, 처리, 반환 흐름을 이해하는 것이 중요하다.

## 4. 복습 문제와 풀이

> 추후 복습 문제를 풀면서 작성

## 5. 실수와 디버깅 기록

> 추후 작성
