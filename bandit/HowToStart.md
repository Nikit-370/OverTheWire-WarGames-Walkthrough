# How to Start — Bandit

Welcome to the **OverTheWire Bandit** wargame.

Bandit is designed for beginners and teaches the Linux and command-line skills that are useful for solving CTFs and other cybersecurity challenges.

---

## Official Bandit

Before starting, check the official Bandit page:

**Official Bandit:**  
https://overthewire.org/wargames/bandit/

**Official OverTheWire Wargames:**  
https://overthewire.org/wargames/

---

# 1. What You Need

You need:

- A computer
- An internet connection
- A terminal
- SSH

You do **not** need any special cybersecurity software to start Bandit.

---

# 2. Bandit Server Details

The Bandit server uses SSH.

```text
Host: bandit.labs.overthewire.org
Port: 2220
```

The first account is:

```text
Username: bandit0
Password: bandit0
```

---

# 3. Connect to Bandit

Open your terminal and run:

```bash
ssh bandit0@bandit.labs.overthewire.org -p 2220
```

You may see a message asking whether you want to continue connecting to the host.

Type:

```text
yes
```

When asked for the password, enter:

```text
bandit0
```

> **Note:** When typing an SSH password, nothing will appear on the screen. This is normal. Type the password and press Enter.

---

# 4. After Login

Once you successfully log in, you will be inside the Bandit Level 0 environment.

You can check the current user with:

```bash
whoami
```

It should show:

```text
bandit0
```

You can see your current directory with:

```bash
pwd
```

And list the files with:

```bash
ls
```

For Level 0, you should find:

```text
readme
```

The objective is to find the password for the next level.

You can read the file using:

```bash
cat readme
```

The output is the password required for **Bandit Level 1**.

---

# 5. Moving to the Next Level

After obtaining the password for the next level, exit your current SSH session:

```bash
exit
```

Then connect as the next user.

For example:

```bash
ssh bandit1@bandit.labs.overthewire.org -p 2220
```

Enter the password you discovered from the previous level.

The general pattern is:

```text
Current level → solve challenge → obtain next password → login to next level
```

For example:

```text
bandit0
   ↓
solve Level 0
   ↓
get bandit1 password
   ↓
login as bandit1
   ↓
solve Level 1
   ↓
get bandit2 password
   ↓
...
```

---

# 6. Important Commands

During Bandit, you will encounter many Linux commands.

Some of the most useful ones are:

```bash
ls
cd
cat
pwd
find
grep
file
strings
sort
uniq
tr
base64
xxd
tar
gzip
bzip2
ssh
nc
openssl
nmap
chmod
diff
md5sum
git
```

You do not need to memorize all of them before starting.

The challenges are designed to help you learn them.

---

# 7. Useful Linux Basics

## List Files

```bash
ls
```

List hidden files as well:

```bash
ls -la
```

---

## Change Directory

```bash
cd directory
```

Go back one directory:

```bash
cd ..
```

Return to your home directory:

```bash
cd ~
```

---

## Show Current Directory

```bash
pwd
```

---

## Read a File

```bash
cat filename
```

---

## Find Files

A common example:

```bash
find . -type f
```

You can also search based on properties such as size, owner, or permissions.

---

## Search Text

```bash
grep "text" filename
```

---

## Identify a File

```bash
file filename
```

This is particularly useful when a file does not have an obvious extension.

---

# 8. SSH Connection Format

For Bandit, the general SSH command is:

```bash
ssh username@bandit.labs.overthewire.org -p 2220
```

For example:

```bash
ssh bandit0@bandit.labs.overthewire.org -p 2220
```

The username changes as you progress:

```text
bandit0
bandit1
bandit2
bandit3
...
bandit33
```

The server and port remain:

```text
bandit.labs.overthewire.org
2220
```

---

# 9. Where to Find the Walkthroughs

Each level has its own Markdown file in this directory.

```text
bandit/
├── HOW TO START.md
├── level0.md
├── level1.md
├── level2.md
├── level3.md
├── ...
└── level33.md
```

Start here:

**[Level 0 → Level 1](level0.md)**

Then continue with:

```text
level1.md
level2.md
level3.md
...
```

Each file covers the corresponding level transition.

---

# 10. Recommended Approach

Try each challenge yourself before opening the walkthrough.

A good workflow is:

```text
1. Read the objective
       ↓
2. Explore the files/environment
       ↓
3. Try commands
       ↓
4. Read the Linux command documentation if needed
       ↓
5. Try to solve the challenge
       ↓
6. Check the walkthrough if you are stuck
       ↓
7. Understand why the solution works
       ↓
8. Move to the next level
```

Do not just copy commands.

The goal is to understand the techniques so that you can use them on other CTF challenges.

---

# 11. Getting Help

Linux provides built-in documentation.

For many commands, you can use:

```bash
man command
```

For example:

```bash
man find
```

You can also use:

```bash
command --help
```

For example:

```bash
find --help
```

These are useful skills to develop while working through Bandit.

---

# 12. Important Note About Passwords

The passwords discovered during the game are intentionally part of the challenge.

This repository focuses on documenting the **methods and commands used to solve the levels**.

If you are learning Bandit for the first time, try solving the level yourself before looking at the solution.

---

# 13. Start Here 🚀

Once you are connected as `bandit0`, begin with:

```bash
ls
```

Then investigate the files available to you.

When you're ready, check:

**[Bandit Level 0 → Level 1](level0.md)**

Good luck and have fun! 🚀

---

## Official Resources

- [OverTheWire Wargames](https://overthewire.org/wargames/)
- [OverTheWire Bandit](https://overthewire.org/wargames/bandit/)