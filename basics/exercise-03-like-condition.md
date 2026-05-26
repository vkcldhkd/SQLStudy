# Exercise 3 — LIKE and Conditions

## Goal

`LIKE`, `=`, `!=`를 사용해 문자열 조건을 검색하는 연습입니다.

---

## 1. Find all the Toy Story movies

```sql
SELECT *
FROM movies
WHERE title LIKE '%Toy Story%';
```

### Learned

- `LIKE`는 문자열 패턴을 검색할 때 사용합니다.
- `%`는 앞뒤로 어떤 문자열이 와도 된다는 의미입니다.

---

## 2. Find all the movies directed by John Lasseter

```sql
SELECT *
FROM movies
WHERE director = 'John Lasseter';
```

### Learned

- 문자열 비교는 작은따옴표를 사용합니다.
- 특정 값과 정확히 일치하는 데이터를 찾을 때는 `=`를 사용합니다.

---

## 3. Find all the movies and director not directed by John Lasseter

```sql
SELECT title, director
FROM movies
WHERE director != 'John Lasseter';
```

### Learned

- `!=`는 같지 않다는 의미입니다.
- 문제에서 movie와 director를 요구하므로 `title`, `director`만 조회했습니다.

---

## 4. Find all the WALL-* movies

```sql
SELECT *
FROM movies
WHERE title LIKE 'WALL-%';
```

### Learned

- `'WALL-%'`는 `WALL-`로 시작하는 문자열을 찾습니다.
- `%WALL%`보다 조건이 더 정확합니다.
