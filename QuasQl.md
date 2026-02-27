## 🧱 SQL COMMANDS 

### **1. Table Management (DDL)**

| Index + Description                           | MySQL                                                   | PostgreSQL                       | MS SQL                         | Oracle SQL                       |
| --------------------------------------------- | ------------------------------------------------------- | -------------------------------- | ------------------------------ | -------------------------------- |
| **1. Create a table — defines a new table.**  | `CREATE TABLE table_name (col1 INT, col2 VARCHAR(50));` | Same                             | Same                           | Same                             |
| **2. Drop a table — deletes a table.**        | `DROP TABLE table_name;`                                | Same                             | Same                           | Same                             |
| **3. Alter table — add/modify/drop columns.** | `ALTER TABLE table_name ADD col3 DATE;`                 | Same                             | Same                           | Same                             |
| **4. Rename table.**                          | `RENAME TABLE old TO new;`                              | `ALTER TABLE old RENAME TO new;` | `EXEC sp_rename 'old', 'new';` | `ALTER TABLE old RENAME TO new;` |
| **5. Truncate table — removes all data.**     | `TRUNCATE TABLE table_name;`                            | Same                             | Same                           | Same                             |

---

### **2. Data Manipulation (DML)**

| Index + Description                              | MySQL                                                | PostgreSQL                          | MS SQL                            | Oracle SQL                                   |
| ------------------------------------------------ | ---------------------------------------------------- | ----------------------------------- | --------------------------------- | -------------------------------------------- |
| **6. Insert record — add new row.**              | `INSERT INTO table_name (col1,col2) VALUES (1,'A');` | Same                                | Same                              | Same                                         |
| **7. Update record — modify existing data.**     | `UPDATE table_name SET col2='B' WHERE col1=1;`       | Same                                | Same                              | Same                                         |
| **8. Delete record — remove row(s).**            | `DELETE FROM table_name WHERE col1=1;`               | Same                                | Same                              | Same                                         |
| **9. Select data — retrieve records.**           | `SELECT * FROM table_name;`                          | Same                                | Same                              | Same                                         |
| **10. Limit results — restrict number of rows.** | `SELECT * FROM table_name LIMIT 5;`                  | `SELECT * FROM table_name LIMIT 5;` | `SELECT TOP 5 * FROM table_name;` | `SELECT * FROM table_name WHERE ROWNUM <=5;` |

---

### **3. Joins & Relationships**

| Index + Description                                             | MySQL                                                                                       | PostgreSQL                  | MS SQL            | Oracle SQL        |
| --------------------------------------------------------------- | ------------------------------------------------------------------------------------------- | --------------------------- | ----------------- | ----------------- |
| **11. Inner Join — return matching rows.**                      | `SELECT * FROM A INNER JOIN B ON A.id=B.id;`                                                | Same                        | Same              | Same              |
| **12. Left Join — return all from left, matching from right.**  | `SELECT * FROM A LEFT JOIN B ON A.id=B.id;`                                                 | Same                        | Same              | Same              |
| **13. Right Join — return all from right, matching from left.** | `SELECT * FROM A RIGHT JOIN B ON A.id=B.id;`                                                | Same                        | Same              | Same              |
| **14. Full Outer Join — return all rows from both tables.**     | `SELECT * FROM A LEFT JOIN B ON A.id=B.id UNION SELECT * FROM A RIGHT JOIN B ON A.id=B.id;` | `FULL OUTER JOIN` supported | `FULL OUTER JOIN` | `FULL OUTER JOIN` |
| **15. Cross Join — Cartesian product.**                         | `SELECT * FROM A CROSS JOIN B;`                                                             | Same                        | Same              | Same              |

---

### **4. Aggregate Functions**

| Index + Description     | MySQL                               | PostgreSQL | MS SQL | Oracle SQL |
| ----------------------- | ----------------------------------- | ---------- | ------ | ---------- |
| **16. Count rows.**     | `SELECT COUNT(*) FROM table_name;`  | Same       | Same   | Same       |
| **17. Sum values.**     | `SELECT SUM(col1) FROM table_name;` | Same       | Same   | Same       |
| **18. Average values.** | `SELECT AVG(col1) FROM table_name;` | Same       | Same   | Same       |
| **19. Maximum value.**  | `SELECT MAX(col1) FROM table_name;` | Same       | Same   | Same       |
| **20. Minimum value.**  | `SELECT MIN(col1) FROM table_name;` | Same       | Same   | Same       |

