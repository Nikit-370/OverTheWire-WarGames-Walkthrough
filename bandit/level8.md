# Bandit Level 8 → Level 9

**Goal:** Find the line that occurs only once.

```
sort data.txt | uniq -u
```

This works because `uniq` detects adjacent duplicates, so sorting first is important.
