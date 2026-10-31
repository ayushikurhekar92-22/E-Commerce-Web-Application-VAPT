# E-Commerce Web Application Vulnerability Assessment & Penetration Testing

## Project Overview

This project demonstrates a practical Web Application Vulnerability Assessment and Penetration Testing (VAPT) exercise conducted on OWASP Juice Shop, an intentionally vulnerable e-commerce application.

The assessment was performed in a controlled local lab environment using Kali Linux, Docker, Burp Suite Community Edition, Firefox and cURL.

The objective was to identify, validate and document potential web application security weaknesses through controlled manual testing.

## Tools & Technologies

- Kali Linux
- OWASP Juice Shop
- Docker
- Burp Suite Community Edition
- Firefox
- cURL
- HTTP/HTTPS
- OWASP Top 10

## Testing Areas

1. SQL Injection
2. Authentication Testing
3. Session Management
4. Broken Access Control (IDOR/BOLA)
5. Cross-Site Scripting (XSS)
6. Security Headers and CORS
7. FTP Directory Listing and File Exposure

## Key Findings

| Finding | Result |
|---|---|
| Cross-account basket access (IDOR/BOLA) | Confirmed |
| Unauthenticated confidential document access | Confirmed |
| FTP directory listing and file exposure | Confirmed |
| SQL Injection | Inconclusive |
| Stored XSS | Inconclusive |
| DOM XSS | Observed – inconsistent |
| Session invalidation | Inconclusive |
| Security Headers and CORS | Informational |

## Methodology

1. Lab environment setup and target identification.
2. Application reconnaissance and endpoint discovery.
3. HTTP traffic interception using Burp Suite.
4. Manual security testing using Burp Repeater.
5. Evidence collection and validation.
6. Vulnerability classification and severity assessment.
7. Security recommendations and reporting.

## Recommendations

- Implement server-side object-level authorization.
- Restrict access to confidential documents.
- Disable unnecessary directory listing.
- Use parameterized SQL queries.
- Implement appropriate input validation and output encoding.
- Strengthen session invalidation mechanisms.
- Configure restrictive CORS policies and security headers.

## Project Limitations

- Testing was conducted against an intentionally vulnerable local training application.
- The assessment was time-bound and manually performed.
- Some tests remained inconclusive or could not be consistently reproduced.
- Severity ratings were provisional qualitative assessments, not CVSS-scored.
- Remediation was recommended but not verified through a completed retest.

## Disclaimer

This project was conducted strictly for educational purposes in a controlled lab environment using OWASP Juice Shop. No unauthorized systems or real user accounts were targeted.

## Author

*Ayushi Kurhekar*

Cybersecurity | Web Application Security | Vulnerability Assessment & Penetration Testing
