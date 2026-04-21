# ApexPlanet-Web-Application-Security-Task-3
# Task 3 - Web Application Security

**Name:** Anjali Kumari
**ID:** APSPL2631216

---

## Objective
To identify, exploit, and provide mitigation strategies for OWASP Top 10 
vulnerabilities in a controlled lab environment using industry-standard 
penetration testing tools.

---

## Tools Used
- **Target Application:** DVWA (Damn Vulnerable Web Application)
- **Operating System:** Kali Linux
- **Proxy & Interception:** Burp Suite Community Edition
- **Database:** MariaDB 11.8.6
- **Attack Techniques:** SQL Injection, Stored Cross-Site Scripting (XSS)

---

## Work Done
- **SQL Injection (SQLi):** Exploited the User ID field using `' OR '1'='1` 
  payload to extract all user records from the database.
- **Advanced SQLi:** Used `' UNION SELECT 1, version() #` to extract the 
  backend database version (MariaDB 11.8.6).
- **Stored XSS:** Injected malicious JavaScript into the DVWA Guestbook field, 
  causing a persistent popup alert on every page load.
- **Burp Suite:** Intercepted and manually manipulated raw HTTP GET/POST 
  requests using the Proxy Intercept feature before they reached the server.

---

## Vulnerabilities Covered

| Vulnerability | Exploit Used | Mitigation |
|---|---|---|
| SQL Injection (SQLi) | `' OR '1'='1`, UNION SELECT | Prepared Statements, Least Privilege |
| Stored XSS | `<script>alert()</script>` in Guestbook | Output Encoding, CSP Headers |

---

## Output
- DVWA exploitation screenshots with proof of concept.
- GitHub Repository with detailed vulnerability analysis and mitigation steps.
- 5-minute Demo Video showing SQLi and XSS exploitation with Burp Suite.

---

## Conclusion
Successfully completed Task 3, demonstrating the ability to identify and exploit 
web application vulnerabilities (SQLi and Stored XSS) and implement effective 
mitigation strategies including prepared statements, output encoding, and 
Content Security Policy (CSP) headers.
