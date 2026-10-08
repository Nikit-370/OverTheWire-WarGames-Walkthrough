# Natas Level 5 → Level 6

## Topic

Cookie manipulation

## Objective

Obtain the password required for the next Natas level.

## Solution

The application uses a cookie to decide whether the user is logged in.

Inspect the cookies in Developer Tools. The relevant cookie is initially:

```text
loggedin=0
```

Change it to:

```text
loggedin=1
```

Reload the page.

The lesson is that authentication decisions must never rely solely on a client-controlled cookie value.

## Key Concepts

This level is primarily about **Cookie manipulation**.

## Next Level

After obtaining the password, log in as:

```text
natas6
```

and continue with [Level 6 → Level 7](level6.md) if that file exists.
