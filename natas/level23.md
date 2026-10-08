# Natas Level 23 → Level 24

## Topic

PHP type juggling

## Objective

Obtain the password required for the next Natas level.

## Solution

The application checks whether a password contains a required substring and also compares it numerically.

PHP's loose comparison rules can cause a string beginning with digits to be converted to a number.

Use a value such as:

```text
123iloveyou
```

The numeric portion satisfies the numeric comparison while the full string satisfies the substring check.

The lesson is to understand PHP's implicit type conversion and prefer strict comparisons when appropriate.

## Key Concepts

This level is primarily about **PHP type juggling**.

## Next Level

After obtaining the password, log in as:

```text
natas24
```

and continue with [Level 24 → Level 25](level24.md) if that file exists.
