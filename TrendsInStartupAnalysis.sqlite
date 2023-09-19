--A glimpse of all the startups
SELECT *
FROM startups;

--Total count of all startups
SELECT COUNT(*)
FROM startups;

--Total valuation of all startups
SELECT SUM(valuation)
FROM startups;

--Maximum amount of money raised by a startup
SELECT max(raised)
FROM startups;

----Maximum amount of money raised by a startup during seed stage
SELECT max(raised)
FROM startups
WHERE stage = 'Seed';

--Oldest company in the list was founded on
SELECT MIN(founded)
FROM startups;

--Valuation in different sectors
SELECT AVG(valuation)
FROM startups;

SELECT category,ROUND(AVG(valuation),2)
FROM startups
GROUP BY 1
ORDER BY 2 DESC;

--Most competitive markets
SELECT category, count(*)
FROM startups
GROUP by 1
HAVING COUNT(*) >3
ORDER BY 2 DESC;


--Analyze if there is a difference in startup sizes among different locations
SELECT location, ROUND(AVG(employees),2)
FROM startups
GROUP BY location
ORDER BY 2 DESC;

SELECT location, AVG(employees)
FROM startups
GROUP BY location
HAVING AVG(employees) > 500;

/* -----Final comments-----
There are a total of 70 companies available. 
The total valuation of the companies amount to $974,455,790,000. 
The most competitive markets are Social, Mobile and Education. 
Brooklyn has the highest size based on employees.
*/
