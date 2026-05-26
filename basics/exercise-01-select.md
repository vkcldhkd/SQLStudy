# Exercise 1 — SELECT

## Goal

`SELECT` 문을 사용해 테이블에서 원하는 컬럼을 조회하는 연습입니다.

---

## 1. Find the title of each film

```sql
SELECT title
FROM movies;
```

### Learned

- 특정 컬럼만 조회할 때는 `SELECT 컬럼명`을 사용합니다.

---

## 2. Find the director of each film

```sql
SELECT director
FROM movies;
```

### Learned

- 하나의 컬럼만 선택해서 조회할 수 있습니다.

---

## 3. Find the title and director of each film

```sql
SELECT title, director
FROM movies;
```

### Learned

- 여러 컬럼을 조회할 때는 쉼표로 구분합니다.

---

## 4. Find the title and year of each film

```sql
SELECT title, year
FROM movies;
```

### Learned

- 필요한 컬럼만 선택하면 결과를 더 명확하게 확인할 수 있습니다.

---

## 5. Find all the information about each film

```sql
SELECT *
FROM movies;
```

### Learned

- `*`는 테이블의 모든 컬럼을 조회할 때 사용합니다.
