# Natas Level 9 → Level 10

## Topic

Command injection

## Objective

Obtain the password required for the next Natas level.

## Solution

The application passes user input into a shell command.

A normal search can be performed through the form, but the input is insufficiently sanitized.

Use shell command injection to make the server read:

```text
/etc/natas_webpass/natas10
```

For example, the general idea is to terminate the intended command and append another command.

The lesson is that concatenating untrusted input into shell commands is dangerous.

## Key Concepts

This level is primarily about **Command injection**.

## Next Level

After obtaining the password, log in as:

```text
natas10
```

and continue with [Level 10 → Level 11](level10.md) if that file exists.
