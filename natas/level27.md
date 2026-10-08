# Natas Level 27 → Level 28

## Topic

MySQL truncation

## Objective

Obtain the password required for the next Natas level.

## Solution

The application creates users in a MySQL database and checks for an existing username.

MySQL can truncate a value to the column's maximum length. Trailing spaces can therefore create a collision between a specially crafted username and an existing username.

Create a username based on the target account followed by enough spaces and additional characters to exploit the truncation behavior.

The duplicate account can then be used to obtain the target user's password.

The key lesson is to validate usernames consistently and understand database type/length semantics.

## Key Concepts

This level is primarily about **MySQL truncation**.

## Next Level

After obtaining the password, log in as:

```text
natas28
```

and continue with [Level 28 → Level 29](level28.md) if that file exists.
