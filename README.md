### What is this?
Simple experiment to apply database indexing to improve query performance for a hypothetical `customer` table, containing 50 million rows on a `country` column. Uses partial indexes.

### Test Environment
- PostgreSQL 13
- PgAdmin 4
- Windows 11 HSL (AMD Ryzen 5)

### Results

For the query `SELECT * FROM customers WHERE country='United Kingdom';`

Using `EXPLAIN ANALYZE` query for obtaining actual run-time statistics on the required statement before and after indexing.

- Query Execution Time without index: 41836.270 ms
- Query Execution Time with index: 24254.644 ms
- Improvement in query execution time ~42.03%

Related article can be found <a href="https://dev.to/karishmashukla/how-to-improve-the-performance-of-your-database-by-indexing-large-tables-1j17">here.</a>
