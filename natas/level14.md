# Natas Level 14 → Level 15

## Topic

SQL injection authentication bypass

## Objective

Obtain the password required for the next Natas level.

## Solution

The login form builds a SQL query using user-controlled input.

Analyze the source and identify the SQL query structure.

Use SQL injection to alter the authentication condition. A classic approach is to make the username condition true and comment out or bypass the password portion of the query.

The goal is to make the application authenticate successfully and reveal the `natas15` password.

The lesson is to use parameterized queries rather than concatenating user input into SQL.

## Key Concepts

This level is primarily about **SQL injection authentication bypass**.

## Next Level

After obtaining the password, log in as:

```text
natas15
```

and continue with [Level 15 → Level 16](level15.md) if that file exists.
