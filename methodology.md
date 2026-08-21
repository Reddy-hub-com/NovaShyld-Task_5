# Task 5 — VAPT Methodology

## 1. Purpose

This document summarizes the methodology used for the NovaShyld Task 5 Advanced VAPT Assessment.

## 2. Assessment Workflow

The assessment followed the documented sequence:

1. Connectivity Verification
2. Reconnaissance and Enumeration
3. Vulnerability Assessment
4. Controlled Exploitation
5. Post-Exploitation Verification
6. Risk Assessment
7. Remediation Planning
8. Final Reporting

## 3. Connectivity Verification

Connectivity to the authorized Metasploitable2 target was verified from Kali Linux using ICMP ping.

Target:
`192.168.195.133`

## 4. Reconnaissance and Enumeration

Nmap was used to identify open ports, services, service versions, and other available information about the target.

Primary scan:

```bash
nmap -A 192.168.195.133 -oN task5_nmap_scan.txt
```

## 5. Vulnerability Assessment

Nmap vulnerability scripts were used to identify potential known vulnerabilities:

```bash
nmap --script vuln 192.168.195.133 -oN task5_vuln_scan.txt
```

The assessment identified the vsFTPd 2.3.4 backdoor vulnerability.

## 6. Controlled Exploitation

The identified vsFTPd 2.3.4 vulnerability was validated using Metasploit against the authorized laboratory target.

The objective was to demonstrate exploitability and security impact without performing destructive activity.

## 7. Post-Exploitation Verification

After successful exploitation, the established Meterpreter session was used for controlled validation including:

- `getuid`
- `sysinfo`
- `pwd`
- `ls`
- `sessions`

The `getuid` result confirmed root-level access.

## 8. Risk Assessment

The confirmed finding was assessed using CVSS v3.1 as documented in the final VAPT report.

## 9. Reporting

Technical findings, evidence, impact, severity, remediation recommendations, and supporting screenshots were documented in the final Task 5 report.
