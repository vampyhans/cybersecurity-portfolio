# TryHackMe - Protocols and Servers 2

## Overview

The **Protocols and Servers 2** room explores authentication mechanisms, password attacks, and secure communication protocols. It introduces common password attack techniques, demonstrates the use of Hydra for password auditing, and discusses modern authentication and mitigation strategies.

---

## Learning Objectives

- Understand authentication factors
- Learn common password attack techniques
- Perform password auditing with Hydra
- Understand secure authentication practices
- Learn mitigation strategies against password attacks

---

## Skills Practiced

- Authentication
- Password Security
- Network Protocols
- Hydra
- Security Best Practices
- Service Enumeration

---

## Protocols Covered

| Protocol | Default Port | Purpose |
|----------|-------------:|---------|
| POP3 | 110 | Retrieve emails |
| IMAP | 143 | Synchronize emails |
| SMTP | 25 | Send emails |
| SSH | 22 | Secure remote administration |
| HTTP | 80 | Web communication |
| HTTPS | 443 | Secure web communication |

---

## Authentication Factors

Authentication can be based on one or more of the following:

- **Something you know** (Password, PIN)
- **Something you have** (Phone, Security Key, Smart Card)
- **Something you are** (Fingerprint, Face Recognition)

Combining multiple factors creates **Multi-Factor Authentication (MFA)**, significantly improving security.

---

## Password Attack Techniques

### Password Guessing

Attempts passwords based on personal information about the target.

Example:
- Pet names
- Birth years
- Favourite sports teams

---

### Dictionary Attack

Attempts passwords from a predefined wordlist.

Common wordlists include:

- RockYou
- SecLists
- CrackStation

---

### Brute Force Attack

Attempts every possible password combination until the correct one is found.

Longer passwords dramatically increase the time required for successful brute-force attacks.

---

### Credential Stuffing

Uses leaked username/password combinations from previous data breaches against other services.

This attack relies on password reuse.

---

### Password Spraying

Attempts a few common passwords against many user accounts.

This helps avoid account lockout mechanisms.

---

### Hybrid Attack

Combines dictionary words with common variations.

Examples:

- Summer2024
- Password123
- P@ssw0rd

---

## Hydra

Hydra is a fast password auditing tool capable of testing authentication against numerous network protocols.

### Basic Syntax

```bash
hydra -l username -P wordlist.txt TARGET_IP ssh
```

### Common Options

| Option | Description |
|---------|-------------|
| `-l` | Single username |
| `-L` | Username list |
| `-p` | Single password |
| `-P` | Password wordlist |
| `-s` | Custom port |
| `-V` | Verbose output |
| `-f` | Stop after first successful login |

---

## Other Password Auditing Tools

- Medusa
- Ncrack
- CrackMapExec / NetExec
- Burp Suite Intruder
- Hashcat
- John the Ripper

---

## Password Attack Mitigation

Effective defences include:

- Strong password policies
- Multi-Factor Authentication (MFA)
- Account lockout
- Rate limiting
- CAPTCHA
- Passwordless authentication
- Breached password detection
- Behavioural analysis
- IP-based restrictions

Using multiple defences together provides better protection than relying on a single control.

---

## Key Takeaways

- Weak and reused passwords remain one of the biggest security risks.
- Hydra automates password auditing across multiple network services.
- Choosing an appropriate wordlist significantly improves password auditing effectiveness.
- MFA is one of the strongest protections against password attacks.
- Understanding authentication mechanisms is essential for penetration testing and security assessments.

---

## Tools Used

- Hydra
- Telnet
- Linux Terminal

---

## References

- TryHackMe – Protocols and Servers 2
- Hydra Documentation

---

## Disclaimer

This writeup documents concepts learned during the room for educational purposes. It intentionally excludes challenge answers, flags, passwords, or assessment-specific solutions in accordance with responsible disclosure and platform guidelines.