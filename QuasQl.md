
---

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

| Index + Description                         | MySQL                | PostgreSQL | MS SQL        | Oracle SQL        |   |       |
| ------------------------------------------- | -------------------- | ---------- | ------------- | ----------------- | - | ----- |
| **26. Concatenate strings.**                | `CONCAT(col1,col2)`  | Same       | `col1 + col2` | `col1             |   | col2` |
| **27. Substring — extract part of string.** | `SUBSTRING(col,1,3)` | Same       | Same          | `SUBSTR(col,1,3)` |   |       |
| **28. Uppercase conversion.**               | `UPPER(col)`         | Same       | Same          | Same              |   |       |
| **29. Lowercase conversion.**               | `LOWER(col)`         | Same       | Same          | Same              |   |       |
| **30. Round numeric value.**                | `ROUND(col,2)`       | Same       | Same          | Same              |   |       |

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


Do you want me to do that next?
