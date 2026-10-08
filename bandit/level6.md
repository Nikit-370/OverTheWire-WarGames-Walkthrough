# Bandit Level 6 → Level 7

**Goal:** Find a file anywhere on the server:

- owned by `bandit7`
- group `bandit6`
- 33 bytes

```
find / -user bandit7 -group bandit6 -size 33c 2>/dev/null
```

Then `cat` the result.

The `2>/dev/null` hides the huge number of permission-denied messages.
