# Exercise 2 — WHERE, BETWEEN, LIMIT

## Goal

`WHERE`, `BETWEEN`, `NOT BETWEEN`, `ORDER BY`, `LIMIT`을 사용해 조건에 맞는 데이터를 조회하는 연습입니다.

---

## 1. Find the movie with a row id of 6

```sql
SELECT *
FROM movies
WHERE id = 6;
```

### Learned

- `WHERE`는 조건에 맞는 행만 조회할 때 사용합니다.

---

## 2. Find the movies released in the years between 2000 and 2010

```sql
SELECT *
FROM movies
WHERE year BETWEEN 2000 AND 2010;
```

### Learned

- `BETWEEN A AND B`는 A 이상 B 이하의 범위를 의미합니다.

---

## 3. Find the movies not released in the years between 2000 and 2010

```sql
SELECT *
FROM movies
WHERE year NOT BETWEEN 2000 AND 2010;
```

### Learned

- `NOT BETWEEN`은 지정한 범위에 포함되지 않는 데이터를 조회할 때 사용합니다.

---

## 4. Find the first 5 Pixar movies and their release year

```sql
SELECT title, year
FROM movies
ORDER BY year ASC
LIMIT 5;
```

### Learned

- `ORDER BY year ASC`는 오래된 연도부터 정렬합니다.
- `LIMIT 5`는 결과를 5개로 제한합니다.
- 문제에서 요구한 컬럼만 조회하기 위해 `title`, `year`만 선택했습니다.
