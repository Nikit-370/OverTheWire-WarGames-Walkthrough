# Natas Level 31 → Level 32

## Topic

`ARGV` filehandle injection

## Objective

Obtain the password required for the next Natas level.

## Solution

The application uses Perl's `ARGV` filehandle to process a submitted file.

Manipulate the parameter so Perl treats attacker-controlled input as a filehandle or command source rather than an ordinary filename.

This can be combined with request parameters to make the server read or execute unintended content.

The lesson is to treat special filehandles and command-capable input paths as dangerous when they are influenced by users.

## Key Concepts

This level is primarily about **`ARGV` filehandle injection**.

## Next Level

After obtaining the password, log in as:

```text
natas32
```

and continue with [Level 32 → Level 33](level32.md) if that file exists.
