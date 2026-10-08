# Natas Level 10 → Level 11

## Topic

Command injection with filtering

## Objective

Obtain the password required for the next Natas level.

## Solution

This level still executes a shell command, but some characters and strings are filtered.

Inspect the source to understand exactly what is blacklisted.

Craft a payload that avoids the blacklist while still causing the shell to read:

```text
/etc/natas_webpass/natas11
```

The important lesson is that blacklist-based command filtering is fragile and can often be bypassed with shell syntax that was not considered by the developer.

## Key Concepts

This level is primarily about **Command injection with filtering**.

## Next Level

After obtaining the password, log in as:

```text
natas11
```

and continue with [Level 11 → Level 12](level11.md) if that file exists.
