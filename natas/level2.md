# Natas Level 2 → Level 3

## Topic

Directory listing and exposed files

## Objective

Obtain the password required for the next Natas level.

## Solution

Inspect the page source. An image references a `files/` directory.

Open:

```text
http://natas2.natas.labs.overthewire.org/files/
```

The directory listing exposes files including `users.txt`.

Open `users.txt` and locate the `natas3` entry.

The vulnerability is information disclosure through an exposed directory listing.

## Key Concepts

This level is primarily about **Directory listing and exposed files**.

## Next Level

After obtaining the password, log in as:

```text
natas3
```

and continue with [Level 3 → Level 4](level3.md) if that file exists.
