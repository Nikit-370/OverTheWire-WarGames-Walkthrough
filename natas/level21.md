# Natas Level 21 → Level 22

## Topic

Session manipulation via a partner server

## Objective

Obtain the password required for the next Natas level.

## Solution

The level uses another application that can set session variables.

The partner site accepts parameters that become session data. Send the appropriate parameters to create an administrator session.

Then reuse the resulting `PHPSESSID` against the main Natas application.

The lesson is that trust boundaries between applications can create authentication bypasses when session data is shared insecurely.

## Key Concepts

This level is primarily about **Session manipulation via a partner server**.

## Next Level

After obtaining the password, log in as:

```text
natas22
```

and continue with [Level 22 → Level 23](level22.md) if that file exists.
