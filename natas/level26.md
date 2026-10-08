# Natas Level 26 → Level 27

## Topic

PHP object injection

## Objective

Obtain the password required for the next Natas level.

## Solution

The application serializes a PHP object and stores it in a cookie.

Inspect the source and identify the object's destructor behavior. The destructor writes data to a file.

Construct a serialized object with attacker-controlled properties so that, when the object is destroyed, it writes PHP code into a web-accessible location.

Then access the generated file and execute the payload.

The vulnerability is PHP object injection caused by unsafe deserialization of attacker-controlled data.

## Key Concepts

This level is primarily about **PHP object injection**.

## Next Level

After obtaining the password, log in as:

```text
natas27
```

and continue with [Level 27 → Level 28](level27.md) if that file exists.
