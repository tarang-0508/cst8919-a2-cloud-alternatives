# CST8919 – DevOps Security and Compliance  
## Assignment 2 – Cloud Service Alternatives Report  



---

##  Objective  
This report compares Microsoft Azure services studied in this course with their closest equivalents in **Amazon Web Services (AWS)** and **Google Cloud Platform (GCP)**. The goal is to understand service similarities, differences, and suitability for **security, compliance, and DevSecOps** practices.

---

##  Quick Comparison Table  

| #  | Azure Service                              | AWS Equivalent(s)                                     | GCP Equivalent(s)                                   |
|----|--------------------------------------------|-------------------------------------------------------|-----------------------------------------------------|
| 1  | Azure Active Directory (Microsoft Entra ID)| AWS IAM + IAM Identity Center (formerly SSO)          | Google Cloud Identity + Cloud IAM                   |
| 2  | Azure Monitor                              | Amazon CloudWatch                                     | Google Cloud Monitoring                             |
| 3  | Azure Log Analytics                        | CloudWatch Logs + CloudWatch Logs Insights            | Cloud Logging + BigQuery                            |
| 4  | Azure Policy                               | AWS Config + Service Control Policies (SCPs)          | Organization Policy Service + Policy Controller     |
| 5  | Microsoft Defender for Cloud               | AWS Security Hub + GuardDuty + Inspector              | Security Command Center                             |
| 6  | Microsoft Sentinel                         | AWS Security Hub + Detective                          | Chronicle Security Operations                       |

---

## 1. Azure Active Directory (Microsoft Entra ID)  

### Overview  
Azure Active Directory (Microsoft Entra ID) is Microsoft’s cloud-based identity and access management (IAM) service. It provides **SSO, MFA, conditional access, and identity governance** for securing applications and resources.

**AWS Equivalent:** AWS IAM + IAM Identity Center  
**GCP Equivalent:** Google Cloud Identity + Cloud IAM  

### Core Features  
- SSO for cloud and on-prem apps  
- MFA and Conditional Access policies  
- Role-based access control (RBAC)  
- B2B and B2C identity federation  
- Integration with OAuth2, SAML, OpenID Connect  

### Security & Compliance  
- ISO 27001, SOC 1/2/3, FedRAMP, HIPAA  
- Supports passwordless authentication  
- Conditional access for Zero Trust security  

### Pricing Model  
- Free tier (basic identity services)  
- Premium P1/P2 based on per-user/month  
- AWS/GCP pricing: mostly free for basic IAM; charges apply for SSO & advanced features  

### DevSecOps Integration  
- API-based automation for user & policy management  
- Integrates with CI/CD pipelines for secure deployments  
- Works with GitHub Actions, Azure DevOps, AWS CodePipeline, and GCP Cloud Build  

---

## 2. Azure Monitor  

### Overview  
Azure Monitor is a unified platform for collecting, analyzing, and acting on telemetry data from cloud and on-prem resources.  

**AWS Equivalent:** Amazon CloudWatch  
**GCP Equivalent:** Google Cloud Monitoring  

### Core Features  
- Metrics and log collection  
- Application Insights for APM  
- Alerts, dashboards, and visualization  
- Auto-scale based on performance metrics  

### Security & Compliance  
- Encrypted in transit and at rest  
- Role-based access to monitoring data  
- Supports compliance requirements like SOC, ISO  

### Pricing Model  
- Pay-as-you-go based on data ingestion & retention  
- AWS/GCP: similar pay-per-GB-ingested model  

### DevSecOps Integration  
- Connects to CI/CD tools for automated alerting  
- API & CLI for custom integrations  
- Hooks into incident management (PagerDuty, ServiceNow, Slack)  

---

## 3. Azure Log Analytics  

### Overview  
Azure Log Analytics is part of Azure Monitor that enables querying and analyzing log data using **Kusto Query Language (KQL)**.  

**AWS Equivalent:** CloudWatch Logs + CloudWatch Logs Insights  
**GCP Equivalent:** Cloud Logging (+ BigQuery for advanced analysis)  

