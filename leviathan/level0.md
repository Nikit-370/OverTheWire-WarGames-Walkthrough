# Leviathan Level 0 → Level 1

## Objective

Find the information required to continue to the next level.

## Walkthrough

Connect using the official starting credentials:

```bash
ssh leviathan0@leviathan.labs.overthewire.org -p 2223
```

List hidden files:

```bash
ls -la
```

A hidden `.backup` directory is present. Inspect it:

```bash
ls -la .backup
```

It contains `bookmarks.html`. Search it for password-related text:

```bash
grep -i password .backup/bookmarks.html
```

The relevant entry contains the information needed for the next level.

## Key Concepts

- Hidden files
- `ls -la`
- `grep`
- Linux filesystem permissions
