# Exercise 7 — OUTER JOIN

## Goal

`LEFT JOIN`을 사용해 기준 테이블의 데이터를 유지하면서 다른 테이블의 데이터를 연결하는 연습입니다.

---

## 1. Find the list of all buildings that have employees

    SELECT DISTINCT building
    FROM employees;

### Learned

- 직원이 배정된 건물만 확인하면 되므로 `employees` 테이블에서 `building` 컬럼을 조회합니다.
- 같은 건물에 여러 직원이 있을 수 있으므로 `DISTINCT`를 사용해 중복을 제거합니다.

---

## 2. Find the list of all buildings and their capacity

    SELECT building_name, capacity
    FROM buildings;

### Learned

- 건물명과 수용 인원은 `buildings` 테이블에 있으므로 JOIN 없이 조회할 수 있습니다.
- 필요한 컬럼만 선택하면 결과를 더 명확하게 확인할 수 있습니다.

---

## 3. List all buildings and the distinct employee roles in each building (including empty buildings)

    SELECT DISTINCT building_name, role
    FROM buildings
    LEFT JOIN employees
    ON buildings.building_name = employees.building;

### Learned

- 모든 건물을 포함해야 하므로 `buildings` 테이블을 기준으로 `LEFT JOIN`을 사용합니다.
- 직원이 없는 건물도 결과에 포함되며, 이 경우 `role` 값은 `NULL`로 표시됩니다.
- 같은 건물에 같은 역할의 직원이 여러 명 있을 수 있으므로 `DISTINCT`를 사용해 중복을 제거합니다.
