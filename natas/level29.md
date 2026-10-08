# Natas Level 29 → Level 30

## Topic

Perl `open()` injection

## Objective

Obtain the password required for the next Natas level.

## Solution

The application is written in Perl and passes user-controlled data to `open()`.

The input is filtered, but Perl's `open()` behavior can interpret special characters as part of a command.

Craft an input that reaches the vulnerable `open()` call and causes command execution or file disclosure.

A null-byte or suffix manipulation can be used to bypass the application's expected filename handling.

The key lesson is to use safe three-argument `open()` calls and never pass untrusted strings to a shell-like interface.

## Key Concepts

This level is primarily about **Perl `open()` injection**.

## Next Level

After obtaining the password, log in as:

```text
natas30
```

and continue with [Level 30 → Level 31](level30.md) if that file exists.
