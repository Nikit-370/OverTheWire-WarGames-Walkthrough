# Leviathan Level 4 → Level 5

## Objective

Find a hidden executable and decode the data it produces.

## Walkthrough

List hidden files:

```bash
ls -la
```

A hidden `.trash` directory contains the relevant executable.

Inspect it:

```bash
ls -la .trash
file .trash/*
```

Run the executable and capture its output:

```bash
./.trash/<program>
```

The output is a sequence of binary byte values rather than normal text.

Convert each binary value to its character representation. Python is convenient for this:

```bash
python3 -c 's=input(); print("".join(chr(int(x,2)) for x in s.split()))'
```

Paste the program's binary output when prompted.

The decoded text provides the information required to continue.

## Key Concepts

- Hidden directories
- Binary representation
- Character encoding
- Python
- Data decoding
