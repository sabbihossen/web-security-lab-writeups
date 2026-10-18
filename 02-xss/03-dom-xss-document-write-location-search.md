# Lab 03: DOM XSS in document.write Sink Using location.search

## Lab Information
- **Platform:** PortSwigger Web Security Academy
- **Category:** DOM-Based Cross-Site Scripting
- **Difficulty:** Apprentice
- **Lab Status:** Update after testing

## Objective
Trigger JavaScript execution by exploiting unsafe handling of URL search parameters.

## Vulnerability Description
DOM-based XSS occurs when client-side JavaScript processes attacker-controlled data and passes it to an unsafe DOM sink. In this lab, `location.search` is used as a source and `document.write` as a sink.

## Steps to Reproduce
1. Open the authorized PortSwigger lab.
2. Locate the search functionality.
3. Test the lab-specific proof-of-concept payload.
4. Observe whether JavaScript executes in the browser.
5. Capture the result and verify the lab status.

## Impact
DOM-based XSS can allow script execution in the context of the vulnerable website, depending on the application and its security controls.

## Recommended Mitigation
- Avoid passing untrusted input to unsafe DOM sinks.
- Prefer safe DOM APIs such as `textContent`.
- Validate and encode data according to its output context.
- Use Content Security Policy as an additional defense.

## Evidence
Store screenshots of the test and confirmed result in the `evidence/` directory.

## References
- [Official PortSwigger Lab](https://portswigger.net/web-security/cross-site-scripting/dom-based/lab-document-write-sink)
- [PortSwigger: DOM-Based XSS](https://portswigger.net/web-security/cross-site-scripting/dom-based)

**Disclaimer:** Testing performed only in an authorized educational lab.
