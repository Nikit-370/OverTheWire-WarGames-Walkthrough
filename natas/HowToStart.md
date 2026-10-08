# How to Start — Natas

Welcome to the **OverTheWire Natas** wargame.

Natas teaches the basics of **server-side web security**. Unlike Bandit, Natas is primarily browser and HTTP based, so you will spend most of your time inspecting web pages, requests, source code, cookies, parameters, and server behavior.

---

# Official Natas

**Official OverTheWire Wargames:**  
https://overthewire.org/wargames/

**Official Natas:**  
https://overthewire.org/wargames/natas/

---

# 1. What You Need

You need:

- A computer
- An internet connection
- A web browser
- Basic knowledge of HTTP
- Developer Tools

Optional but useful:

- Burp Suite
- `curl`
- Python
- A terminal

You do not need all of these tools to start.

---

# 2. How Natas Works

Each Natas level is a separate web application.

Your goal is to:

```text
Open the current level
        ↓
Analyze the application
        ↓
Find the vulnerability
        ↓
Exploit the vulnerability
        ↓
Obtain the next level password
        ↓
Log in to the next level
```

The level URLs follow this format:

```text
http://natasX.natas.labs.overthewire.org
```

For example:

```text
http://natas0.natas.labs.overthewire.org
http://natas1.natas.labs.overthewire.org
http://natas2.natas.labs.overthewire.org
```

---

# 3. Starting Credentials

The first level is:

```text
Username: natas0
Password: natas0
```

Open:

```text
http://natas0.natas.labs.overthewire.org
```

Enter:

```text
Username: natas0
Password: natas0
```

After logging in, you are ready to begin Level 0.

---

# 4. Start With Level 0

Once you are logged in, do not immediately look at the walkthrough.

First inspect the page yourself.

For example:

- Look at the visible page.
- Right-click and inspect the page.
- Open Developer Tools.
- View the HTML source.
- Look at comments.
- Inspect requests and responses.

For the first level, the password is hidden in the page source.

You can use:

```text
Ctrl + U
```

or:

```text
Right Click → View Page Source
```

Once you find the password, it is used to log in to:

```text
natas1
```

Then continue to the next level.

Start the walkthrough here:

**[Level 0 → Level 1](level0.md)**

---

# 5. Browser Developer Tools

Developer Tools will be one of your most useful tools.

Usually you can open them with:

```text
F12
```

or:

```text
Ctrl + Shift + I
```

Important tabs include:

### Elements

Used to inspect the HTML and page structure.

### Console

Used to interact with JavaScript and inspect client-side behavior.

### Network

Used to inspect:

- HTTP requests
- HTTP responses
- Parameters
- Headers
- Cookies
- Redirects
- Response data

### Application / Storage

Useful for inspecting:

- Cookies
- Local Storage
- Session Storage

---

# 6. View Page Source

Always remember that the browser only shows the rendered version of a webpage.

The HTML source may contain information that is not visible on the page.

Use:

```text
Ctrl + U
```

Look for:

- HTML comments
- Hidden inputs
- JavaScript
- File paths
- Developer notes
- Credentials
- Interesting parameters

---

# 7. HTTP Basics

Natas requires understanding basic HTTP.

A request generally looks like:

```text
Client
   ↓
HTTP Request
   ↓
Web Server
   ↓
HTTP Response
   ↓
Browser
```

A request can contain things such as:

```text
Method
URL
Headers
Cookies
Parameters
Body
```

A response can contain:

```text
Status Code
Headers
Cookies
HTML
JavaScript
Other Data
```

Understanding this request/response cycle is extremely useful throughout Natas.

---

# 8. Useful HTTP Methods

You will commonly encounter:

```text
GET
POST
```

### GET

Parameters are commonly included in the URL:

```text
?name=value
```

Example:

```text
index.php?page=home
```

### POST

Data is normally sent in the request body.

Forms often use POST when submitting information such as usernames and passwords.

---

# 9. Cookies

Cookies are stored by your browser and sent with requests.

You can inspect them using:

