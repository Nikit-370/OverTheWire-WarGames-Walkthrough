# Bandit Level 11 → Level 12

**Goal:** Text has been encrypted using ROT13.

```
cat data.txt | tr 'A-Za-z' 'N-ZA-Mn-za-m'
```

You can also use:

```
tr 'A-Za-z' 'N-ZA-Mn-za-m' < data.txt
```
