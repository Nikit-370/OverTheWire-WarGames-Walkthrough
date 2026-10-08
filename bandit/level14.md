# Bandit Level 14 → Level 15

**Goal:** Send the current password to port `30000`.

```
nc localhost 30000
```

Paste your Level 14 password and press Enter.

Alternatively:

```
cat /etc/bandit_pass/bandit14 | nc localhost 30000
```
