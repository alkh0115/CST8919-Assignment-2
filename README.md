# Cloud Service Alternatives Report
*CST8919 – DevOps Security & Compliance – Assignment 2*

- *Student Name:* Rahaf Alkhlaf
- *Student Username:* alkh0115

## Introduction
This report compares key Microsoft Azure security, compliance, and monitoring services studied in the CST8919 course with their closest equivalents in Amazon Web Services (AWS) and Google Cloud Platform (GCP). For each service, an overview table presents the corresponding offerings across the three cloud providers, followed by a comparison of core features, security and compliance capabilities, pricing models, and DevSecOps integration considerations.

## Azure Services vs AWS & GCP Equivalents

---

### 1. Azure Active Directory (SSO, IAM)

| Cloud | Service Name | Overview |
|-------|--------------|----------|
| Azure | Azure Active Directory (Microsoft Entra ID) | Cloud-based identity and access management supporting SSO, MFA, RBAC, and federation across apps and services. |
| AWS   | AWS Identity and Access Management (IAM), IAM Identity Center, Amazon Cognito | Centralized IAM with policy-based access control, SSO for workforce users, and customer identity management with app integration. |
| GCP   | Cloud IAM, Cloud Identity, Identity Platform | Unified identity and access management, SSO, MFA, and policy enforcement for Google Cloud resources and third-party apps. |

**Core Features**  
- Azure: Centralized user management, SSO, MFA, conditional access, application integration.  
- AWS: Role and policy-based access control, temporary credentials, SSO with AWS and SaaS apps, identity federation.  
- GCP: Resource-level IAM, SSO, MFA, conditional access, identity federation.  

**Security & Compliance**  
- All three provide audit logging, compliance with ISO 27001, SOC 2, FedRAMP, GDPR, HIPAA, and support for least privilege.  

**Pricing Model**  
- Azure: Free, Premium P1, and Premium P2 tiers.  
- AWS: IAM is free; charges apply for AWS SSO and Cognito MAUs.  
- GCP: IAM is free; Cloud Identity has free and premium tiers; Identity Platform is pay-per-use.  

**Integration for DevSecOps**  
- All integrate with CI/CD pipelines to control access to repositories, deployments, and cloud resources.

---

### 2. Azure Monitor & Log Analytics

| Cloud | Service Name | Overview |
|-------|--------------|----------|
| Azure | Azure Monitor & Log Analytics | End-to-end observability platform collecting metrics, logs, and traces from Azure and hybrid environments with KQL analytics. |
| AWS   | Amazon CloudWatch | Centralized metrics, logs, and event monitoring for AWS resources and on-premises environments. |
| GCP   | Cloud Monitoring & Cloud Logging | Integrated observability suite for metrics, logs, events, and traces across GCP and hybrid environments. |

**Core Features**  
- Azure: Metrics, logs, alerts, dashboards, KQL querying, integration with Sentinel and Logic Apps.  
- AWS: Metrics, log streams, custom dashboards, alarms, CloudWatch Logs Insights querying.  
- GCP: Metrics explorer, logs querying with Log Explorer, alerting policies, SLO monitoring.  

**Security & Compliance**  
- All support encryption in transit/at rest, RBAC for data access, and compliance with SOC, ISO, HIPAA, GDPR.  

**Pricing Model**  
- Azure: Pay-per-ingested GB and data retention.  
- AWS: Pay-per-metrics, logs ingestion, and retention.  
- GCP: Free quotas; pay for ingestion/storage above quota.  

**Integration for DevSecOps**  
- All integrate with automation workflows for alert-based remediation and pipeline monitoring.

---

### 3. Azure Policy

| Cloud | Service Name | Overview |
|-------|--------------|----------|
| Azure | Azure Policy | Governance service to create, assign, and enforce rules on Azure resources for compliance and configuration control. |
| AWS   | AWS Config, Service Control Policies (SCPs) | Monitors configurations, enforces rules, and applies account-level guardrails across AWS Organizations. |
| GCP   | Organization Policy Service, Policy Controller | Manages constraints and policy enforcement across Google Cloud resources, with Kubernetes policy support. |

**Core Features**  
- Azure: Built-in/custom policies, initiatives, deny/audit/append effects, auto-remediation.  
- AWS: Config rules, SCPs for organization-wide restrictions, remediation actions.  
- GCP: Constraints, org-level policy enforcement, policy as code for GKE.  

**Security & Compliance**  
- All enforce regulatory compliance, restrict insecure configurations, and log policy violations.  

**Pricing Model**  
- Azure: Policy evaluation free; remediation costs depend on actions.  
- AWS: AWS Config is pay-per-resource tracked; SCPs are free.  
- GCP: Included at no additional cost.  

**Integration for DevSecOps**  
- All support policy-as-code for continuous compliance in infrastructure provisioning.

---

### 4. Defender for Cloud

