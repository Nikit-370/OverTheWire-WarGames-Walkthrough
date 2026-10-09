# Leviathan Level 1 → Level 2

## Objective

Analyze a SUID executable and understand its password comparison.

## Walkthrough

Inspect the home directory:

```bash
ls -la
file check
ls -l check
```

`check` is a SUID executable owned by the next-level account.

Run it:

```bash
./check
```

It asks for a password. Rather than guessing, trace its library calls:

```bash
ltrace ./check
```

Look for `strcmp()`. The trace exposes the string being compared with your input.

Run the program again and provide the value identified by the trace:

```bash
./check
```

A successful comparison gives you a shell running with the executable owner's effective privileges.

From that shell, the next-level password file can be accessed:

```bash
cat /etc/leviathan_pass/leviathan2
```

Do not publish the resulting credential in the repository.

## Key Concepts

- SUID
- Effective privileges
- `ltrace`
- `strcmp()`
- Dynamic analysis
