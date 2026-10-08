# Bandit Level 25 → Level 26

First:

```
cat /etc/passwd | grep bandit26
```

You'll discover that Bandit 26 uses a special shell.

You should find a private key in your home directory:

```
ls
```

Use it:

```
ssh -i bandit26.sshkey bandit26@localhost -p 2220
```

The terminal opens into a `more`-style pager.

The trick is to make the terminal **small enough** that `more` pauses.

While inside `more`, press:

```
v
```

This opens `vi`.

Inside `vi`, enter:

```
:set shell=/bin/bash
```

Then:

```
:shell
```

You should now have a Bash shell as `bandit26`.
