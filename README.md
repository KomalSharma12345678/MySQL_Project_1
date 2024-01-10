\\Write a SQL query to get the details of all employees.\\
SELECT * FROM EMPLOYEES;
\\Write a SQL query to display the specific information of all employees\\.
SELECT * FIRST_NAME,LAST_NAME,SALARY FROM EMPLOYEES;
\\Write a SQL query to get the total number of all employees working                
 in company.\\
          SELECT COUNT(*)  FROM EMPLOYEES;
\\Write a SQL query command to display the employee name, and Annual    Salary of all Employees.\\
         SELECT FIRST_NAME,LAST_NAME, 12*(SALARY) AS ‘ANNUALSALARY’;
 \\Write a SQL query to get the total salary being paid to all Employees\\.
            SELECT SUM(SALARY) FROM EMPLOYEES;
\\Write a SQL query to get the Maximum and Minimum Salary from the table.\\
           SELECT Max(SALARY), MIN(SALARY) FROM EMPLOYEES;
\\Write a query to display the detail of Employees in order to earning from lowest Salary to Highest Salary\\
          SELECT  EMP_ID, FIRST_NAME, LAST_NAME, SALARY FROM EMPLOYEES
          ORDER BY SALARY ASC;
\\Write a query to display the detail of Employees in order to earning from Highest Salary to Lowest Salary.\\
          SELECT EMP_ID, FIRST_NAME, LAST_NAME, SALARY FROM EMPLOYEES
          ORDER BY SALARY DESC;
\\Write a query to display the detail of Employees in order to their Hire Date\\
       SELECT * FROM EMPLOYEES
      ORDER BY HIRE_DATE ASC;
\\Write a Oracle SQL query to display the name of the employees in order to alphabetically ascending order\\.
     SELECT FIRST_NAME, LAST_NAME FROM EMPLOYEES 
     ORDER BY FIRST_NAME;
\\Write a SQL query to display EMP_ID, FIRST_NAME,MANAGER_ID, SALARY of the employees. The output first based on name in ascending order.\\
SELECT EMP_ID, FIRST-NAME,MANAGER-ID,SALARY FROM EMPLOYEES
ORDER BY FIRST_NAME ASC,MANAGER_ID ASC,SALARY ASC;
\\Write a Oracle SQL query to display the name of the employees in order to alphabetically ascending order.\\
SELECT * FROM EMPLOYEESS
ORDER BY FIRST_NAME;
\\Write a Oracle SQL query to display the name and their annual salary. The result should contain those employees first who earning the highest salary.\\
SELECT FIRST_NAME, SALARY*12 FROM EMPLOYEES
 ORDER BY SALARY DESC; 
\\Write a Oracle SQL query to display Manager_id and total number of employees working under each Manager.\\
SELECT MANAGER_ID, COUNT (MANAGER_ID) FROM EMPLOYEES
 GROUP BY MANAGER_ID;
\\Write a SQL query to display the name of Employees whose name is starting with alphabet ‘A”.\\
SELECT * FROM EMPLOYEES
WHERE FIRST_NAME LIKE ‘A%’;
\\Write a SQL query to display in ascending order that how many employees works under all managers.\\
SELECT COUNT(MANAGER_ID),MANAGER_ID FROM EMPLOYEES
GROUP BY MANAGER_ID
ORDER BY COUNT(MANAGER_ID) ASC;
\\Write a SQL to find the name of those Employees who gets highest Salary under manager whose Manager_Id is ‘121’.\\
SELECT FIRST_NAME,LAST_NAME,SALARY FROM EMPLOYEES
WHERE MANAGER_ID=’121’
ORDER BY SALARY DESC;
\\Write a SQl query to display the sum of salary in descending order of employees with manage_id=’123’.\\
SELECT  SUM(SALARY),MANAGER_ID FROM EMPLOYEES
GROUP BY MANAGER_ID
ORDER BY COUNT(MANAGER_ID DESC;
\\Write a SQL query to display the name of Employees with lowest to highest  Salary only with Manager_Id =’0’\\
SELECT FIRST_NAME,LAST_NAME,SALARY FROM EMPLOYEES
WHERE MANAGER_ID =’0’
ORDER BY SALARY ASC;
\\Write a SQL query to display the Phone number of each Employee.\\
SELECT  FIRST_NAME,LAST_NAME,PHONE_NO FROM EMPLOYEES;
\\Write a SQLquery to fetch all the Employyes who are also managers from the EMPLOYEES table.
SELECT FIRST_NAME,LAST_NAME FROM EMPLOYEES
WHERE EMP_ID IN (SELECT DISTINCT MANAGER_ID FROM EMPLOYESS);
\\Write a Oracle SQL query to display the Designation and total salary allotted for each designation from the company\\
SELECT DESIGNATION, SUM(SALARY) FROM EMPLOYEES
 GROUP BY DESIGNATION;
\\Write a Oracle SQL query to display the Manager_Id and maximum salary for each Manager.\\
SELECT MANAGER_ID, MAX(SALARY) FROM EMPLOYEES 
GROUP BY MANAGER_ID;
\\Write a query to fetch a list of Employees who are hired in or before 2007.\\
SELECT * FROM EMPLOYEE
  WHERE HIRE_DATE<='31-DEC-2007';
\\Write a query to list the employees name and total salary of a year and yearly salary is more than Rs.10000.\\
SELECT FIRST_NAME, LAST_NAME, SALARY*12 "YEARLY SALARY" FROM EMPLOYEES
WHERE (SALARY*12) >10000;


