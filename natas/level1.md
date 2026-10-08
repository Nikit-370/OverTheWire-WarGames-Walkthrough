# Natas Level 1 → Level 2

## Topic

Right-click protection bypass

## Objective

Obtain the password required for the next Natas level.

## Solution

The page attempts to prevent right-clicking, but this is only a client-side restriction.

Open Developer Tools with `F12`, or directly use View Source:

```text
view-source:http://natas1.natas.labs.overthewire.org/
```

Inspect the HTML and locate the comment containing the password for `natas2`.

The lesson is that client-side UI restrictions do not protect source code.

## Key Concepts

This level is primarily about **Right-click protection bypass**.

## Next Level

After obtaining the password, log in as:

```text
natas2
```

and continue with [Level 2 → Level 3](level2.md) if that file exists.
