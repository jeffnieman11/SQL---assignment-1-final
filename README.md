# SQL---assignment-1-final;
#Question 1 - answer is Honolulu - query follows;
SELECT dest FROM flights ORDER BY distance DESC LIMIT 1; 

#Question 2 part A- answer is 1,2,3,4 - query follows;
SELECT DISTINCT engines FROM planes ORDER BY engines;
#Question 2 part B - answer is 16 - query follows;
SELECT DISTINCT engines, manufacturer, model, seats FROM planes WHERE engines='1' ORDER BY seats DESC LIMIT 1;
#Question 2 part C - answer is 400 - query follows;
SELECT DISTINCT engines, manufacturer, model, seats FROM planes WHERE engines='2' ORDER BY seats DESC LIMIT 1;
#Question 2 part D - answer is 379 - query follows;
SELECT DISTINCT engines, manufacturer, model, seats FROM planes WHERE engines='3' ORDER BY seats DESC LIMIT 1;
#Question 2 part E - answer is 450 - query follows;
SELECT DISTINCT engines, manufacturer, model, seats FROM planes WHERE engines='4' ORDER BY seats DESC LIMIT 1;

#Question 3 - answer is 336776 - query follows;
SELECT COUNT(flight) FROM flights;

#Question 4 - query follows;
SELECT carrier, COUNT(flight) FROM flights GROUP BY carrier ORDER BY carrier;

#Question 5 - query follows;
SELECT carrier, COUNT(flight) FROM flights GROUP BY carrier ORDER BY COUNT(flight) DESC;

#Question 6 - query follows;
SELECT carrier, COUNT(flight) FROM flights GROUP BY carrier ORDER BY COUNT(flight) DESC LIMIT 5;

#Question 7 - query follows;
SELECT carrier, COUNT(flight) FROM flights WHERE distance>1000 GROUP BY carrier ORDER BY COUNT(flight) DESC LIMIT 5;

#Question 8 - 8.	What are the average temperatures of each airport of origin sorted from highest to lowest?  - Query follows;
SELECT origin, AVG(temp) FROM weather GROUP BY origin ORDER BY AVG(temp) DESC;
