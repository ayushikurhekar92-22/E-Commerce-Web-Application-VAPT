# SEC-002 — FTP Directory Listing and File Exposure

## 1. Vulnerability Overview

During the security assessment of OWASP Juice Shop, the FTP-related web directory was found to expose a directory listing containing file and folder names. Selected files were also accessible through direct HTTP requests.

## 2. Testing Environment

- Application: OWASP Juice Shop
- Operating System: Kali Linux
- Tools: Firefox and HTTP response inspection
- Testing Method: Manual directory and file access testing

## 3. Testing Procedure

1. Navigated to the application's FTP-related directory:

`/ftp/`

2. Observed the directory listing.
3. Reviewed the listed files and folders.
4. Tested access to selected resources.
5. Recorded the HTTP response status codes.

## 4. Evidence and Results

- Directory: `/ftp/`
- Directory listing: HTTP 200 OK
- `acquisitions.md`: HTTP 200 OK
- `incident-support.kdbx`: HTTP 200 OK
- Three other tested files: HTTP 403 Forbidden
- `/ftp/quarantine/` was also listed.

Note: The accessibility of the KDBX file was identified through its HTTP response. Its contents were not extracted or verified.

## 5. Security Impact

Directory listing may disclose internal file names, directory structures and potentially sensitive resources.

Unauthorized access to exposed files could result in information disclosure.

## 6. Recommended Remediation

- Disable directory listing on the web server.
- Restrict access to sensitive directories.
- Remove confidential and backup files from the public web root.
- Apply appropriate server-side access controls.
- Review file permissions and exposed resources.
- Verify access restrictions after remediation.

## 7. OWASP Reference

OWASP Top 10: A01 — Broken Access Control.

## 8. Finding Status

Confirmed — directory listing and selected file accessibility were demonstrated in the controlled lab environment.

## 9. Evidence Location

`Evidence/07-Security-Misconfiguration/`

## 10. Retesting

Remediation retesting has not been completed. The finding remains open pending implementation and verification of the recommended security controls.
