# Bandit Level 16 → Level 17

**Goal:** Find which port between `31000` and `32000` is listening, then identify the SSL service.

```
nmap -sV localhost -p 31000-32000
```

Find the SSL-enabled port.

Then:

```
openssl s_client -connect localhost:<PORT>
```

Paste the Level 16 password.

One of the responses will be an SSH private key.

Save it:

```
nano /tmp/bandit17.key
```

Paste the key, then:

```
chmod 600 /tmp/bandit17.key
ssh -i /tmp/bandit17.key bandit17@localhost -p 2220
```
