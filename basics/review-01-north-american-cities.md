# Review 1 — North American Cities

## Goal

도시 데이터를 대상으로 조건 검색, 정렬, 제한, 서브쿼리를 복습합니다.

---

## 1. List all the Canadian cities and their populations

```sql
SELECT city, population
FROM north_american_cities
WHERE country = 'Canada';
```

### Learned

- 문제에서 요구한 `city`, `population` 컬럼만 조회했습니다.

---

## 2. Order all the cities in the United States by their latitude from north to south

```sql
SELECT *
FROM north_american_cities
WHERE country = 'United States'
ORDER BY latitude DESC;
```

### Learned

- 위도가 높을수록 북쪽에 위치합니다.
- 북쪽에서 남쪽 순서로 정렬하려면 `latitude DESC`를 사용합니다.

---

## 3. List all the cities west of Chicago, ordered from west to east

```sql
SELECT *
FROM north_american_cities
WHERE longitude < (
    SELECT longitude
    FROM north_american_cities
    WHERE city = 'Chicago'
)
ORDER BY longitude ASC;
```

### Learned

- Chicago의 longitude 값을 직접 입력하지 않고 서브쿼리로 가져왔습니다.
- 서쪽에 있는 도시는 Chicago보다 longitude 값이 더 작습니다.
- 서쪽에서 동쪽 순서로 보기 위해 `longitude ASC`를 사용했습니다.

---

## 4. List the two largest cities in Mexico by population

```sql
SELECT *
FROM north_american_cities
WHERE country = 'Mexico'
ORDER BY population DESC
LIMIT 2;
```

### Learned

- 인구가 많은 순서로 정렬하기 위해 `population DESC`를 사용했습니다.
- 상위 2개 도시만 보기 위해 `LIMIT 2`를 사용했습니다.

---

## 5. List the third and fourth largest cities by population in the United States and their population

```sql
SELECT city, population
FROM north_american_cities
WHERE country = 'United States'
ORDER BY population DESC
LIMIT 2 OFFSET 2;
```

### Learned

- 1위와 2위를 건너뛰기 위해 `OFFSET 2`를 사용했습니다.
- 3위와 4위만 조회하기 위해 `LIMIT 2`를 사용했습니다.
