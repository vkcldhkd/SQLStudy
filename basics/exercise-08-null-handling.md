# Exercise 8 — NULL Handling

## Goal

`NULL` 값을 조건으로 사용하고, `LEFT JOIN`과 `IS NULL`을 조합해 매칭되지 않는 데이터를 찾는 연습입니다.

---

## 1. Find the name and role of all employees who have not been assigned to a building

    SELECT name, role
    FROM employees
    WHERE building IS NULL;

### Learned

- `NULL`은 값이 없음을 의미합니다.
- `NULL`은 `=`로 비교하지 않고 `IS NULL`을 사용해야 합니다.
- 건물에 배정되지 않은 직원은 `building` 컬럼이 `NULL`인 직원입니다.

---

## 2. Find the names of the buildings that hold no employees

    SELECT building_name
    FROM buildings
    LEFT JOIN employees
    ON buildings.building_name = employees.building
    WHERE employees.building IS NULL;

### Learned

- 직원이 없는 건물도 확인해야 하므로 `buildings` 테이블을 기준으로 `LEFT JOIN`을 사용합니다.
- `employees` 테이블과 매칭되지 않은 건물은 JOIN 결과에서 `employees.building` 값이 `NULL`이 됩니다.
- `LEFT JOIN + IS NULL` 패턴은 한쪽 테이블에는 있지만 다른 테이블에는 없는 데이터를 찾을 때 자주 사용됩니다.
