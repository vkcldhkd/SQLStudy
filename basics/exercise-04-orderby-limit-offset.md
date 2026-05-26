# Exercise 4 — DISTINCT, ORDER BY, LIMIT, OFFSET

## Goal

중복 제거, 정렬, 조회 개수 제한, 조회 시작 위치 이동을 연습합니다.

---

## 1. List all directors of Pixar movies alphabetically, without duplicates

```sql
SELECT DISTINCT director
FROM movies
ORDER BY director ASC;
```

### Learned

- `DISTINCT`는 중복된 값을 제거합니다.
- `ORDER BY director ASC`는 감독 이름을 오름차순으로 정렬합니다.

---

## 2. List the last four Pixar movies released, ordered from most recent to least

```sql
SELECT *
FROM movies
ORDER BY year DESC
LIMIT 4;
```

### Learned

- `DESC`는 내림차순 정렬입니다.
- 최신 영화부터 보기 위해 `year DESC`를 사용했습니다.

---

## 3. List the first five Pixar movies sorted alphabetically

```sql
SELECT *
FROM movies
ORDER BY title ASC
LIMIT 5;
```

### Learned

- `ORDER BY title ASC`는 제목 기준 알파벳 오름차순 정렬입니다.
- `LIMIT 5`로 처음 5개만 조회합니다.

---

## 4. List the next five Pixar movies sorted alphabetically

```sql
SELECT *
FROM movies
ORDER BY title ASC
LIMIT 5 OFFSET 5;
```

### Learned

- `OFFSET 5`는 앞의 5개 결과를 건너뜁니다.
- `LIMIT`과 `OFFSET`은 페이지네이션에 자주 사용됩니다.