---

### **5. Filtering & Sorting**

| Index + Description                 | MySQL                                                   | PostgreSQL | MS SQL | Oracle SQL |
| ----------------------------------- | ------------------------------------------------------- | ---------- | ------ | ---------- |
| **21. WHERE clause — filter rows.** | `SELECT * FROM table_name WHERE col1=5;`                | Same       | Same   | Same       |
| **22. LIKE — pattern matching.**    | `SELECT * FROM table_name WHERE col2 LIKE 'A%';`        | Same       | Same   | Same       |
| **23. IN — match multiple values.** | `SELECT * FROM table_name WHERE col1 IN (1,2,3);`       | Same       | Same   | Same       |
| **24. BETWEEN — range filter.**     | `SELECT * FROM table_name WHERE col1 BETWEEN 1 AND 10;` | Same       | Same   | Same       |
| **25. ORDER BY — sort results.**    | `SELECT * FROM table_name ORDER BY col1 DESC;`          | Same       | Same   | Same       |

---

### **6. Functions & Expressions**

| Index + Description                         | MySQL                | PostgreSQL | MS SQL        | Oracle SQL        |   
| ------------------------------------------- | -------------------- | ---------- | ------------- | ----------------- |  
| **26. Concatenate strings.**                | `CONCAT(col1,col2)`  | Same       | `col1 + col2` | `col1 || col2     |
| **27. Substring — extract part of string.** | `SUBSTRING(col,1,3)` | Same       | Same          | `SUBSTR(col,1,3)` |   
| **28. Uppercase conversion.**               | `UPPER(col)`         | Same       | Same          | Same              |   
| **29. Lowercase conversion.**               | `LOWER(col)`         | Same       | Same          | Same              |   
| **30. Round numeric value.**                | `ROUND(col,2)`       | Same       | Same          | Same              |   

---

### **7. Constraints**

| Index + Description                            | MySQL                                   | PostgreSQL | MS SQL | Oracle SQL |
| ---------------------------------------------- | --------------------------------------- | ---------- | ------ | ---------- |
| **31. Primary Key — unique identifier.**       | `PRIMARY KEY(col)`                      | Same       | Same   | Same       |
| **32. Foreign Key — reference another table.** | `FOREIGN KEY(col) REFERENCES other(id)` | Same       | Same   | Same       |
| **33. Not Null — enforce non-empty value.**    | `col INT NOT NULL`                      | Same       | Same   | Same       |
| **34. Unique — enforce unique values.**        | `col INT UNIQUE`                        | Same       | Same   | Same       |
| **35. Check — enforce condition.**             | `CHECK(col>0)`                          | Same       | Same   | Same       |

---

### **8. Transactions**

| Index + Description                              | MySQL                    | PostgreSQL | MS SQL               | Oracle SQL           |
| ------------------------------------------------ | ------------------------ | ---------- | -------------------- | -------------------- |
| **36. Begin transaction.**                       | `START TRANSACTION;`     | `BEGIN;`   | `BEGIN TRANSACTION;` | `BEGIN TRANSACTION;` |
| **37. Commit transaction.**                      | `COMMIT;`                | Same       | Same                 | Same                 |
| **38. Rollback transaction.**                    | `ROLLBACK;`              | Same       | Same                 | Same                 |
| **39. Savepoint — mark a point in transaction.** | `SAVEPOINT sp1;`         | Same       | Same                 | Same                 |
| **40. Release savepoint.**                       | `RELEASE SAVEPOINT sp1;` | Same       | Same                 | Same                 |

---

### **9. Index & View Management**

| Index + Description                  | MySQL                                  | PostgreSQL             | MS SQL                 | Oracle SQL             |
| ------------------------------------ | -------------------------------------- | ---------------------- | ---------------------- | ---------------------- |
| **41. Create index.**                | `CREATE INDEX idx_name ON table(col);` | Same                   | Same                   | Same                   |
| **42. Drop index.**                  | `DROP INDEX idx_name ON table;`        | `DROP INDEX idx_name;` | `DROP INDEX idx_name;` | `DROP INDEX idx_name;` |
| **43. Create view — virtual table.** | `CREATE VIEW view_name AS SELECT...`   | Same                   | Same                   | Same                   |
| **44. Drop view.**                   | `DROP VIEW view_name;`                 | Same                   | Same                   | Same                   |


---

### **10. DATE / TIME FUNCTIONS**

| Index + Description                                         | MySQL                                  | PostgreSQL                                  | MS SQL                                     | Oracle SQL                                  |
| ----------------------------------------------------------- | -------------------------------------- | ------------------------------------------- | ------------------------------------------ | ------------------------------------------- |
| **45. Current date — returns current date.**                | `CURDATE()`                            | `CURRENT_DATE`                              | `GETDATE()`                                | `SYSDATE`                                   |
| **46. Current time — returns current time.**                | `CURTIME()`                            | `CURRENT_TIME`                              | `GETDATE()`                                | `SYSDATE`                                   |
| **47. Current timestamp — date + time.**                    | `NOW()`                                | `CURRENT_TIMESTAMP`                         | `GETDATE()`                                | `SYSTIMESTAMP`                              |
| **48. Extract year/month/day from date.**                   | `YEAR(date) / MONTH(date) / DAY(date)` | `EXTRACT(YEAR FROM date)` / `MONTH` / `DAY` | `YEAR(date)` / `MONTH(date)` / `DAY(date)` | `EXTRACT(YEAR FROM date)` / `MONTH` / `DAY` |
| **49. Date difference — number of days between two dates.** | `DATEDIFF(date1, date2)`               | `AGE(date1,date2)`                          | `DATEDIFF(day,date2,date1)`                | `date1 - date2`                             |
| **50. Add/subtract interval — add days, months, etc.**      | `DATE_ADD(date, INTERVAL 5 DAY)`       | `date + INTERVAL '5 days'`                  | `DATEADD(day,5,date)`                      | `date + 5`                                  |
| **51. Subtract interval — subtract days, months, etc.**     | `DATE_SUB(date, INTERVAL 3 MONTH)`     | `date - INTERVAL '3 months'`                | `DATEADD(month,-3,date)`                   | `ADD_MONTHS(date,-3)`                       |
| **52. Format date — custom string output.**                 | `DATE_FORMAT(date,'%Y-%m-%d')`         | `TO_CHAR(date,'YYYY-MM-DD')`                | `FORMAT(date,'yyyy-MM-dd')`                | `TO_CHAR(date,'YYYY-MM-DD')`                |
| **53. Truncate to date part — remove time.**                | `DATE(date)`                           | `DATE_TRUNC('day', date)`                   | `CAST(date AS DATE)`                       | `TRUNC(date)`                               |
| **54. Weekday / Day of week.**                              | `DAYOFWEEK(date)`                      | `EXTRACT(DOW FROM date)`                    | `DATEPART(weekday,date)`                   | `TO_CHAR(date,'D')`                         |

---

### **11. MATHEMATICAL FUNCTIONS**

| Index + Description                       | MySQL           | PostgreSQL   | MS SQL       | Oracle SQL          |
| ----------------------------------------- | --------------- | ------------ | ------------ | ------------------- |
| **55. Absolute value.**                   | `ABS(x)`        | Same         | Same         | Same                |
| **56. Round number.**                     | `ROUND(x, n)`   | Same         | Same         | Same                |
| **57. Ceiling — smallest integer ≥ x.**   | `CEIL(x)`       | `CEIL(x)`    | `CEILING(x)` | `CEIL(x)`           |
| **58. Floor — largest integer ≤ x.**      | `FLOOR(x)`      | Same         | Same         | Same                |
| **59. Power — x^y.**                      | `POW(x,y)`      | `POWER(x,y)` | `POWER(x,y)` | `POWER(x,y)`        |
| **60. Square root — √x.**                 | `SQRT(x)`       | Same         | Same         | Same                |
| **61. Modulo — remainder of division.**   | `MOD(x,y)`      | `MOD(x,y)`   | `x % y`      | `MOD(x,y)`          |
| **62. Truncate decimal — drop fraction.** | `TRUNCATE(x,n)` | `TRUNC(x,n)` | `ROUND(x,0)` | `TRUNC(x,n)`        |
| **63. Random number — 0 ≤ x < 1.**        | `RAND()`        | `RANDOM()`   | `RAND()`     | `DBMS_RANDOM.VALUE` |
| **64. Sign — return -1,0,1.**             | `SIGN(x)`       | Same         | Same         | Same                |

---

### **12. DATA TYPE CONVERSIONS**

| Index + Description                             | MySQL                        | PostgreSQL                   | MS SQL                       | Oracle SQL                  |
| ----------------------------------------------- | ---------------------------- | ---------------------------- | ---------------------------- | --------------------------- |
| **65. Convert to integer.**                     | `CAST(col AS SIGNED)`        | `CAST(col AS INTEGER)`       | `CAST(col AS INT)`           | `TO_NUMBER(col)`            |
| **66. Convert to decimal / numeric.**           | `CAST(col AS DECIMAL(10,2))` | `CAST(col AS NUMERIC(10,2))` | `CAST(col AS DECIMAL(10,2))` | `TO_NUMBER(col)`            |
| **67. Convert to string / char.**               | `CAST(col AS CHAR)`          | `CAST(col AS VARCHAR)`       | `CAST(col AS VARCHAR)`       | `TO_CHAR(col)`              |
| **68. Convert to date / timestamp.**            | `CAST(col AS DATE)`          | `CAST(col AS DATE)`          | `CAST(col AS DATE)`          | `TO_DATE(col,'YYYY-MM-DD')` |
| **69. Implicit conversion — auto type change.** | Supported                    | Supported                    | Supported                    | Supported                   |
| **70. Format numeric as string.**               | `FORMAT(col,2)`              | `TO_CHAR(col,'FM9999.00')`   | `FORMAT(col, 'N2')`          | `TO_CHAR(col,'9999.99')`    |

---
### **13. STORED PROCEDURE**

--> MySQL
---

### 1️⃣ Prime Number Check — MySQL

```sql
DELIMITER $$

