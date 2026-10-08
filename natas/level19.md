# Natas Level 19 → Level 20

## Topic

Obfuscated session IDs

## Objective

Obtain the password required for the next Natas level.

## Solution

This level continues the session-ID attack but changes the representation of the session identifier.

The session value is encoded rather than appearing as a simple sequential number.

Inspect the session format and reverse the encoding. Then enumerate candidate values and send the corresponding cookies until the privileged session is found.

Automate the process rather than checking thousands of values manually.

The underlying weakness remains predictable session generation.

## Key Concepts

This level is primarily about **Obfuscated session IDs**.

## Next Level

After obtaining the password, log in as:

```text
natas20
```

and continue with [Level 20 → Level 21](level20.md) if that file exists.