| Cloud | Service Name | Overview |
|-------|--------------|----------|
| Azure | Microsoft Defender for Cloud | Cloud-Native Application Protection Platform (CNAPP) with DevSecOps, CSPM, and CWPP capabilities across Azure, AWS, and GCP. |
| AWS   | AWS Security Hub, Amazon GuardDuty, Amazon Inspector | Aggregated security findings, threat detection, and workload scanning for vulnerabilities and misconfigurations. |
| GCP   | Security Command Center | Unified security and risk management platform with asset discovery, threat detection, and compliance reporting. |

**Core Features**  
- Azure: Code scanning, security posture assessment, workload protection, automated remediation.  
- AWS: Findings aggregation, anomaly detection, container/image scanning.  
- GCP: Asset inventory, threat detection, misconfiguration analysis.  

**Security & Compliance**  
- All provide mappings to compliance frameworks, encryption, and alerting for high-risk issues.  

**Pricing Model**  
- Azure: Tiered by resource type and protection plan.  
- AWS: Pay-per-service (Security Hub per finding, GuardDuty per event, Inspector per scan).  
- GCP: Free tier for basic features; premium tier for advanced detection.  

**Integration for DevSecOps**  
- All integrate with CI/CD pipelines, IaC scanning, and SIEM/SOAR tools.

---

### 5. Azure Sentinel (SIEM/SOAR)

| Cloud | Service Name | Overview |
|-------|--------------|----------|
| Azure | Microsoft Sentinel | Cloud-native SIEM/SOAR for threat detection, investigation, and automated response using KQL analytics. |
| AWS   | Amazon Security Lake, Amazon Detective, OpenSearch Security Analytics | Centralized security data lake with investigation and analysis tools. |
| GCP   | Google Security Operations (Chronicle SIEM & SOAR) | Cloud-native SIEM/SOAR for threat detection, incident investigation, and automated playbooks. |

**Core Features**  
- Azure: Data connectors, hunting queries, incident management, automation via playbooks.  
- AWS: Security data aggregation, investigative queries, visualization dashboards.  
- GCP: Real-time analytics, incident management, threat intelligence feeds.  

**Security & Compliance**  
- All support secure log storage, encryption, RBAC, and compliance mappings.  

**Pricing Model**  
- Azure: Pay-per-GB ingested or capacity reservations.  
- AWS: Pay for data storage, queries, and processing.  
- GCP: Tiered pricing based on ingestion and analysis usage.  

**Integration for DevSecOps**  
- All integrate with monitoring tools, workflow automation, and security incident response processes.

---
## References

Amazon Web Services. (n.d.). *What is IAM?*. Retrieved from https://docs.aws.amazon.com/IAM/latest/UserGuide/introduction.html  
Amazon Web Services. (n.d.). *What is Amazon Detective?*. Retrieved from https://docs.aws.amazon.com/detective/latest/userguide/what-is-detective.html  
Amazon Web Services. (2025, July 30). *What Is AWS Config?*. Retrieved from https://docs.aws.amazon.com/config/latest/developerguide/WhatIsConfig.html  
Amazon Web Services. (2025, August 2). *What is AWS Security Hub CSPM?*. Retrieved from https://docs.aws.amazon.com/securityhub/latest/userguide/what-is-securityhub.html  
Amazon Web Services. (2025, August 8). *What is Amazon CloudWatch?*. Retrieved from https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/WhatIsCloudWatch.html  
Google Cloud. (2025, August 7). *Cloud Monitoring overview*. Retrieved from https://cloud.google.com/monitoring/docs/monitoring-overview  
Google Cloud. (2025, August 7). *Google SecOps overview*. Retrieved from https://cloud.google.com/chronicle/docs/secops/secops-overview  
Google Cloud. (2025, August 7). *IAM overview*. Retrieved from https://cloud.google.com/iam/docs/overview  
Google Cloud. (2025, August 7). *Introduction to the Organization Policy Service*. Retrieved from https://cloud.google.com/resource-manager/docs/organization-policy/overview  
Microsoft. (2025, March 4). *What is Azure Policy?*. Retrieved from https://learn.microsoft.com/en-us/azure/governance/policy/overview  
Microsoft. (2025, May 23). *Azure Monitor overview*. Retrieved from https://learn.microsoft.com/en-us/azure/azure-monitor/fundamentals/overview  
Microsoft. (2025, June 20). *What is Microsoft Entra ID?*. Retrieved from https://learn.microsoft.com/en-us/entra/fundamentals/whatis  
Microsoft. (2025, July 22). *What is Microsoft Sentinel?*. Retrieved from https://learn.microsoft.com/en-us/azure/sentinel/overview?tabs=defender-portal  
Microsoft. (2025, July 23). *What is Microsoft Defender for Cloud?*. Retrieved from https://learn.microsoft.com/en-us/azure/defender-for-cloud/defender-for-cloud-introduction  


