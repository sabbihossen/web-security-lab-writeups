

# Path Traversal — PortSwigger Web Security Academy

## Overview
This section documents my hands-on learning and lab practice on Path Traversal vulnerabilities using PortSwigger Web Security Academy.

**Platform:** PortSwigger Web Security Academy  
**Topic:** File Path Traversal  
**Lab Collection:** https://portswigger.net/web-security/file-path-traversal

## Learning Objectives
- Understand file path traversal vulnerabilities.
- Learn how traversal sequences can be filtered or validated.
- Study absolute path handling and path validation.
- Understand file extension validation and null byte bypass concepts.
- Learn security impact and mitigation techniques.

## Labs and Results

### 1. File path traversal, simple case
**Difficulty:** Apprentice  
**Status:** [Solved / Not Solved]

**What I learned:** How manipulating a file path can potentially allow access to files outside the intended directory.

**Evidence:** Add lab screenshot below.

### 2. File path traversal, traversal sequences blocked with absolute path bypass
**Difficulty:** Practitioner  
**Status:** [Solved / Not Solved]

**What I learned:** How absolute file paths may bypass some traversal-sequence restrictions.

**Evidence:** Add lab screenshot below.

### 3. File path traversal, traversal sequences stripped non-recursively
**Difficulty:** Practitioner  
**Status:** [Solved / Not Solved]

**What I learned:** How incomplete, non-recursive filtering can leave a path traversal weakness.

**Evidence:** Add lab screenshot below.

### 4. File path traversal, validation of start of path
**Difficulty:** Practitioner  
**Status:** [Solved / Not Solved]

**What I learned:** How path validation based on an expected starting directory can be bypassed if implemented incorrectly.

**Evidence:** Add lab screenshot below.

### 5. File path traversal, validation of file extension with null byte bypass
**Difficulty:** Expert  
**Status:** [Solved / Not Solved]

**What I learned:** How flawed file extension validation and null byte handling can affect file access controls in vulnerable environments.

**Evidence:** Add lab screenshot below.

## Security Impact
Path Traversal vulnerabilities can expose sensitive files, configuration data, credentials, or other server-side information, depending on the application's permissions and implementation.

## Mitigation
- Avoid using raw user input to construct file paths.
- Use allowlists for permitted files and directories.
- Canonicalize paths and verify that they remain inside the intended directory.
- Validate file names and extensions securely.
- Apply least-privilege filesystem permissions.
- Test path validation against encoding and normalization edge cases.

## Tools and Resources
- PortSwigger Web Security Academy: https://portswigger.net/web-security/file-path-traversal
- Burp Suite: https://portswigger.net/burp

## Disclaimer
All testing is conducted in authorized training labs for educational purposes.
