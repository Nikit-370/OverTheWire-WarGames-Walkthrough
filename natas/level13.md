# Natas Level 13 → Level 14

## Topic

File type validation bypass

## Objective

Obtain the password required for the next Natas level.

## Solution

This level adds a file signature check to the upload process.

Create a file that begins with valid JPEG magic bytes but also contains executable PHP code.

The goal is to satisfy the file-type check while retaining server-side executable content.

Upload the crafted file, locate the resulting file, and access it so the PHP payload can read the next password.

The lesson is that checking only a file signature is not sufficient to secure uploads when executable files can reach a PHP interpreter.

## Key Concepts

This level is primarily about **File type validation bypass**.

## Next Level

After obtaining the password, log in as:

```text
natas14
```

and continue with [Level 14 → Level 15](level14.md) if that file exists.
