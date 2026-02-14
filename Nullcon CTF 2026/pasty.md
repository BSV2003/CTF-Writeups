# 🧩 Pasty — Web Challenge

📍 Event: Nullcon CTF 2026  
📂 Category: Web  
⭐ Points: 50  

---

## 📌 Overview

Pasty was a web-based challenge that simulated a secure pastebin service.

Private pastes were protected using a custom cryptographic signature system.  
The objective was to analyze this mechanism and access the restricted "flag" paste.

---

## 🔍 Initial Reconnaissance

As my first major web challenge, I started with basic analysis:

- Opened the website
- Created sample pastes
- Observed URL parameters
- Checked request/response behavior
- Downloaded the provided `sig.php` file

This helped me understand how the application handled authentication.

---

## ⚠️ Vulnerability Analysis

After reviewing the source code, I noticed that:

- The application used a custom-made cryptographic method
- It did not use standard HMAC or secure libraries
- The signature generation was predictable

This made it possible to recreate valid signatures.

---

## 🛠️ Exploitation Strategy

My approach was:

1. Study the signature logic in `sig.php`
2. Understand how paste IDs were signed
3. Reproduce the same logic locally
4. Generate valid signatures for restricted IDs
5. Use the forged signature to access private pastes

---

## 🔧 Tools Used

- Web Browser  
- Browser DevTools  
- PHP / Python (basic scripting)  
- Text Editor  

---

## 🏁 Result

Using the forged signature, I successfully accessed the protected paste and retrieved the flag.

---

## 📚 Lessons Learned

- Why custom cryptography is insecure
- Importance of standard security libraries
- How to analyze source code
- How to approach web challenges systematically
- Value of documentation and references

---

This challenge played a major role in improving my confidence in solving web-based CTF problems.

