# Leviathan Level 2 → Level 3

## Objective

Analyze the `printfile` SUID program and find a way around its filename validation.

## Walkthrough

Inspect the program:

```bash
ls -la
file printfile
```

Run it without arguments:

```bash
./printfile
```

It expects a filename.

Trace the program:

```bash
ltrace ./printfile <filename>
```

Also inspect the binary:

```bash
strings printfile
readelf -a printfile
```

The important weakness is the difference between the filename check performed by the program and the way the filename is later passed to a shell command.

This can be abused by supplying a filename containing a space and arranging for the first part of the name to satisfy the access check while the later command execution interprets the remaining text separately.

A useful approach is to create a controlled filename in a writable directory, make the required part accessible, and then use the argument so that the shell invoked by the SUID program processes the second part as another command.

The goal is to make the privileged process read the protected next-level password file.

## Key Concepts

- SUID
- `access()`
- `system()`
- Shell interpretation
- Filename parsing
- Command injection
