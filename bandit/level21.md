# Bandit Level 21 → Level 22

**Goal:** Investigate a cron job.

```
ls /etc/cron.d/
```

Look for:

```
cronjob_bandit22
```

Read it:

```
cat /etc/cron.d/cronjob_bandit22
```

Then inspect the script it executes:

```
cat /usr/bin/cronjob_bandit22
```

The script writes the Bandit 22 password to a predictable `/tmp` filename.

You can calculate that filename yourself:

```
echo "I am user bandit22" | md5sum
```

Then:

```
cat /tmp/<hash>
```
