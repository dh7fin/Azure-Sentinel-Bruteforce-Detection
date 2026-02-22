# Azure Sentinel Brute-Force Detection Lab

## Overview

This project demonstrates the implementation of a cloud-native SIEM solution in Microsoft Azure using Microsoft Sentinel to detect brute-force RDP authentication attempts against a Windows virtual machine.

The lab simulates repeated failed logon attempts (Event ID 4625) and validates end-to-end detection from log ingestion to automated incident generation and investigation.

---

## Threat Context

Brute-force attacks are a common credential access technique targeting internet-exposed services such as RDP. In cloud environments, exposed virtual machines without proper monitoring can be vulnerable to password spraying and automated authentication attacks.

This project focuses on detecting abnormal authentication behaviour using Windows Security Events and transforming that telemetry into actionable security incidents within Microsoft Sentinel.

---

## MITRE ATT&CK Mapping

- **Tactic:** Credential Access  
- **Technique:** Brute Force (T1110)  
- **Sub-technique:** Password Guessing (T1110.001)

---

## Cloud Security Detection Architecture

![Architecture Diagram](architecture-diagram.png)

📄 High-Resolution Architecture Diagram (PDF):  
[Download Architecture Diagram (PDF)](architecture-diagram.pdf)

---

## Detection Logic

The scheduled analytics rule monitors Windows Security Event ID 4625 (failed logon attempts). The detection triggers when multiple failed authentication attempts occur within a defined time window, indicating behaviour consistent with brute-force activity.

When the configured threshold is exceeded, Microsoft Sentinel automatically generates a security incident for investigation.

---

## Key Skills Demonstrated

- Azure infrastructure deployment  
- Log Analytics Workspace configuration  
- Azure Monitor Agent implementation  
- Windows Security Event ingestion  
- KQL query development  
- Detection engineering  
- Incident investigation within Microsoft Sentinel  
- Cloud security monitoring architecture  

---

## Full Technical Report

📄 [Download Full Project Report (PDF)](Microsoft Azure Sentinel Brute-Force Detection Lab Project.pdf)

---

## Conclusion

This project successfully validated a cloud-native detection pipeline capable of identifying brute-force authentication behaviour within an Azure-hosted environment. By operationalizing Windows Security telemetry into automated incident generation, the lab demonstrates practical detection engineering and cloud security monitoring capabilities aligned with modern SOC workflows.
