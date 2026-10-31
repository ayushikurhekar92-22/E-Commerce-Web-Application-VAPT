# BAC-001 — Broken Access Control (IDOR/BOLA)

## 1. Vulnerability Overview

During the security assessment of OWASP Juice Shop, a Broken Access Control vulnerability was identified. An authenticated user could access another user's shopping basket by modifying the basket ID in an API request.

## 2. Testing Environment

- Application: OWASP Juice Shop
- Operating System: Kali Linux
- Tool: Burp Suite Community Edition
- Testing Method: Manual API security testing
- Accounts: Account A and Account B

## 3. Testing Procedure

1. Created two separate test accounts.
2. Logged in using Account A and captured its basket request.
3. Logged in using Account B and captured its basket request.
4. Identified the basket IDs belonging to both accounts.
5. Intercepted Account A's basket request using Burp Suite.
6. Modified the basket ID from Account A's basket to Account B's basket.
7. Replayed the modified request without changing the authentication token.

## 4. Evidence and Results

- Account A basket ID: 6
- Account B basket ID: 7
- Modified request response: HTTP 200 OK
- Response contained Account B's basket information.
- Returned UserId: 26

**Result:** Unauthorized cross-account basket access was successfully demonstrated in the controlled testing environment.

## 5. Security Impact

An authenticated user could potentially access another user's private shopping basket information, resulting in unauthorized disclosure of user-specific data.

## 6. Recommended Remediation

- Implement server-side object-level authorization.
- Verify basket ownership for every API request.
- Restrict access to resources based on authenticated user identity.
- Never rely solely on user-supplied object IDs.
- Perform authorization checks before returning sensitive information.

## 7. OWASP Reference

OWASP Top 10: A01 — Broken Access Control.

## 8. Finding Status

Confirmed — cross-account basket access was demonstrated through manual testing.

## 9. Evidence Location

Supporting screenshots are maintained in:

`Evidence/05-Broken-Access-Control/`

## 10. Retesting

Remediation retesting has not been completed. The finding remains open pending implementation and verification of the recommended security controls.
