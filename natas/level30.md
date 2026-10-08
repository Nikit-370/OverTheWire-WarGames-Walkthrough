# Natas Level 30 → Level 31

## Topic

Perl type confusion

## Objective

Obtain the password required for the next Natas level.

## Solution

This level abuses how Perl handles parameters supplied multiple times.

The application expects a scalar value but can receive multiple values. This changes the behavior of its validation logic.

Submit the parameter more than once and use the resulting type/array behavior to bypass the password comparison.

The lesson is that web frameworks and language runtimes may represent repeated parameters differently than developers expect.

## Key Concepts

This level is primarily about **Perl type confusion**.

## Next Level

After obtaining the password, log in as:

```text
natas31
```

and continue with [Level 31 → Level 32](level31.md) if that file exists.
