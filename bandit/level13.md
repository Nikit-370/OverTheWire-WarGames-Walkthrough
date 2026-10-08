# Bandit Level 13 → Level 14

**Goal:** You aren't given the password directly. You're given an SSH private key.

```
ls
```

You'll find:

```
sshkey.private
```

Use it:

```
ssh -i sshkey.private bandit14@localhost -p 2220
```

Once logged in:

```
cat /etc/bandit_pass/bandit14
```

That gives the password for Level 14. The official challenge confirms that the private key is the intended method.
