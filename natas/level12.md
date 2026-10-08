# Natas Level 12 → Level 13

## Topic

File upload extension bypass

## Objective

Obtain the password required for the next Natas level.

## Solution

The application allows image uploads but generates or controls the filename extension.

Inspect the HTML form and request. The filename is submitted as a parameter and can be modified.

Create a PHP file containing a small payload, then manipulate the upload request so that the server stores it with a `.php` extension instead of the expected image extension.

Access the uploaded PHP file and use it to read the next password.

The vulnerability is insufficient server-side validation of uploaded files.

## Key Concepts

This level is primarily about **File upload extension bypass**.

## Next Level

After obtaining the password, log in as:

```text
natas13
```

and continue with [Level 13 → Level 14](level13.md) if that file exists.
