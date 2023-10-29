--Creating a trip log with the trips and it's users
SELECT *
FROM trips
LEFT JOIN riders 
  ON trips.rider_id = riders.id;

--Creating a link between trips and cars
SELECT *
FROM trips
JOIN cars
  ON trips.car_id = cars.id;

--Adding new riders to old data
SELECT *
FROM riders
UNION
SELECT *
FROM riders2;

--Average cost for a trip
SELECT ROUND(AVG(cost), 2)
FROM trips;

--The riders who have used lyft less than 500 times in both present and past data
SELECT *
FROM riders
WHERE total_trips < 500
UNION
SELECT *
FROM riders2
WHERE total_trips < 500;

--Number of cars that are active
SELECT COUNT(*)
FROM cars
WHERE status = 'active';

--Top two cars that have the highest number of trips completed
SELECT *
FROM cars
ORDER BY trips_completed DESC
LIMIT 2;
