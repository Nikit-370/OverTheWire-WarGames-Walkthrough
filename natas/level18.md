# Natas Level 18 → Level 19

## Topic

PHP session ID prediction

## Objective

Obtain the password required for the next Natas level.

## Solution

The application uses a predictable PHP session identifier.

Inspect the source and understand how the session ID is generated. The valid session range is small enough to brute-force.

Use repeated requests to obtain candidate session IDs and identify the session associated with the privileged user.

Once the privileged session is obtained, use its PHPSESSID cookie to access the protected page and obtain the next password.

The lesson is that session identifiers must be unpredictable and generated using secure randomness.

## Key Concepts

This level is primarily about **PHP session ID prediction**.

## Next Level

After obtaining the password, log in as:

```text
natas19
```

and continue with [Level 19 → Level 20](level19.md) if that file exists.
