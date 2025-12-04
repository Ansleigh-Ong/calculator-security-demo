# Security Scan Analysis - [4/12/2025]

## DAST Results (ZAP Baseline)
- Total URLs scanned: 3
- PASS: 61 checks
- WARN-NEW: 9 warnings
- FAIL-NEW: 0 failures

### Warning Summary
WARN-NEW: Missing Anti-clickjacking Header [10020] x 1 
	http://localhost:5000 (200 OK)
WARN-NEW: X-Content-Type-Options Header Missing [10021] x 1 
	http://localhost:5000 (200 OK)
WARN-NEW: Server Leaks Version Information via "Server" HTTP Response Header Field [10036] x 3 
	http://localhost:5000 (200 OK)
	http://localhost:5000/robots.txt (404 Not Found)
	http://localhost:5000/sitemap.xml (404 Not Found)
WARN-NEW: Content Security Policy (CSP) Header Not Set [10038] x 2 
	http://localhost:5000 (200 OK)
	http://localhost:5000/robots.txt (404 Not Found)
WARN-NEW: Storable and Cacheable Content [10049] x 3 
	http://localhost:5000 (200 OK)
	http://localhost:5000/robots.txt (404 Not Found)
	http://localhost:5000/sitemap.xml (404 Not Found)
WARN-NEW: Permissions Policy Header Not Set [10063] x 3 
	http://localhost:5000 (200 OK)
	http://localhost:5000/robots.txt (404 Not Found)
	http://localhost:5000/sitemap.xml (404 Not Found)
WARN-NEW: Modern Web Application [10109] x 1 
	http://localhost:5000 (200 OK)
WARN-NEW: Insufficient Site Isolation Against Spectre Vulnerability [90004] x 3 
	http://localhost:5000 (200 OK)
	http://localhost:5000 (200 OK)
	http://localhost:5000 (200 OK)
WARN-NEW: Sec-Fetch-Dest Header is Missing [90005] x 12 
	http://localhost:5000 (200 OK)
	http://localhost:5000/robots.txt (404 Not Found)
	http://localhost:5000/sitemap.xml (404 Not Found)
	http://localhost:5000 (200 OK)
	http://localhost:5000/robots.txt (404 Not Found)

## SCA Results (Dependency Check)
- High severity: 0
- Medium severity: 0
- Low severity: 0

### Vulnerable Packages
none

## SAST Results (CodeQL)
❌ High Severity:Flask app is run in debug mode
File: app.py
Line: 40
Issue: Running a Flask application with debug mode enabled may allow an attacker to gain access through the Werkzeug debugger.

## Recommendation: 
Ensure that Flask applications that are run in a production environment have debugging disabled.


# Scanner Comparison

## Only CodeQL (SAST) Found
- Code patterns and logic errors
- Data flow vulnerabilities

## Only ZAP (DAST) Found
- Missing security headers
- Runtime configuration issues
- API endpoint vulnerabilities

## Only Dependency-Check (SCA) Found
- Outdated package versions
