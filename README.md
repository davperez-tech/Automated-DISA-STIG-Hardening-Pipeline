# Automated DISA STIG Hardening Pipeline

## At a Glance
| Compliance Improvement   | Progress                                  |
|:-------------:           |:--------------:                           |
| Baseline Report          | ![Progress](https://progress-bar.xyz/48/) |
| Post-Hardening Report    | ![Progress](https://progress-bar.xyz/96/) |

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
<img width="734" height="180" alt="Workflow" src="https://github.com/user-attachments/assets/f71f0304-4fa5-405d-878e-993236dcb462" />
</p>

## Security Hardening
| Authentication & Access Control                               | Audit & Logging                                  | System Protection                                |
| :-------------                                                |:--------------                                   |:--------------                                   |
| 15+ character passwords with complexity requirements          | auditd enabled with privileged command tracking  | SELinux enforcing mode                           |
| 24-password history enforcement                               | Immutable audit logs                             | Firewalld with minimal allowed services          |
| Account lockout after 3 failed attempts                       | File integrity monitoring (AIDE)                 | Kernel hardening (ASLR, NX bit, exec-shield)     |
| SSH hardening (key-only auth, no root login, idle timeout)    | Centralized syslog configuration                 | Unnecessary services disabled                    |

## Automation Capabilities

- **Idempotent** - Safe to run multiple times

- **Scalable** - Add hundreds of hosts to inventory

- **Auditable** - XML/HTML evidence packages

- **Documented** - Auto-generates exception reports

## Reporting

- HTML reports with visual compliance dashboards

- XML results for SIEM integration

- Before/after comparison metrics

- CAT I/II/III severity categorization

## Results & Analysis Compliance Improvement
| Metric                    | Baseline                                  | Post-Hardening                             | Change          |
| :-------------            | :--------------:                          | :--------------:                           |:--------------: |                        
| **Overall Compliance**    | ![Progress](https://progress-bar.xyz/48/) | ![Progress](https://progress-bar.xyz/96/)  | +47.48% ✅      |
| Rules Passed              | 174                                       | 420                                        | +246            |
| Rules Failed              | 262                                       | 18                                         | -244            |
| Total Rules               | 727                                       | 727                                        | -               |

