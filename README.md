
# CST8919 – DevOps Security and Compliance  
## Cloud Service Comparisons – Azure vs AWS vs GCP  

---

##  Report Objective

This document presents a comparison of 10 Azure services and their nearest equivalent offerings in Amazon Web Services (AWS) and Google Cloud Platform (GCP).
For every service covered, the report outlines:

Overview – a concise description of the service’s purpose

Core Features – key capabilities and functionality

Security & Compliance – relevant protections, certifications, and governance

Pricing Model – a high-level summary of cost structure

Integration for DevSecOps – how the service fits into automation, CI/CD, and monitoring workflows
---

##  Selected Services Mapping  

| #  | Azure Service                  | AWS Equivalent(s)                              | GCP Equivalent(s)                            |
|----|---------------------------------|------------------------------------------------|----------------------------------------------|
| 1  | Microsoft Entra ID (Azure AD)   | IAM + IAM Identity Center                      | Cloud Identity + Cloud IAM                   |
| 2  | Azure Log Analytics             | CloudWatch Logs + Logs Insights                | Cloud Logging (+ BigQuery)                   |
| 3  | Azure Landing Zone              | Control Tower                                  | Landing Zone Blueprints / Toolkit            |
| 4  | Microsoft Defender for Cloud    | Security Hub + GuardDuty + Inspector           | Security Command Center                       |
| 5  | Microsoft Sentinel              | Security Hub + Detective (partial)             | Chronicle Security Operations                 |
| 6  | Azure Functions                 | AWS Lambda                                     | Cloud Functions                               |
| 7  | Azure Storage (Blob)            | S3                                             | Cloud Storage                                 |
| 8  | Azure Key Vault                 | Secrets Manager + KMS                          | Secret Manager + Cloud KMS                    |
| 9  | Azure Firewall                  | AWS Network Firewall                           | Cloud Firewall                                |
| 10 | Azure DevOps                    | CodePipeline / CodeBuild / CodeCommit / Deploy | Cloud Build + Artifact Registry + Cloud Deploy |

---

## Service 1 – Microsoft Entra ID vs AWS IAM + Identity Center vs GCP Cloud Identity + IAM  

**Overview**  
Microsoft Entra ID (Azure AD) is a cloud-based identity platform offering SSO, MFA, and conditional access for secure resource access. AWS pairs IAM for permission control with Identity Center for SSO. GCP uses Cloud Identity for directory services alongside Cloud IAM for resource-level access control.  

**Core Features**  
- Azure: SAML/OIDC federation, privileged identity management, SCIM provisioning.  
- AWS: Policies, permission sets, Access Analyzer for permissions review.  
- GCP: Context-aware access, workload identity federation, custom/predefined roles.  

**Security & Compliance**  
- Enterprise certifications (ISO, SOC, FedRAMP) and advanced authentication methods (MFA, passwordless).  

**Pricing Model**  
- Azure: Free, P1, and P2 tiers. AWS/GCP: IAM free; advanced directory features billed separately.  

**Integration for DevSecOps**  
- All support OIDC integration for CI/CD pipelines to enable temporary, scoped credentials.  

---

## Service 2 – Azure Log Analytics vs AWS CloudWatch Logs/Insights vs GCP Cloud Logging (+ BigQuery)  

**Overview**  
A platform for collecting, querying, and analyzing log data from applications and infrastructure.  

**Core Features**  
- Azure: Uses KQL, offers scheduled alerts, integration with Monitor.  
- AWS: Logs Insights for queries, metric generation, integration with alarms.  
- GCP: Logs Explorer, export to BigQuery for large-scale analysis.  

**Security & Compliance**  
- IAM/RBAC restrictions, encryption at rest and in transit, retention policies.  

**Pricing Model**  
- Pay per GB ingested and stored; query charges apply based on data scanned.  

**Integration for DevSecOps**  
- Integrates with SIEM platforms, triggers incident automation, and monitors deployments.  

---

## Service 3 – Azure Landing Zone vs AWS Control Tower vs GCP Landing Zone Blueprints  

**Overview**  
Predefined deployment patterns and configurations for establishing a secure, governed cloud environment.  

**Core Features**  
- Azure: Sets identity, networking, security, and governance baselines.  
- AWS: Multi-account setup, central logging, security guardrails.  
- GCP: Prebuilt project structures, org policies, and network templates.  

**Security & Compliance**  
- Aligned with CIS/NIST frameworks; enables audit-ready environments.  

**Pricing Model**  
- No direct charge; cost comes from deployed baseline resources.  

**Integration for DevSecOps**  
- Bootstraps IaC repositories, policy-as-code, and automated environment provisioning.  

---

