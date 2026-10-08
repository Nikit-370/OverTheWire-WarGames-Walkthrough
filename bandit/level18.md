# Bandit Level 18 → Level 19

This one has a trick: the normal SSH login immediately logs you out.

Instead, execute a command directly:

```
ssh bandit18@bandit.labs.overthewire.org -p 2220 cat readme
```

You'll get the password without starting the restricted shell.
