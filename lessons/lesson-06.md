# Lesson 6 — 문자열 활용

## 1. 핵심 문법

### 인덱싱

문자열에서 특정 위치의 문자를 가져온다.

```python
text = "Python"

print(text[0])   # P
print(text[1])   # y
print(text[-1])  # n
```

인덱스는 0부터 시작한다.

### 슬라이싱

```python
text = "Python"

print(text[0:3])   # Pyt
print(text[2:])    # thon
print(text[:3])    # Pyt
print(text[::-1])  # nohtyP
```

`text[start:stop:step]` 형태로 사용한다.
`stop` 위치는 포함되지 않는다.

### 문자열 길이와 포함 여부

```python
text = "Python"

print(len(text))       # 6
print("Py" in text)    # True
print("Java" in text)  # False
```

### 주요 문자열 메서드

```python
text = "  Hello Python  "

print(text.strip())  # 양쪽 공백 제거
print(text.upper())  # 대문자 변환
print(text.lower())  # 소문자 변환
```

```python
text = "apple banana apple"

print(text.replace("apple", "orange"))
print(text.count("apple"))  # 2
print(text.find("banana"))  # 6
```

- `replace()`: 문자열 일부 교체
- `count()`: 특정 문자열의 등장 횟수
- `find()`: 처음 발견한 위치, 없으면 -1

### split()

```python
text = "사과,바나나,포도"

fruits = text.split(",")

print(fruits)
# ['사과', '바나나', '포도']
```

### 문자열 검사

```python
text = "Python123"

print(text.startswith("Py"))  # True
print(text.endswith("123"))   # True
print("123".isdigit())        # True
```

## 2. 코드 구조와 실행 흐름

### 문자열은 순서가 있는 데이터

문자열의 각 문자는 인덱스로 접근할 수 있다.

```python
text = "ABC"

for char in text:
    print(char)
```

반복문으로 문자열의 문자를
처음부터 끝까지 순서대로 처리할 수 있다.

### 입력값 검증 후 형변환

```python
value = input("숫자를 입력하세요: ")

if value.isdigit():
    number = int(value)
    print(number * 2)
else:
    print("숫자를 입력하세요.")
```

문자열을 숫자로 변환하기 전에
입력값이 적절한지 확인하는 구조다.

단, `isdigit()`은 음수 기호나 소수점까지
일반적인 숫자 형식으로 인정하는 검사는 아니다.

### 문자열은 변경 불가능한 자료형

```python
text = "hello"
text = text.upper()
```

`upper()`는 원래 문자열을 직접 수정하지 않고
변환된 새 문자열을 반환한다.

변경 결과를 계속 사용하려면
변수에 다시 저장할 수 있다.

## 3. 기억할 핵심

- 문자열 인덱스는 0부터 시작한다.
- 음수 인덱스로 뒤쪽 문자에 접근할 수 있다.
- 슬라이싱의 종료 인덱스는 포함되지 않는다.
- 문자열 메서드는 가공과 검증에 사용된다.
- 문자열은 변경 불가능한 자료형이다.
- 사용자 입력을 처리할 때 검증 순서가 중요하다.

## 4. 복습 문제와 풀이

> 추후 복습 문제를 풀면서 작성

## 5. 실수와 디버깅 기록

> 추후 작성
