# Ex. No: 4 Creating Procedures using PL/SQL
## DATE: 24.08.23
### AIM: To create a procedure using PL/SQL.

### Steps:
1. Create employee table with following attributes (empid NUMBER, empname VARCHAR(10), dept VARCHAR(10),salary NUMBER);
2. Create a procedure named as insert_employee data.
3. Inside the procdure block, write the query for inserting the values into the employee table.
4. End the procedure.
5. Call the insert_employee data procedure to insert the values into the employee table.
6. Display the employee table

### Program:
```SQL> CREATE TABLE emp(empid NUMBER,empname VARCHAR(10),dept VARCHAR(10),salary NUMBER);```

```
SQL> CREATE OR REPLACE PROCEDURE emp_data AS
  2      BEGIN
  3      INSERT INTO emp(empid,empname,dept,salary)
  4      values(1,'KIRA','CSE',15000);
  5      INSERT INTO emp(empid,empname,dept,salary)
  6      values(2,'GORINO','IT',5500);
  7      INSERT INTO emp(empid,empname,dept,salary)
  8      values(3,'THORFIN','ECE',22000);
  9      COMMIT;
 10     FOR emp_rec IN (SELECT * FROM emp)LOOP
 11     DBMS_OUTPUT.PUT_LINE('EMPLOYEE ID:'||emp_rec.empid||',EMPLOYEE NAME:'|| emp_rec.empname||
 12     ',DEPARTMENT:'||emp_rec.dept||',SALARY:'||emp_rec.salary);
 13     END LOOP;
 14     END;
 15    /
```
### Output:
![1](https://github.com/ASHWINKUMAR2903/Ex-No-4-Creating-Procedures-using-PL-SQL/assets/119407186/1072146f-6b5f-4da1-baf4-115f28032676)   
![2](https://github.com/ASHWINKUMAR2903/Ex-No-4-Creating-Procedures-using-PL-SQL/assets/119407186/e084c6df-e6cc-4ec5-a83d-31f27fc91c13)   
![3](https://github.com/ASHWINKUMAR2903/Ex-No-4-Creating-Procedures-using-PL-SQL/assets/119407186/27d6692c-91a3-4321-8c24-41806cd3305e)  
### Result:
the commands using Procedures using PL/SQL has been executed successfully.
