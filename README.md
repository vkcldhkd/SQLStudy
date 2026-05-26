# SQLStudy

SQL 기본 문법을 학습하며 정리한 저장소입니다.  
SQLBolt 예제를 기준으로 `SELECT`, `WHERE`, `LIKE`, `ORDER BY`, `LIMIT`, `JOIN` 등을 단계별로 정리했습니다.

## Study Topics

| File | Topic |
|---|---|
| [Exercise 1](./basics/exercise-01-select.md) | SELECT 기본 조회 |
| [Exercise 2](./basics/exercise-02-where-between-limit.md) | WHERE, BETWEEN, LIMIT |
| [Exercise 3](./basics/exercise-03-like-condition.md) | LIKE, 문자열 조건 검색 |
| [Exercise 4](./basics/exercise-04-orderby-limit-offset.md) | DISTINCT, ORDER BY, LIMIT, OFFSET |
| [Review 1](./basics/review-01-north-american-cities.md) | 필터링, 정렬, 서브쿼리 |
| [Exercise 6](./basics/exercise-06-inner-join.md) | INNER JOIN |

## What I Learned

- `SELECT`를 사용해 필요한 컬럼만 조회하는 방법
- `WHERE`를 사용해 조건에 맞는 데이터만 필터링하는 방법
- `BETWEEN`, `NOT BETWEEN`을 사용한 범위 조건 처리
- `LIKE`와 `%` 와일드카드를 사용한 문자열 검색
- `ORDER BY`를 사용한 정렬
- `LIMIT`, `OFFSET`을 사용한 결과 개수 제한과 페이지 이동
- `DISTINCT`를 사용한 중복 제거
- `INNER JOIN`을 사용해 두 테이블의 데이터를 연결하는 방법
- 서브쿼리를 사용해 특정 행의 값을 기준으로 비교하는 방법

## Repository Structure

```text
SQLStudy/
├── README.md
└── basics/
    ├── exercise-01-select.md
    ├── exercise-02-where-between-limit.md
    ├── exercise-03-like-condition.md
    ├── exercise-04-orderby-limit-offset.md
    ├── review-01-north-american-cities.md
    └── exercise-06-inner-join.md
```
