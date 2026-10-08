# Bandit Level 20 → Level 21

This requires **two terminals**.

The `suconnect` program connects to a port and expects the Level 20 password.

### Terminal 1

```
nc -l 1234
```

### Terminal 2

```
./suconnect 1234
```

Now paste the Level 20 password into Terminal 1.

The program verifies it and returns the Level 21 password.
