# Bandit Level 22 → Level 23

Again inspect the cron job:

```
cat /etc/cron.d/cronjob_bandit23
```

Then:

```
cat /usr/bin/cronjob_bandit23
```

You'll see that it constructs a filename using an MD5 hash.

Calculate it:

```
echo "I am user bandit23" | md5sum
```

Then inspect the corresponding `/tmp` file.

The important lesson here is **reading shell scripts executed by cron and understanding how they construct filenames**.
