# Natas Level 11 → Level 12

## Topic

XOR-encrypted cookie

## Objective

Obtain the password required for the next Natas level.

## Solution

Inspect the PHP source and analyze how the cookie is encrypted.

The cookie is encrypted with XOR and encoded for transport. The source contains enough information to recover the encryption key.

Recover the key, construct a modified cookie that sets the desired value, encode it in the same format, and send it back to the server.

The key lesson is that client-side encrypted state is not secure when the encryption key and algorithm can be recovered from the application.

## Key Concepts

This level is primarily about **XOR-encrypted cookie**.

## Next Level

After obtaining the password, log in as:

```text
natas12
```

and continue with [Level 12 → Level 13](level12.md) if that file exists.
