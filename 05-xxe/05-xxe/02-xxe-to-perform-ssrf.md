**# Lab 02: Exploiting XXE to Perform SSRF Attacks

## Lab Information
- **Platform:** PortSwigger Web Security Academy
- **Category:** XXE Injection / SSRF
- **Difficulty:** Apprentice
- **Lab Status:** Solved

## Objective
Understand how an XXE vulnerability can be used to trigger a server-side request in the lab environment.

## Vulnerability Description
When an XML parser processes attacker-controlled external entity references, it may initiate requests to external or internal destinations. This can create an SSRF vulnerability through the XML processing functionality.

## Methodology
1. Launch the authorized PortSwigger lab.
2. Identify the XML-processing endpoint.
3. Intercept the relevant request using Burp Suite.
4. Examine how external entities are processed.
5. In the lab environment, use the documented lab objective to demonstrate a server-side request through XXE.
6. Inspect the response and confirm that the lab is solved.

## Security Impact
XXE-to-SSRF may allow a vulnerable application to make requests to resources reachable from the server, potentially exposing internal services.

## Recommended Mitigation
- Disable external entity resolution and unnecessary DTD processing.
- Use secure XML parser configurations.
- Restrict outbound server connections.
- Apply network segmentation and least-privilege controls.
- Monitor unexpected server-side requests.

## Evidence
Store screenshots of the relevant XML request, response, and solved confirmation in the `evidence/` directory.

## References
- [Official PortSwigger Lab](https://portswigger.net/web-security/xxe/lab-exploiting-xxe-to-perform-ssrf)
- [PortSwigger: XXE Injection](https://portswigger.net/web-security/xxe)

**Disclaimer:** Testing was conducted in an authorized educational lab.
**
