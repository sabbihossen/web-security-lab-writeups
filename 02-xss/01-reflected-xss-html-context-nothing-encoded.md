# Lab 01: Reflected XSS into HTML Context with Nothing Encoded

## Lab Information
- **Platform:** PortSwigger Web Security Academy
- **Category:** Cross-Site Scripting (XSS)
- **Difficulty:** Apprentice
- **Lab Status:** Solved
- **Vulnerability:** Reflected Cross-Site Scripting

## Objective
Trigger the JavaScript `alert()` function by exploiting the reflected XSS vulnerability in the search functionality.

## Vulnerability Description
The application reflects user-supplied search input into the HTML response without proper output encoding. As a result, the browser interprets the injected HTML and JavaScript as executable code.

## Steps to Reproduce
1. Launch the authorized PortSwigger lab.
2. Locate the search functionality.
3. Enter the following proof-of-concept payload into the search box:

   ```html
   <script>alert(1)</script>
   ```

4. Click **Search**.
5. Observe the JavaScript alert dialog.
6. Confirm that the lab is marked as solved.

## Impact
In a real application, reflected XSS may allow an attacker to execute JavaScript in another user's browser under the vulnerable site's origin. The actual impact depends on the application's security controls and context.

## Root Cause
User-controlled input is reflected into an HTML response without context-appropriate output encoding.

## Recommended Mitigation
- Apply context-aware output encoding.
- Use safe templating practices and avoid inserting untrusted input as raw HTML.
- Apply a Content Security Policy (CSP) as an additional defense.
- Validate input where appropriate, but do not rely on input validation alone.

## Evidence
See the `evidence/` directory for screenshots captured during the lab.

## References
- [Official PortSwigger Lab](https://portswigger.net/web-security/cross-site-scripting/reflected/lab-html-context-nothing-encoded)
- [PortSwigger: Reflected XSS](https://portswigger.net/web-security/cross-site-scripting/reflected)
- [OWASP: Cross Site Scripting Prevention Cheat Sheet](https://cheatsheetseries.owasp.org/cheatsheets/Cross_Site_Scripting_Prevention_Cheat_Sheet.html)

**Disclaimer:** This write-up documents an authorized educational lab. Test only systems for which you have permission.
