# Infotact-Internship-Project
2-Month Internship at Infotact 

----------1st----------------- 



Problem Statement 
Simulate a real-world vulnerability assessment for a small business IT infrastructure. Identify 
security gaps, prioritize risks, and provide mitigation strategies to improve the overall security posture. 



Vulnerability Assessment Report 


 
1. Introduction 
This report summarizes the key vulnerabilities discovered during the security assessment of the target 
web environment. It categorizes vulnerabilities by severity and provides an overview of preventive 
measures necessary to reduce risk exposure. 



 
2. Identified Vulnerabilities and Severity 
Vulnerability Set 1 
• Unauthenticated Directory Access – High severity: Sensitive directories are accessible 
without authentication, increasing the risk of unauthorized access and data exposure. 
• WebDAV Unicode Bypass (ms09_020) – Medium to High severity: This vulnerability could 
allow attackers to bypass WebDAV restrictions using Unicode encoding. 
• SQL Injection (blind/error-based) – Medium to High severity: Potential for database 
compromise exists, although not conclusively confirmed. 
• CMS PHP Code Execution – High severity: Risks of arbitrary code execution on the CMS 
platform were detected but not successfully exploited.



Vulnerability Set 2 
• Directory Listing / Unrestricted Directory Access – High severity: Directory contents are 
exposed, allowing attackers to enumerate files and directories easily. 
• Exposed phpMyAdmin Interface – High severity: phpMyAdmin is accessible without 
proper restrictions, increasing the risk of database attacks. 
• Backup and Sensitive Files Exposure – Medium to High severity: Backup files and 
configuration files with sensitive information are present in publicly accessible locations. 


Vulnerability Set 3 
• Web Server TRACE Method Enabled – High severity: TRACE method can be exploited in 
Cross-Site Tracing (XST) attacks to steal sensitive data. 
• Outdated Server Version – Critical severity: The server is running outdated software with 
known vulnerabilities, posing significant risk. 
• Unprotected /dav/ and /doc/ Paths – Medium severity: These directories lack adequate 
access controls, potentially exposing sensitive data. 


Vulnerability Set 4 
• HTTP TRACE Enabled – High severity: Enabled TRACE method introduces risks of 
sensitive information disclosure. 
• Unsecured WebDAV Access – High severity: WebDAV access is not properly secured, 
allowing unauthorized operations. 
• Outdated Web Server Stack – Critical severity: The server software and components are 
outdated, increasing exposure to known exploits. 
• No SSL/TLS Encryption – Medium severity: Lack of encryption exposes data to 
interception and manipulation during transmission. 
                                                                                
 
3. Prevention Overview 
The vulnerabilities identified highlight the need for comprehensive security hygiene, including: 
• Restricting access to sensitive directories and administrative interfaces to prevent 
unauthorized entry. 
• Disabling unnecessary services like WebDAV and TRACE to reduce attack surface. 
• Keeping all server components, CMS, and related software up to date with security patches. 
• Enforcing encrypted communication channels through SSL/TLS to protect data in transit. 
• Limiting exposure of backup and configuration files by proper file management and 
permissions. 
 
4. Summary 
The assessment reveals several high and critical severity vulnerabilities that could allow attackers to 
compromise sensitive data, execute arbitrary code, or gain unauthorized access. The presence of 
outdated software and insecure configurations further increases risk. 
Immediate attention is required to secure directory access, disable insecure HTTP methods, and 
ensure encryption is properly implemented. Maintaining up-to-date software and restricting 
unnecessary services will significantly improve the security posture and resilience against common 
web-based attacks. 

---------2nd Month ----------

Problem Statement 
The objective of this project is to conduct a comprehensive penetration test on a sample 
vulnerable web application (such as DVWA or OWASP Juice Shop), identifying and 
exploiting vulnerabilities listed in the OWASP Top 10. The ultimate goal is to document the 
vulnerabilities, demonstrate exploitation, and provide actionable recommendations for 
remediation.

 Final Penetration Testing Report 
The final report was structured to meet professional standards and industry practices. 
Report Sections: 
 Executive Summary: 
• Brief overview of the engagement. 
• Objectives of the test. 
• Summary of vulnerabilities found and risk ratings. 
 Scope: 
• Target applications: DVWA and OWASP Juice Shop 
• Local testing environment. 
• OWASP Top 10 vulnerabilities as the core focus. 


 Methodology: 
• Manual and automated testing. 
• Tools used: 
o Burp Suite for interception and manipulation 
o sqlmap for automated SQL injection 
o Browser DevTools for source code inspection and XSS 
o dirb/gobuster for directory brute-forcing 
o Postman for testing API endpoints 


Vulnerability Findings: 
Each vulnerability included: 
• Title 
• Description 
• Proof-of-Concept (PoC) with screenshots 
• Impact 
• Affected components 
• CVSS rating 
• Mitigation/Recommendation 


Examples: 
Vulnerability Description CVSS 
Score Status 
SQL Injection : Input fields vulnerable to unsanitized SQL queries | 9.1 (Critical)| Confirmed 
Stored XSS: Payload stored in database and executed on load |8.8 (High)| Confirmed 
Security Misconfig :mUnrestricted access to admin dashboard| 8.2 (High) |confirmed 


Risk Ratings: 
Each vulnerability was rated based on: 
• Exploitability 
• Impact 
• Likelihood 
• Business risk 

Recommendations: 
Clear, actionable mitigation steps for each issue: 
• Use input validation & output encoding 
• Implement proper session management 
• Configure web server securely 
• Avoid using default or guessable endpoints 
• Enable HTTPS and set security headers
