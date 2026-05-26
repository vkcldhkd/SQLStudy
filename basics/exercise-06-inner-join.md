# Exercise 6 — INNER JOIN

## Goal

`INNER JOIN`을 사용해 `movies` 테이블과 `boxoffice` 테이블을 연결하는 연습입니다.

---

## 1. Find the domestic and international sales for each movie

```sql
SELECT movies.id, title, domestic_sales, international_sales
FROM movies
INNER JOIN boxoffice
ON movies.id = boxoffice.movie_id;
```

### Learned

- `INNER JOIN`은 두 테이블에서 서로 연결되는 데이터만 조회합니다.
- `movies.id`와 `boxoffice.movie_id`를 기준으로 테이블을 연결했습니다.

---

## 2. Show the sales numbers for each movie that did better internationally rather than domestically

```sql
SELECT movies.id, title, domestic_sales, international_sales
FROM movies
INNER JOIN boxoffice
ON movies.id = boxoffice.movie_id
WHERE international_sales > domestic_sales;
```

### Learned

- 해외 매출이 국내 매출보다 큰 영화를 찾기 위해 `international_sales > domestic_sales` 조건을 사용했습니다.

---

## 3. List all the movies by their ratings in descending order

```sql
SELECT *
FROM movies
INNER JOIN boxoffice
ON movies.id = boxoffice.movie_id
ORDER BY boxoffice.rating DESC;
```

### Learned

- 평점이 높은 순서로 정렬하기 위해 `rating DESC`를 사용했습니다.
- JOIN 후에도 연결된 테이블의 컬럼을 기준으로 정렬할 수 있습니다.
