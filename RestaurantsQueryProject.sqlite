--Selecting all restaurants
SELECT *
FROM nomnom;

--Selecting the distinct neighbourhoods
SELECT DISTINCT neighborhood
FROM nomnom;

--Selecting the distinct cuisine types
SELECT DISTINCT cuisine
FROM nomnom;

--Options for Chinese takeout
SELECT *
FROM nomnom
WHERE cuisine = 'Chinese';

--List of restaurants with reviews of 4 and above
SELECT *
FROM nomnom
WHERE review >= 4

--Most expensive Italian restaurants
SELECT *
FROM nomnom
WHERE cuisine = 'Italian'
   AND price = '$$$';

--Restaurant serving meatball   
Select *
FROM nomnom 
 WHERE name LIKE '%meatball%';


--Places close enough for delivery
SELECT *
FROM nomnom
  WHERE neighborhood = 'Midtown'
    OR neighborhood  = 'Downtown'
    OR neighborhood  = 'Chinatown';


--Places with health grade pending
SELECT *
FROM nomnom
WHERE health IS NULL; 


--Top 10 restaurants based on review
SELECT *
FROM nomnom 
ORDER BY review DESC
LIMIT 10

--Case statement for rating system 
SELECT *
CASE
  WHEN review > 4.5 THEN 'Extraordinary'
  WHEN review > 4 THEN 'Excellent'
  WHEN review > 3 THEN 'Good'
  WHEN review > 2 THEN 'Fair'
  ELSE 'Poor'
END AS 'Review'
FROM nomnom;
