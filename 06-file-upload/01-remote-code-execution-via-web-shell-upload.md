# Lab: Web Shell Upload via Extension Blacklist Bypass

## Lab Information

| Field | Details |
|---|---|
| Platform | PortSwigger Web Security Academy |
| Difficulty | Practitioner |
| Status | Solved — update after completing the lab |
| Category | File Upload Vulnerability |
| Vulnerability | Extension Blacklist Bypass |
| Potential Impact | Remote Code Execution (RCE) |
| CWE | CWE-434: Unrestricted Upload of File with Dangerous Type |

## 1. Objective

The objective of this lab was to investigate an avatar-upload feature that blocks certain file extensions but contains a weakness in its blacklist-based validation.

The lab requires uploading a PHP web shell, retrieving the contents of `/home/carlos/secret` in the authorized lab environment, and submitting the secret to verify completion.

## 2. Vulnerability Overview

The application blocks certain dangerous file extensions. However, the blacklist is insufficient, and the Apache server configuration can be modified through an uploaded `.htaccess` file.

If an attacker can upload a configuration file that changes how a custom extension is handled, a file with that extension may be executed as PHP code.

## 3. Testing Summary

1. Logged in using the credentials provided by the lab.
2. Inspected the avatar-upload functionality and how uploaded files were accessed.
3. Attempted to upload a PHP script and observed the extension restriction.
4. Examined the upload request and server response using Burp Suite.
5. Investigated the impact of the server's extension blacklist and Apache configuration handling.
6. Verified the behavior of the uploaded files in the authorized lab.
7. Submitted the requested secret and confirmed successful completion.

## 4. Root Cause

The application relied on a blacklist of file extensions instead of a strict allowlist. It also allowed a user-uploaded configuration file to affect server-side script handling.

These weaknesses allowed an extension that was not explicitly blocked to be treated as executable PHP.

## 5. Security Impact

Depending on the server configuration and permissions, this vulnerability may allow:

- Remote code execution under the web server's privileges.
- Unauthorized access to sensitive files.
- Exposure or modification of application data.
- Further compromise of the application environment.

## 6. Remediation

- Use a strict allowlist of permitted file extensions.
- Validate file contents and file signatures, not just the filename.
- Never allow users to upload server configuration files such as `.htaccess`.
- Disable script execution in user-upload directories.
- Store uploaded files outside the web root when possible.
- Generate safe filenames on the server.
- Apply least-privilege filesystem permissions.
- Configure the web server so user uploads cannot change executable content mappings.

## 7. Evidence

Store personally captured lab screenshots in the `evidence/` directory:

- `04-extension-blacklist.png`
- `05-upload-validation.png`
- `06-lab-solved.png`

Do not include session cookies, authentication tokens, or other sensitive data in screenshots.

## 8. Key Takeaway

A blacklist alone is not a reliable file-upload defense. Secure upload handling requires strict file validation, safe storage, and server configuration that prevents uploaded files from changing how executable content is processed.

## References

- [PortSwigger: Official Lab](https://portswigger.net/web-security/file-upload/lab-file-upload-web-shell-upload-via-extension-blacklist-bypass)
- [PortSwigger: File Upload Vulnerabilities](https://portswigger.net/web-security/file-upload)

## Scope and Ethics

Testing should be limited to the authorized PortSwigger Web Security Academy lab or other systems where explicit permission has been granted.

**Author:** Sheikh Sabbir Hossain  
**Portfolio:** [GitHub Repository](https://github.com/sabbihossen/web-security-lab-writeups)
