# Task 5 — Remediation Plan

## Primary Finding

**vsFTPd 2.3.4 Backdoor — CVE-2011-2523**

## Recommended Remediation

1. Remove the vulnerable vsFTPd 2.3.4 installation.
2. Upgrade to a supported and secure version where the service is required.
3. Disable unnecessary FTP services.
4. Restrict network exposure using appropriate firewall rules.
5. Apply network segmentation to limit access to sensitive services.
6. Monitor exposed services and authentication activity.
7. Perform periodic vulnerability scanning.
8. Conduct a security retest after remediation.

## Priority

Because the confirmed vulnerability was rated Critical with a CVSS v3.1 score of 9.8, remediation should receive the highest priority within the laboratory risk assessment.

## Verification

After remediation, the service should be rescanned and the affected vulnerability should be revalidated to confirm that the vulnerable condition is no longer present.
