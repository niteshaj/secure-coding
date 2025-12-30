# **SIEM (Security Information and Event Management)**

SIEM is a security solution that **collects, normalizes, correlates, and analyzes logs/events** from across an organization’s IT environment to **detect threats, investigate incidents, and meet compliance requirements**.

### Core Functions

1. **Log Collection & Normalization**

   * Ingests logs from servers, applications, databases, firewalls, IAM, cloud services, etc.
2. **Correlation & Detection**

   * Applies rules, signatures, and analytics to identify suspicious patterns (e.g., brute force, lateral movement).
3. **Alerting & Incident Response**

   * Generates alerts and supports investigations with timelines and context.
4. **Compliance & Reporting**

   * Prebuilt reports for standards like ISO 27001, PCI-DSS, SOX, HIPAA.

## SIEM architecture (logical view)

```
[ Systems / Apps / Cloud / Network devices/ IAM (AD, Entra ID, Keycloak) ]
          ↓
     Log Collectors
          ↓
     Normalization
          ↓
   Correlation Engine
          ↓
   Alerts & Dashboards
          ↓
   SOC / Incident Response
```

### Typical Data Sources

* OS & application logs
* Network devices (firewalls, IDS/IPS)
* IAM (AD, Entra ID, Keycloak)
* Cloud logs (AWS CloudTrail, Azure Activity Logs)

### Benefits

* Centralized visibility
* Faster threat detection & response
* Audit & compliance readiness
* Forensics and root-cause analysis

### Common SIEM Tools

* **Splunk Enterprise Security**
* **IBM QRadar**
* **Microsoft Sentinel**
* **Elastic SIEM**
* **ArcSight**

## SIEM vs related tools (important distinction)

| Tool        | Purpose                 |
| ----------- | ----------------------- |
| **SIEM**    | Detect & investigate    |
| **SOAR**    | Automate response       |
| **EDR**     | Endpoint behavior       |
| **IDS/IPS** | Network detection       |
| **UEBA**    | User behavior analytics |

📌 Modern SIEMs often **embed UEBA** and **integrate with SOAR**.

## SIEM from an Architect perspective (key expectations)

As an Architect, you should:

* Identify **what logs are security-relevant**
* Ensure **logs are structured and trustworthy**
* Design **secure log pipelines**
* Avoid logging sensitive data (PII, secrets)
* Ensure **immutability & retention**
* Align detection with **threat models**

---

## Secure Coding + SIEM (very important)

Your applications should:

* Log authentication & authorization events
* Log failures, not just success
* Include **correlation IDs**
* Avoid logging secrets
* Use consistent log formats (JSON preferred)

📌 Good logs = effective SIEM

---
