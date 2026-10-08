# Bandit Level 4 → Level 5

**Goal:** Find the only human-readable file.

```
cd inhere
file ./*
```

Look for the file identified as ASCII/text, then:

```
cat ./<filename>
```

For example, you can automate it:

```
file ./* | grep text
```
