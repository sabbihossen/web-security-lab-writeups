# SQL Injection in WHERE Clause — Retrieving Hidden Data

## Lab Information

- **Platform:** PortSwigger Web Security Academy
- **Category:** SQL Injection
- **Status:** Solved
- **Environment:** Authorized training lab

## Objective

The objective was to exploit a SQL injection vulnerability in a product filtering feature to retrieve data that the application intended to hide.

## Vulnerability Overview

SQL injection occurs when an application incorporates untrusted user input into an SQL query without safely separating data from query instructions.

In a vulnerable product filter, manipulated input may alter the query's logical conditions and expose records that should not be returned.

## Testing Methodology

1. Opened the authorized PortSwigger lab.
2. Inspected the product filtering functionality.
3. Tested how the application handled the filter parameter.
4. Verified the vulnerability by observing whether hidden records became accessible.
5. Confirmed the lab completion.

## Evidence

Add a screenshot from my completed lab here.

- Screenshot: `evidence/lab-01.png`

## Potential Impact

Depending on the affected query and database permissions, SQL injection may expose restricted records or other sensitive application data.

## Remediation

- Use parameterized queries or prepared statements.
- Avoid constructing SQL queries through unsafe string concatenation.
- Apply least-privilege database permissions.
- Handle errors securely and test database queries appropriately.

## Key Learning

This lab demonstrated how unsafe handling of user-controlled filter input can affect SQL query logic and expose hidden records.

## Reference

[PortSwigger — SQL Injection](https://portswigger.net/web-security/sql-injection)
