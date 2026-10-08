# Bandit Level 12 → Level 13

This is one of the more important levels.

**Goal:** `data.txt` is repeatedly compressed.

First create a working copy:

```
mkdir /tmp/bandit12
cp data.txt /tmp/bandit12/
cd /tmp/bandit12
```

Convert the hex dump back into binary:

```
xxd -r data.txt data
```

Now inspect it:

```
file data
```

It will tell you whether it is gzip, bzip2, or tar.

### If gzip:

```
mv data data.gz
gzip -d data.gz
```

### If bzip2:

```
mv data data.bz2
bzip2 -d data.bz2
```

### If tar:

```
mv data data.tar
tar -xf data.tar
```

Then:

```
file *
```

Repeat the appropriate decompression operation until you finally get plain text:

```
cat <final-file>
```

This level is essentially practice at recognizing file formats with `file` and peeling off layers.
