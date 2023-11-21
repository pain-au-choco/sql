### [WEATHER OBSERVATION 1](https://www.hackerrank.com/challenges/weather-observation-station-1/problem?isFullScreen=true) ###

Query a list of CITY and STATE from the STATION table.
The STATION table is described as follows:

|  Field | Type |
|-------|-----|
| ID  | NUMBER |
| CITY | VARCHAR2(21)   |
| STATE  | VARCHAR2(2)  |
| LAT_N |  NUMBER |
| LONG_W | NUMBER |

where LAT_N is the northern latitude and LONG_W is the western longitude.

**Solution:**
```sql
SELECT city, state
FROM STATION;
```
###[WEATHER OBSERVATION 2](https://www.hackerrank.com/challenges/weather-observation-station-2/problem?isFullScreen=true)###

Query the following two values from the STATION table:

The sum of all values in LAT_N rounded to a scale of  decimal places.
The sum of all values in LONG_W rounded to a scale of  decimal places.

|  Field | Type |
|-------|-----|
| ID  | NUMBER |
| CITY | VARCHAR2(21)   |
| STATE  | VARCHAR2(2)  |
| LAT_N |  NUMBER |
| LONG_W | NUMBER |

where LAT_N is the northern latitude and LONG_W is the western longitude.

**Solution:**
```sql
SELECT ROUND(SUM(LAT_N), 2) AS lat, ROUND(SUM(LONG_W), 2) AS lon
FROM STATION;

SELECT CAST(ROUND(SUM(LAT_N), 2)AS NUMERIC(12,2)), CAST(ROUND(SUM(LONG_W), 2) AS NUMERIC(12,2)) 
FROM STATION;
```

###[WEATHER OBSERVATION 3](https://www.hackerrank.com/challenges/weather-observation-station-3/problem?isFullScreen=true)###

Query a list of CITY names from STATION for cities that have an even ID number. Print the results in any order, but exclude duplicates from the answer

|  Field | Type |
|-------|-----|
| ID  | NUMBER |
| CITY | VARCHAR2(21)   |
| STATE  | VARCHAR2(2)  |
| LAT_N |  NUMBER |
| LONG_W | NUMBER |

where LAT_N is the northern latitude and LONG_W is the western longitude.

**Solution:**
```sql
SELECT DISTINCT(city) FROM STATION 
WHERE mod(ID,2) = 0;
```

###[WEATHER OBSERVATION 4](https://www.hackerrank.com/challenges/weather-observation-station-4/problem?isFullScreen=true)###

Find the difference between the total number of CITY entries in the table and the number of distinct CITY entries in the table.

|  Field | Type |
|-------|-----|
| ID  | NUMBER |
| CITY | VARCHAR2(21)   |
| STATE  | VARCHAR2(2)  |
| LAT_N |  NUMBER |
| LONG_W | NUMBER |

where LAT_N is the northern latitude and LONG_W is the western longitude.

**Solution:**
```sql
SELECT COUNT(CITY) - COUNT(DISTINCT CITY) AS difference
FROM STATION;
```

###[WEATHER OBSERVATION 6](https://www.hackerrank.com/challenges/weather-observation-station-6/problem?isFullScreen=true)###

Query the list of CITY names starting with vowels (i.e., a, e, i, o, or u) from STATION. Your result cannot contain duplicates.

The STATION table is described as follows:

|  Field | Type |
|-------|-----|
| ID  | NUMBER |
| CITY | VARCHAR2(21)   |
| STATE  | VARCHAR2(2)  |
| LAT_N |  NUMBER |
| LONG_W | NUMBER |

where LAT_N is the northern latitude and LONG_W is the western longitude.

**Solution:**
```sql
SELECT DISTINCT(CITY) 
FROM STATION 
WHERE CITY LIKE 'A%' OR CITY LIKE 'E%' OR CITY LIKE 'I%' OR CITY LIKE 'O%' 
OR CITY LIKE 'U%'
ORDER BY CITY ASC; 
```

###[WEATHER OBSERVATION 7](https://www.hackerrank.com/challenges/weather-observation-station-7/problem?isFullScreen=true)###

Query the list of CITY names ending with vowels (a, e, i, o, u) from STATION. Your result cannot contain duplicates.

The STATION table is described as follows:

|  Field | Type |
|-------|-----|
| ID  | NUMBER |
| CITY | VARCHAR2(21)   |
| STATE  | VARCHAR2(2)  |
| LAT_N |  NUMBER |
| LONG_W | NUMBER |

where LAT_N is the northern latitude and LONG_W is the western longitude.

**Solution:**
```sql
SELECT DISTINCT(CITY)
FROM STATION
WHERE CITY LIKE '%a' OR CITY LIKE '%e' OR CITY LIKE '%i' OR CITY LIKE '%o' OR CITY LIKE '%u';
```
