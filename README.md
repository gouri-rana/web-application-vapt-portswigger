# Web Application Vulnerability Assessment & Penetration Testing

## Project Overview

This project involved conducting a controlled Web Application Vulnerability Assessment and Penetration Testing (VAPT) exercise using vulnerable laboratories provided by PortSwigger Web Security Academy.

The assessment focused on identifying, exploiting, analyzing, and documenting common web application and API security vulnerabilities through manual testing using Burp Suite and browser-based interaction.

All testing was performed within authorized training laboratories provided by PortSwigger Web Security Academy.

---

## Objectives

- Identify common web application and API vulnerabilities.
- Analyze application requests, responses, parameters, and attack surfaces.
- Validate vulnerabilities through controlled proof-of-concept exploitation.
- Assess the potential security impact of identified vulnerabilities.
- Document findings along with appropriate remediation recommendations.

---

## Platform

**PortSwigger Web Security Academy**

**Environment:** Authorized vulnerable training laboratories

**Testing Approach:** Manual testing using Burp Suite and browser-based interaction

---

## Tools Used

- **Burp Suite** – HTTP request interception, modification, and analysis
- **Burp Repeater** – Manual request manipulation and vulnerability testing
- **Web Browser** – Application interaction and validation
- **PortSwigger Web Security Academy** – Controlled vulnerable laboratory environment

---

## Methodology

The assessment followed a structured vulnerability testing process:

### 1. Reconnaissance and Application Understanding
- Examined application functionality and user interactions.
- Identified user-controlled inputs, parameters, and relevant endpoints.
- Observed HTTP requests and responses using Burp Suite.
- Identified potential attack surfaces.

### 2. Vulnerability Identification
- Tested relevant endpoints based on the assigned vulnerability.
- Modified request parameters and data.
- Analyzed application behavior and server responses.

### 3. Exploitation and Validation
- Developed and tested appropriate proof-of-concept payloads.
- Confirmed successful exploitation within the controlled laboratory environment.
- Avoided destructive actions outside the scope of the assigned labs.

### 4. Evidence Collection
- Captured relevant Burp Suite requests and responses.
- Documented affected endpoints and testing results.
- Collected proof of successful vulnerability validation.

### 5. Risk Analysis and Remediation
- Assessed the potential impact of each vulnerability.
- Assigned severity based on the laboratory assessment.
- Documented recommended security controls and remediation measures.

---

## Vulnerabilities Assessed

| Vulnerability | Severity | Security Area |
|---|---|---|
| SQL Injection | High | Input Validation / Database Security |
| DOM-Based XSS | Medium | Client-Side Security |
| CSRF | Medium | Access Control |
| CORS Misconfiguration | High | Security Configuration |
| API3 BOPLA / Mass Assignment | High | API Authorization |
| IDOR / API1 BOLA | High | Access Control |
| Race Condition | High | Transaction Security |
| SSRF | Critical | Server-Side Request Handling |

---

## Key Findings

### SQL Injection
- Identified a SQL injection vulnerability in a product category filter.
- Validated a UNION-based injection to retrieve database version information.
- Demonstrated the importance of parameterized queries and strict input validation.

### DOM-Based XSS
- Identified unsafe processing of user-controlled URL input.
- Validated JavaScript execution through a DOM-based XSS vulnerability.
- Highlighted the importance of safe DOM APIs and context-aware output encoding.

### CSRF
- Identified inconsistent CSRF token validation based on the HTTP request method.
- Demonstrated unauthorized modification of account information.
- Recommended consistent CSRF protection for all state-changing requests.

### CORS Misconfiguration
- Identified a CORS configuration that trusted attacker-controlled origins.
- Validated the ability to access sensitive authenticated responses.
- Recommended explicit origin allowlisting and restricted credentialed cross-origin requests.

### API3 BOPLA / Mass Assignment
- Identified an API that accepted an unauthorized sensitive object property.
- Demonstrated manipulation of a discount-related property.
- Recommended property allowlisting and property-level authorization.

### IDOR / API1 BOLA
- Identified predictable object references in a chat transcript functionality.
- Demonstrated unauthorized access to another user's transcript.
- Highlighted the need for server-side authorization and object ownership checks.

### Race Condition
- Identified a race condition in the purchasing workflow.
- Demonstrated how concurrent requests could affect transaction processing.
- Recommended atomic transactions and appropriate concurrency controls.

### SSRF
- Identified a server-side request forgery vulnerability in a stock-check functionality.
- Demonstrated bypass of blacklist-based SSRF protection to access an internal administrative interface.
- Recommended destination allowlisting, URL normalization, and restrictions on internal network resources.

---

## Security Recommendations

The assessment highlighted several recurring security controls:

- Implement strict server-side authorization for objects and individual properties.
- Use parameterized queries and prepared statements.
- Validate and normalize user-controlled input.
- Apply explicit allowlists for trusted origins and server-side request destinations.
- Avoid relying on blacklist-based security controls.
- Implement consistent CSRF protection for state-changing requests.
- Use secure DOM manipulation methods and context-aware output encoding.
- Apply atomic transactions and concurrency controls to sensitive operations.
- Prevent exposure of passwords, API keys, tokens, and other sensitive information.
- Conduct regular vulnerability assessments, API security testing, and security reviews.

---

## Key Skills Demonstrated

- Web Application Security
- Vulnerability Assessment and Penetration Testing (VAPT)
- API Security Testing
- Burp Suite
- HTTP Request Analysis
- SQL Injection Testing
- Cross-Site Scripting (XSS)
- Cross-Site Request Forgery (CSRF)
- Broken Access Control
- BOLA / IDOR
- BOPLA / Mass Assignment
- CORS Security Testing
- Server-Side Request Forgery (SSRF)
- Race Condition Testing
- Security Risk Analysis
- Vulnerability Documentation

---

## Disclaimer

This project was conducted exclusively within authorized vulnerable laboratories provided by PortSwigger Web Security Academy for educational and cybersecurity training purposes.

No unauthorized systems, real-world applications, or third-party infrastructure were targeted. Testing was limited to the assigned laboratory environments and did not include destructive attacks or denial-of-service activity.
