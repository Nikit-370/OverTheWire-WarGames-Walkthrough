# Natas Level 32 → Level 33

## Topic

`ARGV` and command execution

## Objective

Obtain the password required for the next Natas level.

## Solution

This level extends the previous `ARGV` technique.

Construct a request that causes Perl to interpret attacker-controlled input through the `ARGV` mechanism and execute a command.

The challenge can be automated with a small Python script using `requests`.

The objective is to obtain execution in the context of the Natas application and read the next password.

## Key Concepts

This level is primarily about **`ARGV` and command execution**.

## Next Level

After obtaining the password, log in as:

```text
natas33
```

and continue with [Level 33 → Level 34](level33.md) if that file exists.