CREATE PROCEDURE CheckPrime(IN num INT)
BEGIN
    DECLARE i INT DEFAULT 2;
    DECLARE flag INT DEFAULT 0;

    IF num < 2 THEN
        SELECT 'Not Prime';
    ELSE
        WHILE i <= SQRT(num) DO
            IF num % i = 0 THEN
                SET flag = 1;
                LEAVE WHILE;
            END IF;
            SET i = i+1;
        END WHILE;

        IF flag = 0 THEN
            SELECT 'Prime';
        ELSE
            SELECT 'Not Prime';
        END IF;
    END IF;
END$$

DELIMITER ;

CALL CheckPrime(7);
```

✅ Output: `Prime`

---

### 2️⃣ Even Number Check — MySQL

```sql
DELIMITER $$

CREATE PROCEDURE CheckEven(IN num INT)
BEGIN
    IF num % 2 = 0 THEN
        SELECT 'Even';
    ELSE
        SELECT 'Odd';
    END IF;
END$$

DELIMITER ;

CALL CheckEven(8);
```

✅ Output: `Even`

---

### 3️⃣ Sum of Two Numbers — MySQL

```sql
DELIMITER $$

CREATE PROCEDURE AddNumbers(IN a INT, IN b INT)
BEGIN
    SELECT a + b AS SumResult;
