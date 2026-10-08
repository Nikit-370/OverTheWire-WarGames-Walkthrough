# Natas Level 25 → Level 26

## Topic

Path traversal and log poisoning

## Objective

Obtain the password required for the next Natas level.

## Solution

The application includes a language file based on a user-controlled parameter.

It attempts to block path traversal, but the filtering can be bypassed.

Use path traversal to reach the Apache access log, and inject PHP code into the log through a controlled HTTP header such as `User-Agent`.

Then include the poisoned log through the vulnerable file parameter.

The PHP interpreter executes the injected log content, allowing the password file to be read.

Key concepts:

- Path traversal
- Local File Inclusion
- Log poisoning
- Header injection

## Key Concepts

This level is primarily about **Path traversal and log poisoning**.

## Next Level

After obtaining the password, log in as:

```text
natas26
```

and continue with [Level 26 → Level 27](level26.md) if that file exists.
