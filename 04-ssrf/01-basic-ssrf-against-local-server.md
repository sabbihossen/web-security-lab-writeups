# Lab 01: Basic SSRF Against the Local Server

## Lab Information
- **Platform:** PortSwigger Web Security Academy
- **Category:** Server-Side Request Forgery (SSRF)
- **Difficulty:** Apprentice
- **Lab Status:** Solved

## Objective
Exploit a server-side request forgery vulnerability to access a local service running on the application server.

## Vulnerability Description
Server-Side Request Forgery (SSRF) occurs when an application makes server-side requests to a destination influenced by user-controlled input. If the destination is not properly restricted, an attacker may be able to make requests to internal services.

## Methodology
1. Open the authorized PortSwigger lab.
2. Inspect the application's functionality and identify the server-side request parameter.
3. Use Burp Suite to intercept and examine the relevant HTTP request.
4. Modify the destination to target the local server, as required by the lab.
5. Follow the lab instructions to access the internal service and complete the objective.
6. Verify that the lab displays the solved status.

## Impact
SSRF may expose internal services or resources that are not directly accessible from outside the application. The impact depends on the server's network access and the protections in place.

## Recommended Mitigation
- Apply strict allowlists for permitted destinations.
- Block requests to loopback, private, and link-local addresses where appropriate.
- Validate resolved IP addresses and re-check redirects.
- Restrict outbound network access using firewall rules.
- Avoid relying on simple string checks to validate URLs.

## Evidence
Screenshots documenting the relevant request, response, and lab completion are stored in the `evidence/` directory.

## References
- [Official PortSwigger Lab](https://portswigger.net/web-security/ssrf/lab-basic-ssrf-against-localhost)
- [PortSwigger: Server-Side Request Forgery](https://portswigger.net/web-security/ssrf)

**Disclaimer:** Testing was performed in an authorized educational lab.
