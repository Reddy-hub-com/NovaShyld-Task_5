# Task 5 — Retesting Procedure

## Purpose

Retesting verifies whether the remediation actions have successfully removed the confirmed vulnerability.

## Retesting Steps

### 1. Confirm Service State

Verify whether the vulnerable FTP service is still enabled and accessible.

### 2. Perform Nmap Enumeration

Run the documented Nmap service/version scan against the authorized target.

```bash
nmap -A 192.168.195.133 -oN retest_nmap_scan.txt
```

### 3. Perform Vulnerability Validation

Run the vulnerability assessment again:

```bash
nmap --script vuln 192.168.195.133 -oN retest_vuln_scan.txt
```

### 4. Verify vsFTPd Version

Confirm that the vulnerable vsFTPd 2.3.4 installation is no longer present.

### 5. Validate Exploitability

If authorized and required by the engagement, verify that the previously demonstrated exploitation path is no longer successful.

### 6. Document Results

Record:

- Retest date
- Target
- Service state
- Vulnerability status
- Scan output
- Validation result
- Remaining risks

## Expected Result

The expected secure result is that the vulnerable vsFTPd 2.3.4 condition is removed and the previously demonstrated exploitation path is no longer available.

## Final Status

Retesting should be marked:

- **Remediated** — vulnerability no longer detected.
- **Partially Remediated** — risk reduced but vulnerability or exposure remains.
- **Not Remediated** — vulnerable condition remains.
