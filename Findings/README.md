# Vulnerability Assessment Findings

This folder contains the documented findings identified during the E-Commerce Web Application VAPT assessment conducted on OWASP Juice Shop.

## Confirmed Findings

### 1. BAC-001 — Broken Access Control (IDOR/BOLA)
Cross-account basket access was demonstrated by modifying the basket ID in an authenticated API request.

### 2. BAC-002 — Unauthenticated Confidential Document Access
The `/ftp/acquisitions.md` resource was accessible without authentication.

### 3. SEC-002 — FTP Directory Listing and File Exposure
The `/ftp/` directory exposed a directory listing, and selected files were accessible.

## Documentation

Each finding includes:
- Vulnerability overview
- Testing methodology
- Evidence and results
- Potential security impact
- Recommended remediation
- Finding status

All testing was conducted in a controlled OWASP Juice Shop lab environment.
