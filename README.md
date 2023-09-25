# 570.-Managers-with-at-Least-5-Direct-Reports-
 ### Description : [ Managers with at Least 5 Direct Reports](https://leetcode.com/problems/managers-with-at-least-5-direct-reports/description/?envType=study-plan-v2&envId=top-sql-50)


## Solution

```sql
SELECT name FROM Employee
WHERE id IN(
  SELECT managerId FROM employee
  GROUP BY managerId 
  HAVING COUNT(managerId)>=5
  )

