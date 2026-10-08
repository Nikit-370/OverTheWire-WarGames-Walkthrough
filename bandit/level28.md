# Bandit Level 28 → Level 29

Clone the repository similarly:

```
git clone ssh://bandit28-git@bandit.labs.overthewire.org:2220/home/bandit28-git/repo
cd repo
```

Check:

```
cat README.md
```

It won't directly give you the password.

Look at the commit history:

```
git log
```

Then inspect previous commits:

```
git show <commit>
```

You should find the password in an earlier commit.
