# Pewlett Hackard Employee Database Analysis

## Overview of the analysis:
- Pewlett Hackard (PH) is a large company with several thousand employees. A considerable number of the employees are ready to retire in the next few years. 

- The primary goal of this analysis is to identify who is going to retire for each department, and how many positions PH needs to fill based on department/title. 

- PH has been using spreed sheets to store and manage their data. The first step of this analysis is building an employee database using PostgreSQL.

## Data files:
1. departments.csv 
2. dept_emp.csv
3. dept_manager.csv
4. employees.csv
5. salaries.csv
6. titles.csv
	
## software / Tools:
- PostgreSQL 14.2
 - pgAdmin4 6.8
  - Terminal

## Results: 
- 41380 (about **14%** ) of PH's employees will be retiring in the coming few years

- There are a only around 1,500 employees who are eligible for the mentorship program.

- The results of this analysis will help PH how to proceed to fill will be vacant positions based on title and department.

- The upcoming retirements for each title is summrized in the teable bellow:
	
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>count</th>
      <th>title</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>25916</td>
      <td>Senior Engineer</td>
    </tr>
    <tr>
      <th>1</th>
      <td>24926</td>
      <td>Senior Staff</td>
    </tr>
    <tr>
      <th>2</th>
      <td>9285</td>
      <td>Engineer</td>
    </tr>
    <tr>
      <th>3</th>
      <td>7636</td>
      <td>Staff</td>
    </tr>
    <tr>
      <th>4</th>
      <td>3603</td>
      <td>Technique Leader</td>
    </tr>
    <tr>
      <th>5</th>
      <td>1090</td>
      <td>Assistant Engineer</td>
    </tr>
    <tr>
      <th>6</th>
      <td>2</td>
      <td>Manager</td>
    </tr>
  </tbody>
</table>

## Summary:
- From the result of the first two analyses, we found that there will be **more than 40,000** employees ready to retire in the near future, while there are just a little over **1,500** who are eligible for the mentorship program.

- The table bellow summarises the count for both retiring and mentors by department. 

## Retiring and Mentor  Counts

 <table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>dept_name</th>
      <th>retiring_count</th>
      <th>mentor_count</th>
      <th>rmc_ratio</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Marketing</td>
      <td>2782</td>
      <td>126</td>
      <td>22</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Finance</td>
      <td>2374</td>
      <td>74</td>
      <td>32</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Human Resources</td>
      <td>2446</td>
      <td>107</td>
      <td>22</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Production</td>
      <td>10224</td>
      <td>356</td>
      <td>28</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Development</td>
      <td>11627</td>
      <td>435</td>
      <td>26</td>
    </tr>
    <tr>
      <th>5</th>
      <td>Quality Management</td>
      <td>2816</td>
      <td>97</td>
      <td>29</td>
    </tr>
    <tr>
      <th>6</th>
      <td>Sales</td>
      <td>7301</td>
      <td>272</td>
      <td>26</td>
    </tr>
    <tr>
      <th>7</th>
      <td>Research</td>
      <td>2956</td>
      <td>113</td>
      <td>26</td>
    </tr>
    <tr>
      <th>8</th>
      <td>Customer Service</td>
      <td>3258</td>
      <td>128</td>
      <td>25</td>
    </tr>
  </tbody>
</table>

- The summary table clearly shows the huge gap between the number of expected retirements and the number of employees who qualify for the mentorship program.

- In every department, there are more than 20 employees ready to retire for evey qualifying mentor. The **rmc-ratio** column shows the approximate retiring-to-mentor ratio. In Finance department, for instance there will be more than 32 retirements for every mentor. 