# Lab 01: Exploiting XXE Using External Entities to Retrieve Files

## Lab Information
- **Platform:** PortSwigger Web Security Academy
- **Category:** XML External Entity (XXE) Injection
- **Difficulty:** Apprentice
- **Lab Status:** Solved

## Objective
Exploit an XML External Entity vulnerability to retrieve a file from the lab server.

## Vulnerability Description
XXE occurs when an application processes XML input containing external entity references without safely restricting them. Depending on the parser configuration, this can allow an attacker to access files available to the application server.

## Methodology
1. Launch the authorized PortSwigger lab.
2. Identify the functionality that accepts XML input.
3. Intercept the relevant request using Burp Suite.
4. Examine how the application parses the submitted XML.
5. In the lab environment, test an external entity declaration that references the designated file.
6. Inspect the response and verify the lab's solved status.

## Security Impact
XXE may expose sensitive server-side files or other resources accessible to the XML parser.

## Recommended Mitigation
- Disable external entity processing where it is not required.
- Disable DTD processing when possible.
- Use securely configured, up-to-date XML parsers.
- Validate input and apply least-privilege permissions.

## Evidence
Add screenshots of the XML request, relevant response, and solved confirmation to the `evidence/` directory.

## References
- [Official PortSwigger Lab](https://portswigger.net/web-security/xxe/lab-exploiting-xxe-to-retrieve-files)
- [PortSwigger: XXE Injection](https://portswigger.net/web-security/xxe)

**Disclaimer:** Testing was conducted in an authorized educational lab.
