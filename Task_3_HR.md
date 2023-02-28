1.```sql
SELECT emp.first_name, emp.last_name, emp.department_id, dep.department_name
FROM employees emp JOIN departments dep
ON emp.department_id = dep.department_id;
```
