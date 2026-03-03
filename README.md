# Vulnerable Web Lab (Educational Purpose Only)
# Project Overview:
This is a simple intentionally vulnerable website created for learning and practicing basic web security concepts.
The goal of this project is to understand how common web vulnerabilities work in a safe and controlled environment.

## This project is for educational purposes only.
## Do not use these techniques on websites you do not own.

# Live Demo:
https://unwritten-one.github.io/vulnerable-lab/

# Vulnerabilities Included

# 1️ Reflected XSS (Cross-Site Scripting): 
The search feature directly inserts user input into the page using innerHTML.
## Example payload:
<img src=x onerror=alert("XSS")>
## Why it works:
User input is not sanitized.
innerHTML executes injected HTML/JS.

# 2️ Client-Side Authentication Flaw
Login validation is done entirely in JavaScript.
## Hardcoded credentials:
Username: admin ,
Password: 1234
## Why it is insecure:
Anyone can view source code.
Anyone can modify Document Object Model (DOM) from browser console.
## Example bypass:
document.getElementById("message").innerHTML = "Welcome Admin!";

# 3️ IDOR (Insecure Direct Object Reference)
The profile page reads id directly from the URL parameter:
https://unwritten-one.github.io/vulnerable-lab/profile.html?id=1
## Try modifying:
?id=2
?id=999
?id=admin

## Why it is vulnerable:
No authentication check.
No authorization validation.

# Technologies Used
HTML
Basic JavaScript
GitHub Pages (Hosting)

# Learning Objectives
Understand how XSS works
Learn why client-side validation is insecure
Practice parameter tampering
Analyze source code for vulnerabilities
Develop hacker mindset in a legal way

# How to Use
Open the live demo link.
Try injecting JavaScript in the search field.
Inspect page source.
Manipulate URL parameters.
Use browser developer tools.

⚠️ Disclaimer
This project was created for educational and ethical hacking practice only.
The author is not responsible for misuse of this code.
