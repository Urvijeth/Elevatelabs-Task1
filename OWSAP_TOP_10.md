###Why OWASP Top 10 Matters

1. Most common real-world web vulnerabilities

2. Basis for security testing & compliance

3. Helps developers build secure code

4. Threat modelling & risk assessment foundation

5. Used in VAPT, bug bounties, audits, and compliance

---

###1. A01: Broken Access Control.

####What it is:

Users can access data or functions they shouldn’t (e.g., user accessing admin pages).

####Why dangerous:

####Attackers can:

- View other users’ data

- Modify or delete data

- Perform admin functions without permission

####Example: 

Changing a user ID in the URL to view other people’s profiles.

---

###2. A02: Cryptographic Failures.

####What it is:

Weak or missing encryption for sensitive data.

####Why dangerous:

####Sensitive data is exposed:

- In transit (network)

- At rest (storage)

- In logs or backups

####Example: 

Storing passwords or credit card numbers in plain text.

---

###3. A03: Injection (SQL, Command, LDAP, etc.).

####What it is:

Untrusted input is sent to an interpreter (database, OS) and executed.

####Why dangerous:

####Attackers can:

- Read, modify, or delete database records

- Execute system commands

- Take over the entire application

####Example: 

'; DROP TABLE users; -- in a login form.

---

###4. A04: Insecure Design.

####What it is:

Flaws in design decisions — not just code bugs.

####Why dangerous:

Even perfect code can be insecure if the design has logic flaws.

####Example: 

Trusting user session tokens for sensitive actions without validation.

---

###5. A05: Security Misconfiguration.

####What it is:

Default settings, unnecessary services, or debug enabled in production.

####Why dangerous:

- Misconfigurations are easy entry points:

- Exposed admin panels

- Verbose errors revealing internal info

####Example: 

“admin/admin” default credentials left enabled.

---

###6. A06: Vulnerable and Outdated Components.

####What it is: 

Using old libraries, frameworks, or software with known security flaws.

####Why dangerous:

- Attackers can exploit known bugs without much effort.

####Example: 

Running an outdated CMS with known exploits available publicly.

---

###7. A07: Identification & Authentication Failures.

####What it is:

Weak login mechanisms (passwords, sessions, tokens).

####Why dangerous:

####Attackers can:

- Bypass login

- Hijack sessions

- Reset passwords without validation

####Example: 

No account lockout — attackers can brute-force passwords.

---

###8. A08: Software and Data Integrity Failures.

####What it is:

Trusting code or data without verifying integrity (e.g., unsigned updates).

####Why dangerous:

####Attackers can:

- Inject malware into updates

- Modify code libraries

- Supply unsafe dependencies

####Example: 

Pulling and running an npm package without checking authenticity.

---

####9. A09: Security Logging and Monitoring Failures.

####What it is:

Missing or insufficient logging of security events.

####Why dangerous:

####Attacks go undetected:

- No alarm on breaches

- No forensic trail for investigation

####Example: 

Failed login attempts not logged or alerted.

---

###10. A10: Server-Side Request Forgery (SSRF).

####What it is:

Forcing the server to make malicious requests on attacker’s behalf.

####Why dangerous:

####Attackers can:

- Access internal services

- Scan internal networks

- Exploit cloud metadata services

####Example: 

Submitting a URL to your app that fetches sensitive internal APIs.

---

