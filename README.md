# Automated DISA STIG Hardening Pipeline

## At a Glance
| Compliance Improvement   | Progress                                  |
|:-------------:           |:--------------:                           |
| Baseline Report          | ![Progress](https://progress-bar.xyz/48/) |
| Post-Remediation Report  | ![Progress](https://progress-bar.xyz/96/) |

**Security Posture**

- ✅ CAT I: 12 → 5 (58% resolved)

- ✅ CAT II: 228 → 8 (96% resolved)

- ✅ CAT III: 19 → 5 (74% resolved)

## Overview
This project demonstrates automated security compliance for Department of Defense (DoD) and federal IT systems. It takes a fresh RHEL 9 installation from 48.64% DISA STIG compliance to 96.12% compliance in under 30 minutes using:

- OpenSCAP for security scanning against official DISA STIGs

- Ansible for automated remediation
  
- Infrastructure as Code principles for repeatability

**The Problem ❌**

Manual STIG implementation on Linux systems:
- Takes 40+ hours per server
  
- Prone to human error

- Requires extensive documentation

- Difficult to maintain consistency across fleets

**The Solution ✅**

An automated pipeline that:

1. Scans the system against 727 DISA STIG controls
2. Generates Ansible remediation playbooks automatically
3. Applies hardening configurations idempotently
4. Validates compliance with post-remediation scans
5. Documents exceptions with risk assessments

## Architecture
<p align="center">
<img width="394" height="515" alt="Architecture" src="https://github.com/user-attachments/assets/b9d87ace-c8af-407f-baaf-382d2eae2f15" />
</p>

## Workflow
<p align="center">
<img width="734" height="270" alt="Workflow" src="https://github.com/user-attachments/assets/6c8d4fbe-2505-49ce-a254-a1d847836419" />
</p>
