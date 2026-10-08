# Natas Level 33 — Final Level

## Topic

PHAR deserialization

## Objective

Complete the final normal Natas challenge.

## Solution

The final Natas challenge combines file handling, hashing, and PHP object deserialization.

The application processes a PHAR archive and uses `md5_file()` before deleting or otherwise processing the uploaded file.

Create a malicious PHAR containing a serialized PHP object whose destructor performs an attacker-controlled action.

Arrange the request so the application processes the PHAR and triggers deserialization.

The resulting object-deserialization gadget executes the payload and allows the final password to be obtained.

Key concepts:

- PHAR archives
- PHP serialization
- Magic methods such as `__destruct()`
- File handling
- Object injection
- Hashing sinks

This is the final normal Natas level in the series.


## Key Concepts

- PHAR deserialization
- PHP object injection
- Magic methods
- File handling
- `md5_file()`
- Server-side web security

This is the final normal Natas level.
