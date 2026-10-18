# Lab 02: Stored XSS into HTML Context with Nothing Encoded

## Lab Information
- **Platform:** PortSwigger Web Security Academy
- **Category:** Stored Cross-Site Scripting (XSS)
- **Difficulty:** Apprentice
- **Lab Status:** Update after testing

## Objective
Trigger JavaScript execution through a stored XSS vulnerability.

## Vulnerability Description
Stored XSS occurs when an application stores untrusted input and later displays it to users without appropriate output encoding or sanitization.

## Steps to Reproduce
1. Open the official PortSwigger lab.
2. Locate the comment form.
3. Enter a harmless test payload in a field that accepts the comment:

   ```html
   <script>alert(1)</script>
   ```

4. Complete any required fields and submit the comment.
5. Revisit the page where the comment is displayed.
6. Observe whether the JavaScript alert executes.
7. Record the actual result and lab status.

## Impact
Stored XSS may affect users who view the stored content, depending on the vulnerable context and security controls.

## Recommended Mitigation
- Apply context-aware output encoding.
- Avoid rendering untrusted input as raw HTML.
- Sanitize HTML when HTML input is genuinely required.
- Use a Content Security Policy as an additional defense.

## Evidence
Add screenshots of the submitted comment, observed behavior, and solved status to the `evidence/` directory.

## References
- [Official PortSwigger Lab](https://portswigger.net/web-security/cross-site-scripting/stored/lab-html-context-nothing-encoded)
- [PortSwigger: Stored XSS](https://portswigger.net/web-security/cross-site-scripting/stored)

**Disclaimer:** Educational testing only. Use authorized labs and systems.
