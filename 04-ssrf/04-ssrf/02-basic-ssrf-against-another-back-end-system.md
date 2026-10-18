# Lab 02: Basic SSRF Against Another Back-End System

## Lab Information
- **Platform:** PortSwigger Web Security Academy
- **Category:** Server-Side Request Forgery (SSRF)
- **Difficulty:** Practitioner
- **Lab Status:** Update after testing

## Objective
Understand how an SSRF vulnerability can be used to reach another back-end system accessible from the vulnerable application server.

## Vulnerability Description
Server-Side Request Forgery occurs when an application makes server-side requests to a destination influenced by user input. If destination validation is insufficient, the application may be abused to reach internal systems that are not directly accessible externally.

## Methodology
1. Launch the authorized PortSwigger lab.
2. Inspect the application's functionality and identify the server-side request parameter.
3. Intercept the relevant HTTP request using Burp Suite.
4. Examine how the application handles the destination supplied in that parameter.
5. In the lab environment, follow the instructions to reach the designated back-end system and complete the objective.
6. Record the actual response and verify the lab completion status.

## Security Impact
An SSRF vulnerability may allow unauthorized access to internal services or resources. The severity depends on the reachable systems, accessible functions, and the application's network privileges.

## Recommended Mitigation
- Use strict allowlists for permitted destinations.
- Block access to internal and sensitive network ranges where appropriate.
- Validate resolved IP addresses and restrict redirects.
- Apply network segmentation and outbound firewall rules.
- Avoid relying on basic string matching as the only URL validation mechanism.

## Evidence
Store screenshots of the relevant request, response, and confirmed lab completion in the `evidence/` directory.

## References
- [Official PortSwigger Lab](https://portswigger.net/web-security/ssrf/lab-basic-ssrf-against-another-back-end-system)
- [PortSwigger: SSRF](https://portswigger.net/web-security/ssrf)

**Disclaimer:** Testing is limited to authorized educational labs.
