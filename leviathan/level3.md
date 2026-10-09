# Leviathan Level 3 → Level 4

## Objective

Reverse the password check performed by the `level3` SUID binary.

## Walkthrough

Inspect the executable:

```bash
ls -la
file level3
```

Run it:

```bash
./level3
```

It asks for a password and rejects incorrect input.

Use `ltrace`:

```bash
ltrace ./level3
```

The trace shows `strcmp()` calls. One comparison is internal to the program; another compares the text entered by the user.

Pay attention to the newline added by `fgets()`.

Once the expected input is identified, run:

```bash
./level3
```

The correct input causes the program to provide a shell with elevated effective privileges.

From that shell:

```bash
cat /etc/leviathan_pass/leviathan4
```

Keep the resulting credential out of the public walkthrough.

## Key Concepts

- `ltrace`
- `strcmp()`
- `fgets()`
- SUID
- Input validation
