1.```SELECT emp.first_name, emp.last_name, emp.department_id, dep.department_name
FROM employees emp JOIN departments dep
ON emp.department_id = dep.department_id;```

![image](https://user-images.githubusercontent.com/123379322/221872565-ebc94358-8c3e-4e4e-9f84-890db80ab5c4.png)

2.```SELECT emp.first_name, emp.last_name, dep.department_name, loc.city, loc.state_province FROM employees emp JOIN departments dep ON emp.department_id = dep.department_id JOIN locations loc ON dep.location_id = loc.location_id;```

![image](https://user-images.githubusercontent.com/123379322/221874552-3c477ae6-8a49-4a2d-939e-b2b3f61f289f.png)

3.```SELECT emp.first_name, emp.last_name, emp.salary, job.grade_level FROM employees emp JOIN job_grades job ON emp.salary BETWEEN job.lowest_sal AND job.highest_sal;```

![image](https://user-images.githubusercontent.com/123379322/221875691-49470a2a-5061-4a6d-933b-d01c6c837ae3.png)

4.```SELECT emp.first_name, emp.last_name, emp.department_id, dep.department_name FROM employees emp JOIN departments dep ON emp.department_id = dep.department_id AND emp.department_id IN (80, 40) ORDER BY emp.last_name;```

![image](https://user-images.githubusercontent.com/123379322/221878155-32e25e11-99b1-46dc-91d6-2c2994e2cff4.png)