## Service 4 – Microsoft Defender for Cloud vs AWS Security Hub + GuardDuty + Inspector vs GCP Security Command Center  

**Overview**  
A unified platform for cloud security posture management and threat protection.  

**Core Features**  
- Azure: Posture recommendations, workload protection, DevOps scanning.  
- AWS: Security Hub (aggregation), GuardDuty (threat detection), Inspector (vulnerability scanning).  
- GCP: SCC for posture, findings, and threat intelligence.  

**Security & Compliance**  
- Compliance mapping to CIS/NIST/PCI; integrates with IAM, logging, and policy services.  

**Pricing Model**  
- Free CSPM tier; paid tiers for advanced protection features.  

**Integration for DevSecOps**  
- Feeds findings to SIEMs, runs IaC scans in pipelines, supports automated remediation.  

---

## Service 5 – Microsoft Sentinel vs AWS Security Hub + Detective vs GCP Chronicle Security Operations  

**Overview**  
Cloud-native SIEM and SOAR platform for security monitoring and automation.  

**Core Features**  
- Azure: KQL analytics, UEBA, playbooks with Logic Apps.  
- AWS: Security Hub + Detective for investigation workflows.  
- GCP: Chronicle provides integrated SIEM and SOAR capabilities.  

**Security & Compliance**  
- Meets enterprise compliance needs; supports CMEK and regional storage.  

**Pricing Model**  
- Pay-per-GB ingested; retention costs apply.  

**Integration for DevSecOps**  
- Supports automated incident response, integrates with ticketing, and enables proactive detection testing.  

---

## Service 6 – Azure Functions vs AWS Lambda vs GCP Cloud Functions  

**Overview**  
Serverless compute environments that execute code in response to events.  

**Core Features**  
- Azure: Rich bindings, triggers for multiple services.  
- AWS: Triggers from API Gateway, S3, DynamoDB, and more.  
- GCP: HTTP, Pub/Sub, and Cloud Storage triggers.  

**Security & Compliance**  
- Role-based access, VNET/VPC integration, secrets management.  

**Pricing Model**  
- Pay per request and execution time; free monthly tiers offered.  

**Integration for DevSecOps**  
- Works in CI/CD pipelines for automated deployment and testing.  

---

## Service 7 – Azure Storage (Blob) vs AWS S3 vs GCP Cloud Storage  

**Overview**  
Object storage for unstructured data and static content.  

**Core Features**  
- Tiered storage, versioning, lifecycle policies, event notifications.  

**Security & Compliance**  
- Encryption at rest, private networking, IAM-based access.  

**Pricing Model**  
- Charged per GB stored, requests, and egress traffic.  

**Integration for DevSecOps**  
- Used for storing artifacts, logs, and triggering automated processes.  

---

## Service 8 – Azure Key Vault vs AWS Secrets Manager + KMS vs GCP Secret Manager + Cloud KMS  

**Overview**  
Secure storage for secrets, encryption keys, and certificates.  

**Core Features**  
- Versioning, rotation, HSM-backed key management, API access.  

**Security & Compliance**  
- FIPS-compliant encryption, RBAC/IAM policies, private endpoints.  

**Pricing Model**  
- Per-operation costs for secrets and keys; storage fees for versions.  

**Integration for DevSecOps**  
- Injects secrets into pipelines, encrypts artifacts, manages signing keys.  

---

## Service 9 – Azure Firewall vs AWS Network Firewall vs GCP Cloud Firewall  

**Overview**  
Managed firewall services for controlling traffic at the network and application layers.  

**Core Features**  
- Stateful/stateless filtering, application rules, threat intelligence integration.  

**Security & Compliance**  
- Logs to SIEM, compliance with enterprise network security standards.  

**Pricing Model**  
- Gateway cost plus data processing fees; extra for advanced security features.  

**Integration for DevSecOps**  
- Firewall rules deployed as code, integrated into change management pipelines.  

---

## Service 10 – Azure DevOps vs AWS CodePipeline/Build/Commit/Deploy vs GCP Cloud Build + Artifact Registry + Cloud Deploy  

**Overview**  
Integrated development and delivery platforms with CI/CD capabilities.  

**Core Features**  
- Azure: Boards, Repos, Pipelines, Artifacts.  
- AWS: CodeCommit, CodeBuild, CodeDeploy, CodePipeline.  
- GCP: Cloud Build, Artifact Registry, Cloud Deploy.  

**Security & Compliance**  
- Role-based access, SSO, compliance certifications.  

**Pricing Model**  
- Free tiers for basic use; billed for users, storage, and build minutes.  

**Integration for DevSecOps**  
- Integrates code scanning, policy enforcement, and deployment approvals into pipelines.  

---