```text
Developer Tools → Application/Storage → Cookies
```

You can also inspect them from the Network tab.

A cookie may look like:

```text
PHPSESSID=abcdef123456
```

During Natas, you may encounter levels where cookies influence authentication or application behavior.

Always ask:

```text
Who controls this value?
Can I modify it?
Does the server trust it?
```

---

# 10. Parameters

Web applications frequently use parameters such as:

```text
?page=home
?file=test
?name=user
?debug=1
```

When you see a parameter, investigate what happens when its value changes.

For example:

```text
?page=home
```

Try to understand whether the application:

- Reads a file
- Includes another page
- Searches a database
- Executes a command
- Changes application behavior

Never assume that a parameter is safe just because it appears in the URL.

---

# 11. Useful Command-Line Tools

Natas can also be worked on from the terminal.

Useful commands include:

```bash
curl
wget
grep
strings
base64
xxd
```

For example:

```bash
curl http://example.com
```

You can inspect response headers with:

```bash
curl -i http://example.com
```

You can send custom headers with:

```bash
curl -H "Header: value" http://example.com
```

And cookies with:

```bash
curl -b "cookie=value" http://example.com
```

---

# 12. Burp Suite

Burp Suite is optional, but it is extremely useful for Natas.

It allows you to intercept and modify HTTP requests before they reach the server.

A typical workflow is:

```text
Browser
   ↓
Burp Proxy
   ↓
Natas Server
```

You can inspect and modify:

- Parameters
- Cookies
- Headers
- POST data
- Requests
- Responses

Burp becomes particularly useful when manually changing requests in the browser becomes inconvenient.

---

# 13. Important Web-Security Concepts

As you progress through Natas, you will encounter different types of vulnerabilities.

Some important concepts include:

- Information disclosure
- Source-code disclosure
- Authentication bypass
- Cookie manipulation
- HTTP header manipulation
- Directory traversal
- Local File Inclusion
- Command injection
- SQL injection
- Blind SQL injection
- File upload vulnerabilities
- PHP type juggling
- Session vulnerabilities
- PHP object injection
- Log poisoning
- Cryptographic weaknesses
- Deserialization
- PHAR-related attacks

You do not need to know all of these before starting.

You will learn them level by level.

---

# 14. A Good Way to Solve Each Level

Use this workflow:

```text
1. Read the challenge
        ↓
2. Look at the webpage
        ↓
3. Inspect the HTML source
        ↓
4. Inspect JavaScript
        ↓
5. Inspect requests and responses
        ↓
6. Check parameters and cookies
        ↓
7. Identify the vulnerability
        ↓
8. Test your theory
        ↓
9. Obtain the next password
        ↓
10. Understand why the exploit worked
```

The most important step is:

**Understand why it works.**

Do not simply copy the final request from a walkthrough.

---

# 15. Getting Help

If you are stuck, first investigate the application yourself.

Useful things to inspect include:

```text
Page Source
HTTP Headers
Cookies
GET Parameters
POST Parameters
JavaScript
Response Body
Redirects
File Paths
Error Messages
```

You can also use documentation and command help:

```bash
man curl
```

or:

```bash
curl --help
```

---

# 16. Walkthrough Files

The `natas/` directory contains a separate Markdown file for each level.

```text
natas/
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

Then continue sequentially:

```text
level1.md
level2.md
level3.md
...
```

---

# 17. Important Note

Natas is a security training environment provided by OverTheWire.

Only use these techniques against systems where you have permission to test.

The techniques learned here are intended for:

- CTFs
- Security labs
- Your own applications
- Authorized security testing

---

# 18. Start Your First Level 🚀

Open:

```text
http://natas0.natas.labs.overthewire.org
```

Login with:

```text
Username: natas0
Password: natas0
```

Then inspect the webpage and try to find the password for the next level.

When you are ready:

**[Start Level 0 → Level 1](level0.md)**

Good luck! 🚀

---

## Official Resources

- https://overthewire.org/wargames/
- https://overthewire.org/wargames/natas/