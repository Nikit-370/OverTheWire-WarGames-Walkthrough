# Natas Level 6 → Level 7

## Topic

Exposed secret in source

## Objective

Obtain the password required for the next Natas level.

## Solution

Inspect the PHP source made available by the application.

The page references a file containing a secret. Retrieve that secret and submit it through the form.

The key technique is source-code inspection: when a challenge gives you source code, read it carefully for file paths, variables, validation logic, and secrets.

## Key Concepts

This level is primarily about **Exposed secret in source**.

## Next Level

After obtaining the password, log in as:

```text
natas7
```

and continue with [Level 7 → Level 8](level7.md) if that file exists.
