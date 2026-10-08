# Natas Level 3 → Level 4

## Topic

robots.txt disclosure

## Objective

Obtain the password required for the next Natas level.

## Solution

Check the site's `robots.txt`:

```text
http://natas3.natas.labs.overthewire.org/robots.txt
```

It reveals a disallowed directory.

Visit the disclosed directory and inspect its files to find the password for `natas4`.

The lesson is that `robots.txt` is not an access-control mechanism.

## Key Concepts

This level is primarily about **robots.txt disclosure**.

## Next Level

After obtaining the password, log in as:

```text
natas4
```

and continue with [Level 4 → Level 5](level4.md) if that file exists.
