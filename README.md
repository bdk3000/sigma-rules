# SIGMA Detection Rules

Vendor-neutral detection rules in SIGMA format, developed and validated 
against live lab telemetry in an isolated HyperV environment.

Cross-platform translations provided for KQL (Microsoft Sentinel), 
SPL (Splunk), and EQL (Elastic) inline within each rule file.

## Rules

| Rule | Technique | MITRE | Severity |
|------|-----------|-------|----------|
| [NTLM Enumeration Burst](rules/windows/sigma_ntlm_enumeration_burst.yml) | Unauthenticated AD Reconnaissance | T1046, T1078 | High |

## Validation Environment
- Windows Server 2022 DC with Sysmon + Azure Monitor Agent
- Telemetry pipeline → Microsoft Sentinel
- Attacker tooling: enum4linux-ng, netexec (Kali Linux)
