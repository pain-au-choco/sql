**[WEATHER OBSERVATION 1] (https://www.hackerrank.com/challenges/weather-observation-station-1/problem?isFullScreen=true)**

Query a list of CITY and STATE from the STATION table.
The STATION table is described as follows:

|  Field | Type |
|-------|-----|
| ID  | NUMBER |
| CITY | VARCHAR2(21)   |
| STATE CODE  | VARCHAR2(2)  |
| LAT_N |  NUMBER |
| LONG_W | NUMBER |

where LAT_N is the northern latitude and LONG_W is the western longitude.

**Solution:**
```sql
SELECT city, state
FROM STATION;
```

**[WEATHER OBSERVATION 6] (https://www.hackerrank.com/challenges/weather-observation-station-6/problem?isFullScreen=true)**

|  Field | Type |
|-------|-----|
| ID  | NUMBER |
| CITY | VARCHAR2(21)   |
| STATE CODE  | VARCHAR2(2)  |
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
