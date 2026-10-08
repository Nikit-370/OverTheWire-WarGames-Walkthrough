# Bandit Level 31 → Level 32

Clone:

```
git clone ssh://bandit31-git@bandit.labs.overthewire.org:2220/home/bandit31-git/repo
cd repo
```

Read:

```
cat README.md
```

The instructions tell you to create a file called:

```
key.txt
```

Put the Level 31 password into it:

```
echo "YOUR_LEVEL31_PASSWORD" > key.txt
```

Git may ignore the file, so force-add it:

```
git add -f key.txt
git commit -m "add key"
git push
```

The repository accepts the push and gives you the Level 32 password.
