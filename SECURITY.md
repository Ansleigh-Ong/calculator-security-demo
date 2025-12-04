# Security Scanning

## Overview
This repository uses three types of security scanning:

### SAST (Static Analysis with CodeQL)
- Scans source code for vulnerabilities
- Runs on push to main branch
- Checks for: [- Code patterns and logic errors
               - Data flow vulnerabilities]
- Artifacts: See GitHub Security tab

### SCA (Dependency Check)
- Scans Python packages for known CVEs
- Runs on push to main branch
- Checks for: [- Outdated package versions]
- Artifacts: sca-reports

### DAST (Live Application with ZAP)
- Tests running application for vulnerabilities
- Runs on push to main branch
- Checks for: [- Missing security headers
               - Runtime configuration issues
               - API endpoint vulnerabilities]
- Artifacts: zap-baseline-reports, zap-fullscan-reports

## Reporting Vulnerabilities
Please email security@example.com