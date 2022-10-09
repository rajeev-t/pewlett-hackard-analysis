# Pewlett-Hackard-Analysis
an activity to learn SQL and use it to create databases, and query the data stored on those databases

## ERD Text

    departments
    -
    dept_no varchar pk
    dept_name varchar

    dept_emp
    -
    emp_no varint pk fk -< employees.emp_no pk fk -< dept_manager.emp_no
    dept_no varint pk fk -< dept_manager.dept_no
    from_date date
    to_date date

    dept_manager
    -
    dept_no varint pk fk - departments.dept_no
    emp_no varint pk fk - employees.emp_no
    from_date date
    to_date date

    employees
    -
    emp_no varint pk
    birth_date date
    first_name varchar
    last_name varchar
    gender varchar
    hire_date date

    salaries
    -
    emp_no varint pk fk - employees.emp_no
    salary varint pk
    from_date date
    to_date date

    titles
    -
    emp_no varint pk fk >- employees.emp_no
    title varchar pk
    from_date date
    to_date date