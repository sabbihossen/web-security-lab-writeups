# SQL Injection UNION Attack — Determining the Number of Columns

- **Platform:** PortSwigger Web Security Academy
- **Category:** SQL Injection
- **Status:** Solved
- **Environment:** Authorized training lab

## Objective
Determine how many columns are returned by the application's SQL query using a UNION-based SQL injection technique.

## Vulnerability Overview
A UNION-based SQL injection attack can combine results from another query with the original query. The number and compatible data types of columns must match.

## Testing Methodology
Tested the authorized PortSwigger lab and identified the number of columns returned by the query.

## Evidence
Add the actual lab completion screenshot here.

## Impact
Depending on the application's query and database permissions, UNION-based SQL injection may expose data that should not be accessible.

## Remediation
- Use parameterized queries.
- Avoid dynamically concatenating untrusted input into SQL statements.
- Apply least-privilege database permissions.

## Key Learning
Learned how to determine the number of columns in a UNION-based SQL injection scenario.

## Reference
https://portswigger.net/web-security/sql-injection/union-attacks



