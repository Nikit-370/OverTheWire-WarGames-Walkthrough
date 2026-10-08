# Natas Level 4 → Level 5

## Topic

HTTP Referer validation

## Objective

Obtain the password required for the next Natas level.

## Solution

The application checks the HTTP `Referer` header.

Send a request with the expected Referer value using `curl`:

```bash
curl -e "http://natas5.natas.labs.overthewire.org/" http://natas4.natas.labs.overthewire.org/
```

You can also modify the Referer header in browser DevTools or Burp Suite.

The server trusts a client-controlled HTTP header, allowing the check to be bypassed.

## Key Concepts

This level is primarily about **HTTP Referer validation**.

## Next Level

After obtaining the password, log in as:

```text
natas5
```

and continue with [Level 5 → Level 6](level5.md) if that file exists.
