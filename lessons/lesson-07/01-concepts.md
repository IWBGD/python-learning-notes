# Lesson 7 — 리스트

## 1. 핵심 문법

### 리스트란?

여러 데이터를 하나의 변수에 순서대로 저장하는 자료형이다.

```python
scores = [80, 90, 75]
names = ["민수", "지수", "승현"]
```

### 인덱싱과 슬라이싱

```python
scores = [80, 90, 75, 100]

print(scores[0])    # 80
print(scores[-1])   # 100
print(scores[1:3])  # [90, 75]
```

### 요소 추가와 변경

```python
fruits = ["사과", "바나나"]

fruits.append("포도")
fruits[0] = "딸기"
```

### 요소 삭제

```python
fruits = ["사과", "바나나", "포도"]

fruits.remove("바나나")
del fruits[0]
last = fruits.pop()
```

- `remove()`: 값으로 삭제
- `del`: 인덱스로 삭제
- `pop()`: 요소를 꺼내고 삭제

### 검색과 정렬

```python
numbers = [3, 1, 2, 3]

print(numbers.count(3))  # 2
print(numbers.index(1))  # 1

numbers.sort()
print(numbers)  # [1, 2, 3, 3]

numbers.reverse()
print(numbers)  # [3, 3, 2, 1]
```

### 리스트 복사

```python
a = [1, 2, 3]

b = a
c = a.copy()
```

- `b = a`: 같은 리스트를 참조한다.
- `c = a.copy()`: 새로운 리스트를 만든다.

단, `copy()`는 얕은 복사이므로
중첩된 내부 리스트까지 독립적으로 복사하지는 않는다.

## 2. 코드 구조와 실행 흐름

### 리스트 순회

```python
scores = [80, 45, 90]

for score in scores:
    print(score)
```

리스트의 요소를 하나씩 가져와 처리한다.

### 조건을 만족하는 값만 모으기

```python
scores = [80, 45, 90, 60]
passed = []

for score in scores:
    if score >= 70:
        passed.append(score)

print(passed)  # [80, 90]
```

실행 흐름:

1. 결과를 저장할 빈 리스트를 만든다.
2. 원본 리스트를 순회한다.
3. 조건을 검사한다.
4. 조건을 만족하는 값을 결과 리스트에 추가한다.

### 리스트 참조와 복사의 차이

```python
a = [1, 2, 3]
b = a

b.append(4)

print(a)  # [1, 2, 3, 4]
```

두 변수가 같은 리스트를 가리키므로
`b`를 통해 수정해도 `a`에서 변화가 보인다.

### 중첩 리스트

```python
students = [
    ["민수", 85],
    ["지수", 92]
]

print(students[0][0])  # 민수
print(students[1][1])  # 92
```

첫 번째 인덱스로 내부 리스트를 선택하고,
두 번째 인덱스로 그 안의 요소를 선택한다.

## 3. 기억할 핵심

- 리스트는 여러 값을 순서대로 저장한다.
- 리스트는 요소를 추가하거나 변경할 수 있다.
- `append()`는 요소 하나를 추가한다.
- `sort()`는 원본 리스트를 정렬하며 반환값은 `None`이다.
- 변수 대입과 리스트 복사는 다르다.
- 반복문과 조건문으로 원하는 요소를 추출할 수 있다.
- 중첩 리스트에서는 인덱스가 가리키는 구조를 확인한다.
