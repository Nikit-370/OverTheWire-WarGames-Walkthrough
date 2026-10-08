# Bandit Level 5 → Level 6

**Goal:** Find a file that is:

- 1033 bytes
- not executable
- somewhere under `inhere`

```
find inhere -type f -size 1033c ! -executable
```

Then:

```
cat ./inhere/<path-to-file>
```
