# Lesson 5 — 반복문

## 1. 핵심 문법

### for 반복문

정해진 범위나 데이터의 각 요소를 순서대로 처리한다.

```python
for i in range(5):
    print(i)
```

출력: 0, 1, 2, 3, 4

### range()

```python
range(5)         # 0부터 4까지
range(1, 6)      # 1부터 5까지
range(1, 10, 2)  # 1, 3, 5, 7, 9
```

형식:

`range(start, stop, step)`

- `start`: 시작값
- `stop`: 종료 경계값 (포함되지 않음)
- `step`: 증가하거나 감소하는 간격

### while 반복문

조건이 참인 동안 반복한다.

```python
count = 1

while count <= 5:
    print(count)
    count += 1
```

### break

가장 가까운 반복문을 즉시 종료한다.

```python
for i in range(1, 11):
    if i == 5:
        break

    print(i)
```

### continue

현재 반복의 남은 부분을 건너뛰고
다음 반복으로 진행한다.

```python
for i in range(1, 6):
    if i == 3:
        continue

    print(i)
```

### 누적합

```python
total = 0

for i in range(1, 6):
    total += i

print(total)  # 15
```

## 2. 코드 구조와 실행 흐름

### 반복문 안과 밖

```python
total = 0

for i in range(1, 4):
    total += i
    print(f"현재 합계: {total}")

print(f"최종 합계: {total}")
```

반복문 안의 출력은 매 반복마다 실행된다.
반복문 밖의 출력은 반복이 끝난 후 한 번 실행된다.

### 반복문 + 조건문

```python
total = 0

for i in range(1, 11):
    if i % 2 == 0:
        total += i

print(total)
```

실행 흐름:

1. 반복할 값을 하나 가져온다.
2. 조건을 검사한다.
3. 조건을 만족하면 누적한다.
4. 다음 값으로 이동한다.
5. 반복이 끝나면 결과를 출력한다.

### while의 종료 조건

```python
count = 5

while count > 0:
    print(count)
    count -= 1
```

반복 중 조건에 영향을 주는 값이 바뀌지 않으면
무한 반복이 발생할 수 있다.

### break와 continue의 차이

- `break`: 반복문 자체를 종료
- `continue`: 현재 반복만 건너뜀

`while`에서 `continue`를 사용할 때는
조건을 바꾸는 코드가 건너뛰어지지 않도록 주의한다.

## 3. 기억할 핵심

- `for`는 정해진 데이터나 범위를 순회할 때 유용하다.
- `while`은 조건이 참인 동안 반복한다.
- `range()`의 종료값은 포함되지 않는다.
- 누적 변수는 보통 반복문 시작 전에 초기화한다.
- 들여쓰기에 따라 반복 실행되는 코드가 달라진다.
- `break`와 `continue`는 역할이 다르다.
