# BAC-002 — Unauthenticated Confidential Document Access

## 1. Vulnerability Overview

During the security assessment of OWASP Juice Shop, a confidential document was found accessible without authentication through the application's FTP-related web directory.

## 2. Testing Environment

- Application: OWASP Juice Shop
- Operating System: Kali Linux
- Tool: Firefox
- Testing Method: Direct URL access without an authenticated session

## 3. Testing Procedure

1. Opened a private browsing window.
2. Ensured that no authenticated application session was active.
3. Accessed the following resource directly:

`/ftp/acquisitions.md`

4. Observed that the document was accessible without a login requirement.

## 4. Evidence and Results

- Resource: `/ftp/acquisitions.md`
- HTTP response: 200 OK
- Authentication required: No
- Result: Unauthenticated document access confirmed.

## 5. Security Impact

Unauthorized visitors may access confidential business information if sensitive documents are stored in publicly accessible directories.

## 6. Recommended Remediation

- Restrict access to confidential documents.
- Store sensitive files outside the public web root.
- Implement server-side authentication and authorization.
- Review file permissions and access policies.

## 7. OWASP Reference

OWASP Top 10: A01 — Broken Access Control.

## 8. Finding Status

Confirmed — unauthenticated access to the document was demonstrated in the controlled lab environment.

## 9. Evidence Location

`Evidence/05-Broken-Access-Control/`

## 10. Retesting

Remediation retesting has not been completed. The finding remains open pending implementation and verification of the recommended security controls.
