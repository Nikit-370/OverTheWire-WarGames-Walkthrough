# Natas Level 7 → Level 8

## Topic

Local File Inclusion / path traversal

## Objective

Obtain the password required for the next Natas level.

## Solution

The page parameter controls which file is included.

Normal requests look like:

```text
index.php?page=home
index.php?page=about
```

Try traversing out of the intended directory and reading the password file.

A typical target is:

```text
/etc/natas_webpass/natas8
```

The vulnerability is a Local File Inclusion/path traversal issue caused by trusting the `page` parameter.

## Key Concepts

This level is primarily about **Local File Inclusion / path traversal**.

## Next Level

After obtaining the password, log in as:

```text
natas8
```

and continue with [Level 8 → Level 9](level8.md) if that file exists.
