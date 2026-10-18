# File Upload Vulnerabilities

This folder contains my completed PortSwigger Web Security Academy lab write-ups focused on insecure file upload handling.

## Completed Labs

### 01. Remote Code Execution via Web Shell Upload

- **Difficulty:** Apprentice
- **Status:** Solved
- **Vulnerability:** Unrestricted File Upload
- **Key Concepts:** Server-side PHP execution, web shell risk, arbitrary file read

**Lab:** [Open the official PortSwigger lab](https://portswigger.net/web-security/file-upload/lab-file-upload-remote-code-execution-via-web-shell-upload)

## Learning Objectives

- Understand the security risks of unrestricted file uploads.
- Analyze how uploaded files are stored and accessed.
- Understand how unsafe server-side script execution can lead to remote code execution.
- Document security findings and practical remediation strategies.

## Recommended Security Controls

- Allow only explicitly permitted file extensions and validate file content.
- Generate server-side filenames instead of trusting user-provided names.
- Store uploads outside the web root when possible.
- Disable script execution in upload directories.
- Apply least-privilege file permissions.
- Enforce file-size limits and securely process uploaded files.

## Evidence

Screenshots demonstrating the lab completion and relevant observations are stored in the `evidence/` directory.

## Scope and Ethics

All practical testing documented here was performed in the authorized PortSwigger Web Security Academy lab environment. These techniques must only be tested on systems for which explicit authorization has been granted.

**Author:** Sheikh Sabbir Hossain  
**Repository:** [web-security-lab-writeups](https://github.com/sabbihossen/web-security-lab-writeups)
