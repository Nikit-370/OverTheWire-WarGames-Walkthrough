# Natas Level 28 → Level 29

## Topic

AES-ECB and SQL injection

## Objective

Obtain the password required for the next Natas level.

## Solution

The application encrypts the search query using AES in ECB mode.

Because ECB encrypts identical plaintext blocks identically, ciphertext blocks can be rearranged or combined.

Analyze the encrypted request and construct a ciphertext that makes the server execute a modified SQL query.

The attack combines:

- SQL injection
- Block-size analysis
- AES-ECB properties
- Ciphertext block manipulation

Use a script to determine the block boundaries and construct the final ciphertext.

## Key Concepts

This level is primarily about **AES-ECB and SQL injection**.

## Next Level

After obtaining the password, log in as:

```text
natas29
```

and continue with [Level 29 → Level 30](level29.md) if that file exists.
