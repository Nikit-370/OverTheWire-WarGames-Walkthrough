# Leviathan Level 6 → Level 7

## Objective

Find a four-digit code accepted by the `leviathan6` program.

## Walkthrough

Inspect the program:

```bash
ls -la
file leviathan6
```

Run it without an argument:

```bash
./leviathan6
```

It expects a four-digit code.

There are only 10,000 possible values, so automation is practical.

A simple shell loop is enough:

```bash
for i in $(seq -w 0000 9999); do
    ./leviathan6 "$i" 2>/dev/null
done
```

Watch the output for the successful attempt.

Once the correct code is accepted, the program reveals the information needed for the next level.

## Key Concepts

- Small key spaces
- Brute force
- Shell loops
- Automation
- Program exit/output behavior