### Core Features  
- Centralized log collection  
- KQL for advanced queries  
- Integration with Application Insights & Sentinel  
- Custom dashboards and reports  

### Security & Compliance  
- Data encryption at rest/in transit  
- Access control via Azure RBAC  
- Meets SOC, ISO, HIPAA requirements  

### Pricing Model  
- Pay-per-GB-ingested + retention costs  
- AWS/GCP: similar usage-based log storage & query costs  

### DevSecOps Integration  
- Automates log collection during deployments  
- Enables proactive monitoring of CI/CD pipelines  
- Supports alert automation for anomalies  

---

## 4. Azure Policy  

### Overview  
Azure Policy allows you to create, assign, and manage policies to enforce organizational compliance and governance rules.  

**AWS Equivalent:** AWS Config + Service Control Policies (SCPs)  
**GCP Equivalent:** Organization Policy Service + Policy Controller  

### Core Features  
- Policy definitions (allow/deny actions)  
- Compliance dashboards  
- Resource tagging enforcement  
- Location/region restrictions  

### Security & Compliance  
- Enforces compliance with security baselines  
- Helps maintain ISO, HIPAA, NIST standards  
- Auditing & remediation support  

### Pricing Model  
- Included with Azure (no extra cost for basic)  
- AWS Config/GCP: pay for configuration item tracking and evaluations  

### DevSecOps Integration  
- Validates deployments in CI/CD pipelines  
- Prevents non-compliant resources at build time  
- Works with Terraform & ARM templates for policy-as-code  

---

## 5. Microsoft Defender for Cloud  

### Overview  
Microsoft Defender for Cloud is a cloud-native security posture management (CSPM) and workload protection (CWPP) tool.  

**AWS Equivalent:** AWS Security Hub + GuardDuty + Inspector  
**GCP Equivalent:** Security Command Center  

### Core Features  
- Continuous security assessment  
- Threat detection & response  
- Vulnerability scanning  
- Recommendations for security hardening  

### Security & Compliance  
- Supports CIS, PCI-DSS, ISO, HIPAA frameworks  
- AI-driven threat detection  
- Real-time security alerts  

### Pricing Model  
- Free tier for CSPM; paid for workload protection per resource type  
- AWS/GCP follow per-resource and per-scan pricing  

### DevSecOps Integration  
- Security scanning in CI/CD pipelines  
- API integration for automated remediation  
- Works with Azure DevOps, GitHub, AWS CodePipeline, GCP Cloud Build  

---

## 6. Microsoft Sentinel  

### Overview  
Microsoft Sentinel is a cloud-native **SIEM** (Security Information and Event Management) and **SOAR** (Security Orchestration, Automation, and Response) platform.  

**AWS Equivalent:** AWS Security Hub + Detective  
**GCP Equivalent:** Chronicle Security Operations  

### Core Features  
- Centralized security log ingestion  
- AI/ML threat detection  
- Automated incident response playbooks  
- Threat hunting with KQL  

### Security & Compliance  
- Meets SOC, ISO, FedRAMP, and GDPR requirements  
- Integrates with threat intelligence feeds  
- Supports compliance auditing  

### Pricing Model  
- Pay-per-GB-ingested with 90-day free retention  
- AWS/GCP: pay-per-data-ingestion or events analyzed  

### DevSecOps Integration  
- Ingests logs from DevOps pipelines  
- Automates response to security incidents during deployments  
- Works with Logic Apps, AWS Lambda, GCP Functions for automation  

---

##  Conclusion  
While Azure, AWS, and GCP offer **similar core functionalities**, the choice depends on:  
- **Integration needs** (e.g., Azure AD works best in Microsoft environments)  
- **Pricing models** for logs & monitoring  
- **Compliance certifications** required by your organization  
- **Ecosystem alignment** with existing DevOps toolchains  

In practice, most enterprises adopt a **multi-cloud approach**, selecting the best tool from each provider while maintaining governance, compliance, and automation pipelines.

---
