# Natas Level 22 → Level 23

## Topic

Hidden redirect / `revelio` parameter

## Objective

Obtain the password required for the next Natas level.

## Solution

The application redirects normal visitors away from the protected functionality.

Inspect the source and identify the special `revelio` parameter.

Request the page with the parameter while preventing your HTTP client from automatically following the redirect.

With `curl`:

```bash
curl -u natas22:PASSWORD -i "http://natas22.natas.labs.overthewire.org/?revelio=1"
```

Look at the response before the redirect is followed. The password is exposed by the protected code path.

## Key Concepts

This level is primarily about **Hidden redirect / `revelio` parameter**.

## Next Level

After obtaining the password, log in as:

```text
natas23
```

and continue with [Level 23 → Level 24](level23.md) if that file exists.
