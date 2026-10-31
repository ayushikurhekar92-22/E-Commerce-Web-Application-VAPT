# E-Commerce Web Application Vulnerability Assessment & Penetration Testing (VAPT)

## Project Overview

This project focuses on conducting a practical Vulnerability Assessment and Penetration Testing (VAPT) exercise on the OWASP Juice Shop web application in a controlled lab environment.

The assessment involved identifying, validating, documenting, and analyzing web application security weaknesses using manual security testing techniques and industry-standard security tools.

The objective was to understand common web application vulnerabilities, evaluate their potential security impact, and provide appropriate remediation recommendations.

## Project Objectives

- Identify potential web application security vulnerabilities.
- Perform manual security testing and validation.
- Evaluate authentication and access control mechanisms.
- Analyze application security weaknesses.
- Document findings with supporting evidence.
- Recommend suitable mitigation measures.

## Testing Environment

| Component | Details |
|---|---|
| Target Application | OWASP Juice Shop |
| Operating System | Kali Linux |
| Proxy Tool | Burp Suite Community Edition |
| Browser | Firefox |
| Testing Approach | Manual Security Testing |
| Additional Tools | Nmap, curl |
| Environment | Controlled Lab Environment |

## Tools & Technologies

- **Kali Linux** – Security testing environment.
- **Burp Suite Community Edition** – Intercepting and analyzing HTTP requests and responses.
- **Firefox** – Web application testing.
- **Nmap** – Network reconnaissance and scanning.
- **curl** – HTTP request and response analysis.
- **OWASP Juice Shop** – Intentionally vulnerable web application.

## Vulnerability Assessment Methodology

The assessment followed these general stages:

1. **Reconnaissance:** Understanding the target application and identifying accessible endpoints.
2. **Application Mapping:** Reviewing application functionality and HTTP traffic.
3. **Vulnerability Testing:** Performing manual security tests.
4. **Validation:** Analyzing application responses to determine whether vulnerabilities were confirmed.
5. **Risk Analysis:** Evaluating the potential impact of identified weaknesses.
6. **Documentation:** Preparing vulnerability reports and recording observations.
7. **Remediation:** Providing recommendations to address identified security weaknesses.

## Documented Vulnerability Findings

The following findings are documented in the repository:

| Finding ID | Vulnerability | Category |
|---|---|---|
| BAC-001 | Broken Access Control (IDOR/BOLA) | Access Control |
| BAC-002 | Unauthenticated Document Access | Access Control |
| SEC-002 | FTP Directory Listing and File Exposure | Information Disclosure |

### Detailed Finding Reports

- [BAC-001 – Broken Access Control](Findings/BAC-001-Broken-Access-Control.md)
- [BAC-002 – Unauthenticated Document Access](Findings/BAC-002-Unauthenticated-Document-Access.md)
- [SEC-002 – FTP Directory Listing](Findings/SEC-002-FTP-Directory-Listing.md)

Each report contains the vulnerability overview, testing environment, testing procedure, observations, impact, and mitigation recommendations.

## Project Deliverables

The repository includes:

- Individual vulnerability finding reports.
- Supporting project evidence.
- Capstone project presentation.
- Proof of Concept (PoC) report in Excel format.
- Project documentation.

## Repository Structure

```text
E-Commerce-Web-Application-VAPT/
│
├── Evidence/
│   ├── 01-Project-Setup/
│   └── 02-Burp-Suite/
│
├── Findings/
│   ├── BAC-001-Broken-Access-Control.md
│   ├── BAC-002-Unauthenticated-Document-Access.md
│   ├── SEC-002-FTP-Directory-Listing.md
│   └── README.md
│
├── Ecommerce_VAPT_Capstone_Presentation.pptx
├── Ecommerce_VAPT_PoC_Report.xlsx
└── README.md
```

*Note: The presentation filename and folder contents should match the actual uploaded files.*

## Security Recommendations

- Enforce server-side authorization checks.
- Restrict access to sensitive documents and resources.
- Implement proper authentication and session management.
- Disable unnecessary directory listing.
- Apply least-privilege access controls.
- Validate and securely handle user input.
- Conduct regular security assessments.

## Disclaimer

This project was conducted strictly for educational purposes in a controlled lab environment using an intentionally vulnerable application.

No unauthorized testing against real-world systems was performed.

## Author

**Ayushi Kurhekar**

Cybersecurity | Vulnerability Assessment & Penetration Testing | Web Application Security

**Project:** E-Commerce Web Application VAPT

Cybersecurity | Web Application Security | Vulnerability Assessment & Penetration Testing
