# Natas Level 15 → Level 16

## Topic

Blind SQL injection

## Objective

Obtain the password required for the next Natas level.

## Solution

The application checks whether a username exists but does not directly reveal the database contents.

This creates a Boolean-based blind SQL injection primitive.

Test conditions against the `users` table and determine whether your injected condition is true based on the application's response.

You can automate character-by-character extraction with Python and `requests`.

The objective is to recover the password for `natas16` without the application directly printing the database value.

## Key Concepts

This level is primarily about **Blind SQL injection**.

## Next Level

After obtaining the password, log in as:

```text
natas16
```

and continue with [Level 16 → Level 17](level16.md) if that file exists.
