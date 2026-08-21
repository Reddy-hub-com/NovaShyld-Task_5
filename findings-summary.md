# Task 5 — Findings Summary

## Confirmed Finding

### vsFTPd 2.3.4 Backdoor

| Attribute | Value |
|---|---|
| Vulnerability | vsFTPd 2.3.4 Backdoor |
| CVE | CVE-2011-2523 |
| Severity | Critical |
| CVSS v3.1 | 9.8 |
| Target | 192.168.195.133 |
| Validation | Metasploit |
| Result | Meterpreter session established |
| Privilege | Root |

## Security Impact

Successful validation demonstrated that the vulnerable service could provide unauthorized remote access to the target and result in root-level privileges.

## Evidence

The assessment evidence is maintained in:

```text
02-Screenshots/
03-Scan-Results/
```

The final report contains the detailed technical analysis and evidence mapping.

## Assessment Limitation

Testing was performed against the authorized, intentionally vulnerable Metasploitable2 laboratory target.
