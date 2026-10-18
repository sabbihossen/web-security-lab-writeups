# Lab 01: CSRF Where Token Validation Depends on Token Being Present

## Lab Information
- **Platform:** PortSwigger Web Security Academy
- **Category:** Cross-Site Request Forgery (CSRF)
- **Difficulty:** Practitioner
- **Lab Status:** Update after testing

## Objective
Understand how inconsistent CSRF token validation can allow a cross-site request forgery attack.

## Vulnerability Description
The application validates the CSRF token when one is provided but may accept a request when the token is omitted. This inconsistent validation can allow an attacker to bypass the intended protection.

## Methodology
1. Open the authorized PortSwigger lab.
2. Log in using the lab-provided credentials.
3. Identify the account action protected by a CSRF token.
4. Inspect the relevant request using Burp Suite.
5. Compare the application's behavior when the token is present and when it is omitted.
6. Verify whether the application accepts the request without the token.
7. Record the observed result and lab completion status.

## Security Impact
If an application accepts forged requests without validating a CSRF token, an attacker may be able to trigger unwanted actions on behalf of an authenticated user.

## Recommended Mitigation
- Require a valid CSRF token for every state-changing request.
- Reject requests with missing or invalid tokens.
- Use appropriate SameSite cookie settings.
- Validate request origins where appropriate.
- Apply defense in depth to sensitive account actions.

## Evidence
Store screenshots of the relevant request, response, and confirmed lab completion in the `evidence/` directory.

## References
- [Official PortSwigger Lab](https://portswigger.net/web-security/csrf/bypassing-token-validation/lab-token-validation-depends-on-token-being-present)
- [PortSwigger: CSRF](https://portswigger.net/web-security/csrf)

**Disclaimer:** This write-up is for authorized educational testing only.
