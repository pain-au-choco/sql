### [REVISING THE SELECT QUERY 1](https://www.hackerrank.com/challenges/revising-the-select-query/problem?isFullScreen=true) ###

Query all columns for all American cities in the CITY table with populations larger than 100000. The CountryCode for America is USA.

The CITY table is described as follows:

|  Field        | Type         |
|---------------|--------------|
| ID            | NUMBER       |
| NAME          | VARCHAR2(17) |
| COUNTRY CODE  | VARCHAR2(3)  |
| DISTRICT      | VARCHAR2(20) |
| POPULATION    | NUMBER       |

**Solution:**
```sql
SELECT *
FROM CITY
WHERE POPULATION > 100000
AND COUNTRYCODE = 'USA';
```

### [REVISING THE SELECT QUERY 2](https://www.hackerrank.com/challenges/revising-the-select-query-2/problem?isFullScreen=true) ###

Query the NAME field for all American cities in the CITY table with populations larger than 120000. The CountryCode for America is USA.

The CITY table is described as follows:

|  Field        | Type         |
|---------------|--------------|
| ID            | NUMBER       |
| NAME          | VARCHAR2(17) |
| COUNTRY CODE  | VARCHAR2(3)  |
| DISTRICT      | VARCHAR2(20) |
| POPULATION    | NUMBER       |

**Solution:**
```sql
SELECT NAME
FROM CITY
WHERE POPULATION > 120000
AND CountryCode = 'USA';
```
