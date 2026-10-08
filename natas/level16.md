# Natas Level 16 → Level 17

## Topic

Command injection through grep

## Objective

Obtain the password required for the next Natas level.

## Solution

The application searches a dictionary using the supplied input.

The input is inserted into a shell command, but some obvious shell characters are filtered.

Use command substitution and shell syntax that survives the filter to make the command read the `natas17` password file.

A useful strategy is to make the command output depend on whether a guessed character is present, then automate the guesses.

The key lesson is that command injection can still exist even when a few dangerous characters are blacklisted.

## Key Concepts

This level is primarily about **Command injection through grep**.

## Next Level

After obtaining the password, log in as:

```text
natas17
```

and continue with [Level 17 → Level 18](level17.md) if that file exists.
