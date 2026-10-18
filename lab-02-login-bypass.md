# SQL Injection — Login Bypass

- **Platform:** PortSwigger Web Security Academy
- **Category:** SQL Injection
- **Status:** Solved
- **Environment:** Authorized training lab

## Objective
Understand how SQL injection can affect authentication and allow an attacker to bypass a login mechanism.

## Vulnerability Overview
SQL injection may occur when an application incorporates untrusted input into a database query without proper parameterization.

## Testing Methodology
- Reviewed the login functionality.
- Tested the lab using the techniques covered in the SQL injection lesson.
- Verified the result within the authorized training environment.

## Evidence
Add the actual lab completion screenshot here.

## Impact
If exploitable in a real application, authentication bypass could allow unauthorized access to user accounts or protected functionality.

## Remediation
- Use parameterized queries or prepared statements.
- Avoid building SQL queries through string concatenation.
- Apply appropriate authentication and access controls.

## Key Learning
Learned how SQL injection can affect authentication and why parameterized queries are essential.

## Reference
https://portswigger.net/web-security/sql-injection

