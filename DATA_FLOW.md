# Data Flow with Attack Points  
## User → Application → Server → Database

Understanding **where attacks occur during data flow** is critical for **cybersecurity, VAPT, threat modeling, and exams**.

---

##  1. User (Client)

The **user** initiates the data flow by interacting with the system.

### Typical Actions
- Entering credentials
- Submitting forms
- Clicking links or buttons

### Possible Attacks at User Level
- Phishing attacks
- Credential theft
- Social engineering
- Malware infection
- Weak passwords

**Example:**  
User enters login credentials on a fake website created by an attacker.

---

## 2. Application (Frontend / Client Application)

The **application** collects user input and sends it to the server.

### Responsibilities
- Input collection
- Basic client-side validation
- Sending HTTPS requests
- UI rendering

### Possible Attacks at Application Level
- Cross-Site Scripting (XSS)
- Cross-Site Request Forgery (CSRF)
- Client-side validation bypass
- Session hijacking
- Malicious JavaScript injection

**Example:**  
An attacker injects JavaScript into a comment field that executes in another user’s browser.

---

## 3. Network (Between Application & Server)

Data travels over the network between the client and server.

### Possible Attacks at Network Level
- Man-in-the-Middle (MITM)
- Packet sniffing
- DNS spoofing
- SSL stripping

**Example:**  
An attacker intercepts unencrypted traffic on public Wi-Fi.

---

## 4. Server (Backend / Application Server)

The **server** processes requests and enforces business logic.

### Responsibilities
- Authentication & authorization
- Server-side validation
- Business logic execution
- Database interaction

### Possible Attacks at Server Level
- Authentication bypass
- Broken access control (IDOR)
- Command injection
- Insecure deserialization
- Privilege escalation

**Example:**  
Changing a user ID in a request to access another user’s data.

---

## 5. Database

The **database** stores sensitive information.

### Responsibilities
- Data storage and retrieval
- Query execution
- Data consistency

### Possible Attacks at Database Level
- SQL Injection
- Unauthorized data access
- Data manipulation
- Data deletion
- Backup data exposure

**Example:**  
Injecting malicious SQL code to extract all user records.

---

## End-to-End Attack Mapping

| Data Flow Stage | Possible Attacks |
|----------------|-----------------|
| User           | Phishing, malware |
| Application    | XSS, CSRF |
| Network        | MITM, sniffing |
| Server         | IDOR, auth bypass |
| Database       | SQL injection |

---

## Security Controls by Layer

| Layer        | Security Controls |
|-------------|------------------|
| User        | MFA, security awareness |
| Application | Input validation, CSRF tokens |
| Network     | HTTPS, TLS encryption |
| Server      | Access control, logging |
| Database    | Prepared statements, encryption |

---


