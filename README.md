# Sql5

## 1 Problem 1 : Report Contiguos Dates		(https://leetcode.com/problems/report-contiguous-dates/ )
<br>

### 

## 2 Problem 2 : Student Report By Geography		(https://leetcode.com/problems/students-report-by-geography/ )

## 3 Problem 3 : Average Salary Department vs Company		(https://leetcode.com/problems/average-salary-departments-vs-company/solution/ )
<br>

### Solution 1 Using Case When Statements


## 4 Problem 4 : Game Play Analysis I		(https://leetcode.com/problems/game-play-analysis-i/ )
<br>

### Solution 1 Using Group BY and Min
SELECT DISTINCT player_id, MIN(event_date) AS first_login
FROM Activity
GROUP BY player_id
<br>
### Solution 2 Using First Value Function
SELECT Distinct player_id, FIRST_VALUE(event_date) OVER(PARTITION BY player_id ORDER BY event_date) AS first_login
FROM Activity
