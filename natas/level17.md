# Natas Level 17 → Level 18

## Topic

Blind SQL injection

## Objective

Obtain the password required for the next Natas level.

## Solution

This level uses a SQL query but does not directly display the result.

The application response changes depending on whether the SQL condition succeeds.

Use Boolean or timing-based inference to extract the password one character at a time.

A Python script with `requests` can automate:

1. Guess a character.
2. Inject a condition comparing the guessed character.
3. Observe the response or timing.
4. Keep the correct character.
5. Repeat until the password is recovered.

This is a classic blind SQL injection technique.

## Key Concepts

This level is primarily about **Blind SQL injection**.

## Next Level

After obtaining the password, log in as:

```text
natas18
```

and continue with [Level 18 → Level 19](level18.md) if that file exists.
