# Lesson 8 — 딕셔너리

## 1. 핵심 문법

### 딕셔너리란?

키(key)와 값(value)을 연결하여 저장하는 자료형이다.

```python
player = {
    "name": "승현",
    "level": 15,
    "hp": 80
}
```

### 값 접근

```python
print(player["name"])
print(player["level"])
```

리스트는 인덱스로 접근하지만,
딕셔너리는 키를 이용해 값에 접근한다.

### 값 변경과 추가

```python
player["hp"] = 100
player["job"] = "전사"
```

기존 키에 대입하면 값을 변경하고,
새로운 키에 대입하면 항목을 추가한다.

### 값 삭제

```python
del player["job"]
```

### get() 메서드

```python
player = {"name": "승현", "level": 15}

print(player.get("name"))     # 승현
print(player.get("hp"))       # None
print(player.get("hp", 100))  # 100
```

`get()`은 키가 없을 때 오류 대신
기본값을 반환할 수 있다.

기본값을 반환한다고 해서
딕셔너리에 해당 키가 추가되지는 않는다.

### keys(), values(), items()

```python
player = {"name": "승현", "level": 15}

for key in player.keys():
    print(key)

for value in player.values():
    print(value)

for key, value in player.items():
    print(key, value)
```

## 2. 코드 구조와 실행 흐름

### 리스트와 딕셔너리의 차이

리스트는 데이터의 순서가 중요할 때 유용하다.

```python
scores = [80, 90, 70]
```

딕셔너리는 데이터의 의미를
이름으로 구분할 때 유용하다.

```python
student = {
    "name": "민수",
    "score": 80
}
```

### 딕셔너리와 조건문

```python
player = {"level": 15, "hp": 80}

if player["level"] >= 10 and player["hp"] > 0:
    print("입장 가능")
```

딕셔너리에서 값을 꺼내
조건식에 사용할 수 있다.

### 리스트 안의 딕셔너리

```python
players = [
    {"name": "민수", "level": 12},
    {"name": "지수", "level": 8},
    {"name": "승현", "level": 15}
]

for player in players:
    if player["level"] >= 10:
        print(player["name"])
```

실행 흐름:

1. 리스트에서 딕셔너리 하나를 가져온다.
2. 딕셔너리의 특정 키에 접근한다.
3. 값을 조건식에 사용한다.
4. 조건을 만족하면 필요한 데이터를 처리한다.

### 중첩 딕셔너리

```python
game = {
    "player": {
        "name": "승현",
        "hp": 80
    }
}

print(game["player"]["hp"])  # 80
```

큰 딕셔너리 안에서 작은 딕셔너리로 이동한 뒤
필요한 값에 접근한다.

## 3. 기억할 핵심

- 딕셔너리는 키와 값의 쌍으로 구성된다.
- 키를 이용해 의미 있는 데이터에 접근한다.
- 없는 키에 `[]`로 접근하면 `KeyError`가 발생한다.
- `get()`은 없는 키를 안전하게 조회할 때 유용하다.
- `get()`은 딕셔너리를 변경하지 않는다.
- `.items()`는 키와 값을 함께 순회할 때 유용하다.
- 리스트와 딕셔너리를 결합하면 여러 개체를 구조적으로 표현할 수 있다.

## 4. 복습 문제와 풀이

> 추후 복습 문제를 풀면서 작성

## 5. 실수와 디버깅 기록

> 추후 작성
