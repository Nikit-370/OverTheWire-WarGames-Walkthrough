# Natas Level 20 → Level 21

## Topic

PHP session parsing

## Objective

Obtain the password required for the next Natas level.

## Solution

This level uses PHP sessions and processes user-controlled session data.

Study how the application parses session input and how newline-separated key/value pairs are handled.

Inject a value that creates an administrative session variable.

The important concept is that session parsing must not allow an attacker to inject additional session fields through uncontrolled input.

## Key Concepts

This level is primarily about **PHP session parsing**.

## Next Level

After obtaining the password, log in as:

```text
natas21
```

and continue with [Level 21 → Level 22](level21.md) if that file exists.