END$$

DELIMITER ;

CALL AddNumbers(5, 10);
```

✅ Output: `15`

---
--> PostgreSQL
---

### 1️⃣ Prime Number Check — PostgreSQL

```sql
CREATE OR REPLACE FUNCTION CheckPrime(num INT) RETURNS TEXT AS $$
DECLARE
    i INT := 2;
BEGIN
    IF num < 2 THEN
        RETURN 'Not Prime';
    END IF;

    FOR i IN 2..FLOOR(SQRT(num)) LOOP
        IF num % i = 0 THEN
            RETURN 'Not Prime';
        END IF;
    END LOOP;

    RETURN 'Prime';
END;
$$ LANGUAGE plpgsql;

-- Test
SELECT CheckPrime(7);
```

✅ Output: `Prime`

---

### 2️⃣ Even Number Check — PostgreSQL

```sql
CREATE OR REPLACE FUNCTION CheckEven(num INT) RETURNS TEXT AS $$
BEGIN
    IF num % 2 = 0 THEN
        RETURN 'Even';
    ELSE
        RETURN 'Odd';
    END IF;
END;
$$ LANGUAGE plpgsql;

-- Test
SELECT CheckEven(8);
```

✅ Output: `Even`

---

### 3️⃣ Sum of Two Numbers — PostgreSQL

```sql
CREATE OR REPLACE FUNCTION AddNumbers(a INT, b INT) RETURNS INT AS $$
BEGIN
    RETURN a + b;
