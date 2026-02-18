# 1. What is HTTP?

- HTTP stands for HyperText Transfer Protocol.


- It's the foundation of communication on the World Wide Web.


- When you type a website address like http://example.com, your browser uses HTTP to request web pages from a server.

```bash

# NOTE: Problem with HTTP: All data sent between your browser and the website (like login details, forms, cookies, etc.) is sent in plain text.

→ Anyone who can intercept the connection (e.g., on public Wi-Fi, rogue ISPs, hackers) can read everything — including passwords, credit card numbers, or private messages.
```

## Key point

* Anyone can read the data
* Not secure
* No guarantee it's the real site
* URL : http://
* Port : 80



# 2. What is HTTPS?

- HTTPS stands for HyperText Transfer Protocol Secure.

- It's basically HTTP + encryption (using TLS/SSL).

```bash
# When you visit https://example.com, the connection is encrypted, so data traveling between your browser and the server is scrambled and unreadable to anyone intercepting it.
```

## keyPoint

* Secure
* Certificate proves the site's identity
* URL : https://
* port : 443
* Only the browser and server can read it
