# Natas Level 8 → Level 9

## Topic

Encoded secret

## Objective

Obtain the password required for the next Natas level.

## Solution

The application contains a secret in its source code and transforms it before displaying or checking it.

Inspect the source and reverse the transformations in the correct order.

The level uses hexadecimal, Base64, and a custom XOR operation. Decode the value and submit the resulting secret to obtain the `natas9` password.

## Key Concepts

This level is primarily about **Encoded secret**.

## Next Level

After obtaining the password, log in as:

```text
natas9
```

and continue with [Level 9 → Level 10](level9.md) if that file exists.