END;
$$ LANGUAGE plpgsql;

-- Test
SELECT AddNumbers(5, 10);
```

✅ Output: `15`

---
--> MS SQL
---

### 1️⃣ Prime Number Check — MS SQL

```sql
CREATE PROCEDURE CheckPrime
    @num INT
AS
BEGIN
    DECLARE @i INT = 2;
    DECLARE @flag BIT = 0;

    IF @num < 2
        SELECT 'Not Prime' AS Result;
    ELSE
    BEGIN
        WHILE @i <= SQRT(@num)
        BEGIN
            IF @num % @i = 0
            BEGIN
                SET @flag = 1;
                BREAK;
            END
            SET @i = @i + 1;
        END

        IF @flag = 0
            SELECT 'Prime' AS Result;
        ELSE
            SELECT 'Not Prime' AS Result;
    END
END;
GO

-- Test
EXEC CheckPrime 7;
```

✅ Output: `Prime`

---

### 2️⃣ Even Number Check — MS SQL

```sql
CREATE PROCEDURE CheckEven
    @num INT
AS
BEGIN
    IF @num % 2 = 0
        SELECT 'Even' AS Result;
    ELSE
        SELECT 'Odd' AS Result;
END;
GO

-- Test
EXEC CheckEven 8;
```

✅ Output: `Even`

---

### 3️⃣ Sum of Two Numbers — MS SQL

```sql
CREATE PROCEDURE AddNumbers
    @a INT,
    @b INT
AS
BEGIN
    SELECT @a + @b AS SumResult;
END;
GO

-- Test
EXEC AddNumbers 5, 10;
```

✅ Output: `15`

---

--> Oracle SQL
---

### 1️⃣ Prime Number Check — Oracle SQL

```sql
CREATE OR REPLACE PROCEDURE CheckPrime(num IN NUMBER) IS
    flag NUMBER := 0;
    i NUMBER := 2;
BEGIN
    IF num < 2 THEN
        DBMS_OUTPUT.PUT_LINE('Not Prime');
    ELSE
        WHILE i <= SQRT(num) LOOP
            IF MOD(num, i) = 0 THEN
                flag := 1;
                EXIT;
            END IF;
            i := i + 1;
        END LOOP;

        IF flag = 0 THEN
            DBMS_OUTPUT.PUT_LINE('Prime');
        ELSE
            DBMS_OUTPUT.PUT_LINE('Not Prime');
        END IF;
    END IF;
END;
/

-- Test
BEGIN
    CheckPrime(7);
END;
/
```

✅ Output: `Prime`

---

### 2️⃣ Even Number Check — Oracle SQL

```sql
CREATE OR REPLACE PROCEDURE CheckEven(num IN NUMBER) IS
BEGIN
    IF MOD(num, 2) = 0 THEN
        DBMS_OUTPUT.PUT_LINE('Even');
    ELSE
        DBMS_OUTPUT.PUT_LINE('Odd');
    END IF;
END;
/

-- Test
BEGIN
    CheckEven(8);
END;
/
```

✅ Output: `Even`

---

### 3️⃣ Sum of Two Numbers — Oracle SQL

```sql
CREATE OR REPLACE PROCEDURE AddNumbers(a IN NUMBER, b IN NUMBER) IS
BEGIN
    DBMS_OUTPUT.PUT_LINE('Sum = ' || (a + b));
END;
/

-- Test
BEGIN
    AddNumbers(5, 10);
END;
/
```

✅ Output: `Sum = 15`

---


