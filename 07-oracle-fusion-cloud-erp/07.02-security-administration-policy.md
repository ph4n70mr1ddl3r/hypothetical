# Oracle Fusion Cloud ERP Security and Administration Policy

## BuildRight Home Improvement, Inc. (BRHI)

---

## 1. Document Control

| Field | Detail |
|---|---|
| **Document ID** | BRHI-SEC-001 |
| **Version** | 1.1 |
| **Classification** | Internal — Confidential |
| **Effective Date** | April 2, 2026 |
| **Document Owner** | Chief Technology Officer |
| **Approved By** | Executive Leadership Team |
| **Review Cycle** | Quarterly |
| **Next Review Date** | July 2, 2026 |
| **Distribution** | IT Department, Security Team, Oracle CoE, Business Process Owners |

### Revision History

| Version | Date | Author | Description |
|---|---|---|---|
| 1.1 | April 2, 2026 | Security and Compliance Team | Added AI and agent security section |
| 1.0 | April 2, 2026 | Security and Compliance Team | Initial release — comprehensive security policy |

---

## 2. Purpose and Scope

### 2.1 Purpose

This policy establishes the security framework for Oracle Fusion Cloud ERP at BuildRight Home Improvement, Inc. It defines:

- **Access Control Standards**: How access is granted, reviewed, and revoked
- **Data Protection Requirements**: Safeguards for sensitive financial and personal data
- **Administrative Procedures**: Day-to-day security administration processes
- **Compliance Requirements**: SOX, GDPR, and other regulatory obligations
- **Incident Response Procedures**: How security incidents are detected, reported, and resolved

### 2.2 Scope

This policy applies to:

- All Oracle Fusion Cloud ERP modules deployed at BuildRight
- All users accessing Oracle Fusion Cloud ERP (employees, contractors, suppliers)
- All data stored in or transmitted through Oracle Fusion Cloud ERP
- All integrations with Oracle Fusion Cloud ERP
- All Oracle Cloud Infrastructure (OCI) components used by BuildRight

### 2.3 Regulatory Framework

| Regulation | Applicability | Key Requirements |
|---|---|---|
| **Sarbanes-Oxley (SOX)** | U.S. public company | Internal controls over financial reporting |
| **GDPR** | EU citizen data | Data protection, consent, right to erasure |
| **CCPA** | California residents | Consumer privacy rights |
| **PCI DSS** | Payment card data | Secure payment processing |
| **SOC 2** | Service providers | Security, availability, processing integrity |
| **CFIUS** | Foreign investment | Data sovereignty requirements |

---

## 3. Access Control Policy

### 3.1 Role-Based Access Control (RBAC)

Oracle Fusion Cloud ERP uses a three-tier RBAC model:

**Tier 1: Job Roles**
- Based on organizational job functions
- Examples: Store Manager, AP Clerk, HR Business Partner
- Assigned based on position in organizational hierarchy

**Tier 2: Duty Roles**
- Functional permissions grouped by business process
- Examples: Invoice Processing, Payment Processing, GL Journal Entry
- Assigned based on job role requirements

**Tier 3: Privileges**
- Specific actions within the system
- Examples: Create Invoice, Approve Payment, Run Report
- Assigned based on duty role requirements

### 3.2 Access Request Process

#### 3.2.1 New User Access

1. **Request Initiation**
   - Manager submits access request via Oracle Self-Service Portal
   - Required information: User name, position, required access, business justification
   - Request timestamp recorded automatically

2. **Manager Approval**
   - Direct manager reviews and approves request
   - Manager must confirm business need and appropriateness of access
   - Approval timestamp recorded

3. **Segregation of Duties (SoD) Check**
   - Oracle Risk Management Cloud performs automated SoD analysis
   - Conflicts flagged for review before provisioning
   - Conflicts require risk acceptance from appropriate authority

4. **Security Administration**
   - Security team provisions access based on approved roles
   - Access provisioned with effective date (typically next business day)
   - User receives welcome email with login instructions

5. **Training Verification**
   - User must complete required training before access is activated
   - Training completion tracked in Oracle HCM Learning
   - Compliance training required annually

#### 3.2.2 Access Modification

1. **Change Request**
   - Manager submits change request with business justification
   - Current access reviewed for continued need
   - SoD check performed for new access combinations

2. **Approval and Implementation**
   - Same approval process as new access
   - Old access revoked if no longer needed
   - Change documented in audit trail

#### 3.2.3 Access Termination

1. **Automated Termination**
   - Access automatically terminated upon employment end date
   - Integration with HR system triggers termination workflow
   - Termination effective at end of business day

2. **Manual Termination**
   - Security team can manually terminate access for immediate need
   - Used for disciplinary actions or immediate risk mitigation
   - Requires manager or HR approval

### 3.3 Privileged Access Management

#### 3.3.1 Administrative Roles

| Role | Access Level | Approval Required | Review Frequency |
|---|---|---|---|
| **Security Administrator** | Full security configuration | CTO approval | Monthly |
| **Application Administrator** | Module configuration | CTO approval | Monthly |
| **Technical Administrator** | Infrastructure and integration | CTO approval | Monthly |
| **Audit Administrator** | Read-only access to audit logs | CIO approval | Quarterly |

#### 3.3.2 Privileged Access Controls

1. **Multi-Factor Authentication (MFA)**
   - Required for all administrative roles
   - Hardware token or authenticator app required
   - Session timeout: 15 minutes for administrative access

2. **Just-In-Time (JIT) Access**
   - Administrative access granted only for specific tasks
   - Temporary elevation with automatic expiration
   - All actions logged and reviewed

3. **Break-Glass Procedure**
   - Emergency access for critical system issues
   - Requires two-person authorization
   - Post-incident review required within 24 hours

### 3.4 Access Certification

#### 3.4.1 Quarterly User Access Reviews

1. **Certification Campaign Initiation**
   - Oracle Risk Management Cloud initiates certification campaigns
   - Campaign distributed to certification owners (managers)
   - 30-day window for completion

2. **Certification Process**
   - Manager reviews each direct report's access
   - Certifies appropriateness for current role
   - Flags unnecessary access for revocation

3. **Remediation**
   - Unnecessary access revoked within 5 business days
   - Conflicting access remediated within 10 business days
   - Escalation for non-compliance

#### 3.4.2 Annual Comprehensive Review

1. **Full Access Audit**
   - Complete review of all user access
   - Comparison with organizational structure
   - Identification of orphaned accounts

2. **SoD Analysis**
   - Comprehensive SoD conflict analysis
   - Risk assessment for existing conflicts
   - Remediation plan for high-risk conflicts

3. **Policy Compliance Assessment**
   - Review of access provisioning processes
   - Assessment of control effectiveness
   - Recommendations for improvement

---

## 4. Data Protection Policy

### 4.1 Data Classification

| Classification | Description | Examples | Protection Requirements |
|---|---|---|---|
| **Public** | Information intended for public distribution | Marketing materials, public financials | Standard protection |
| **Internal** | Information for internal use only | Process documentation, training materials | Access control, encryption in transit |
| **Confidential** | Sensitive business information | Financial data, customer data, vendor contracts | Encryption at rest and in transit, access logging |
| **Restricted** | Highly sensitive information | PII, payment card data, trade secrets | Strong encryption, strict access control, monitoring |

### 4.2 Encryption Standards

#### 4.2.1 Data at Rest

- **Database Encryption**: Oracle Transparent Data Encryption (TDE)
- **File Encryption**: AES-256 encryption for all sensitive files
- **Backup Encryption**: All backups encrypted with separate encryption keys
- **Key Management**: Oracle Key Vault for centralized key management

#### 4.2.2 Data in Transit

- **Transport Encryption**: TLS 1.2 or higher for all connections
- **API Security**: OAuth 2.0 with JWT tokens for API access
- **File Transfer**: SFTP with encryption for batch file transfers
- **VPN Requirements**: VPN required for administrative access

### 4.3 Data Loss Prevention (DLP)

#### 4.3.1 Controls

1. **Content Inspection**
   - Automated scanning of outbound data
   - Pattern matching for sensitive data (SSN, credit cards, etc.)
   - Alert and block on policy violations

2. **Access Monitoring**
   - Real-time monitoring of sensitive data access
   - Alert on unusual access patterns
   - Integration with SIEM for correlation

3. **Watermarking**
   - Digital watermarks on sensitive reports
   - Track and trace capabilities
   - Deterrence against unauthorized sharing

#### 4.3.2 Data Retention and Disposal

| Data Type | Retention Period | Disposal Method |
|---|---|---|
| **Financial Records** | 7 years | Secure deletion with verification |
| **Employee Records** | Employment + 7 years | Secure deletion with verification |
| **Customer Data** | 7 years after last transaction | Secure deletion with verification |
| **Audit Logs** | 7 years | Archive and secure deletion |
| **System Logs** | 1 year | Automated purge |

### 4.4 Privacy Controls

#### 4.4.1 Personal Data Processing

1. **Lawful Basis**
   - Document lawful basis for all personal data processing
   - Maintain records of processing activities
   - Regular review of processing purposes

2. **Data Subject Rights**
   - Right to access: Provide personal data upon request
   - Right to rectification: Correct inaccurate data
   - Right to erasure: Delete personal data upon valid request
   - Right to portability: Export data in machine-readable format

3. **Data Protection Impact Assessment (DPIA)**
   - Required for high-risk processing activities
   - Conducted before implementation of new processing
   - Documented and reviewed annually

---

## 5. System Administration Policy

### 5.1 Change Management

#### 5.1.1 Configuration Changes

1. **Change Request**
   - All configuration changes require change request
   - Business justification and impact assessment required
   - Emergency changes require separate process

2. **Approval Process**
   - Low-risk changes: Oracle CoE approval
   - Medium-risk changes: Business process owner approval
   - High-risk changes: Steering committee approval

3. **Testing Requirements**
   - Unit testing in development environment
   - Integration testing with related processes
   - User acceptance testing (UAT)
   - Regression testing for existing functionality

4. **Deployment**
   - Scheduled deployment during maintenance windows
   - Rollback plan required for all changes
   - Post-deployment verification

#### 5.1.2 Quarterly Updates

Oracle releases quarterly updates that are mandatory for all customers.

1. **Update Review**
   - Review release notes 30 days before update
   - Identify features and changes relevant to BuildRight
   - Assess impact on customizations and integrations

2. **Testing Cycle**
   - Test in Oracle test environment
   - Validate critical business processes
   - Test integrations and custom reports

3. **Opt-In Process**
   - Evaluate new features for opt-in
   - Test opt-in features before activation
   - Schedule opt-in activation

### 5.2 Monitoring and Alerting

#### 5.2.1 System Monitoring

| Metric | Monitoring Tool | Alert Threshold | Response Time |
|---|---|---|---|
| **System Availability** | Oracle Infrastructure Monitoring | < 99.9% | 15 minutes |
| **Response Time** | Application Performance Monitoring | > 2 seconds | 30 minutes |
| **Error Rate** | Log Analytics | > 1% | 15 minutes |
| **Integration Failures** | Integration Monitoring | Any failure | 15 minutes |
| **Security Events** | SIEM | Any critical event | Immediate |

#### 5.2.2 Security Monitoring

1. **User Activity Monitoring**
   - Log all user logins and logouts
   - Monitor for failed login attempts
   - Alert on suspicious activity patterns

2. **Privileged Activity Monitoring**
   - Log all administrative actions
   - Monitor configuration changes
   - Alert on unauthorized access attempts

3. **Data Access Monitoring**
   - Log access to sensitive data
   - Monitor bulk data exports
   - Alert on unusual data access patterns

### 5.3 Backup and Recovery

#### 5.3.1 Backup Strategy

| Backup Type | Frequency | Retention | Storage |
|---|---|---|---|
| **Full Backup** | Daily | 30 days | Oracle Cloud Object Storage |
| **Incremental Backup** | Hourly | 7 days | Oracle Cloud Object Storage |
| **Transaction Logs** | Continuous | 7 days | Oracle Cloud Object Storage |
| **Configuration Backup** | Weekly | 90 days | Oracle Cloud Object Storage |

#### 5.3.2 Recovery Procedures

1. **Point-in-Time Recovery**
   - Available for up to 30 days
   - Recovery time: 2-4 hours depending on data volume
   - Requires approval from CTO or designee

2. **Disaster Recovery**
   - Oracle's disaster recovery services
   - Recovery Time Objective (RTO): 4 hours
   - Recovery Point Objective (RPO): 1 hour
   - Annual DR testing required

---

## 6. Incident Response Policy

### 6.1 Incident Classification

| Severity | Description | Examples | Response Time | Resolution Time |
|---|---|---|---|---|
| **Critical** | System down or major security breach | System outage, data breach | 15 minutes | 4 hours |
| **High** | Significant impact on business operations | Major integration failure, large-scale data issue | 1 hour | 8 hours |
| **Medium** | Moderate impact, workaround available | Non-critical integration issue, performance degradation | 4 hours | 24 hours |
| **Low** | Minor impact, no workaround needed | Cosmetic issues, minor bugs | 24 hours | 72 hours |

### 6.2 Incident Response Process

#### 6.2.1 Detection and Reporting

1. **Detection Methods**
   - Automated monitoring and alerting
   - User reports via help desk
   - Oracle Support alerts
   - Audit findings

2. **Initial Reporting**
   - Report via help desk portal or hotline
   - Include: What happened, when, impact, who is affected
   - Automatic ticket creation with timestamp

#### 6.2.2 Analysis and Classification

1. **Initial Assessment**
   - Triage team assesses severity and impact
   - Assign incident classification
   - Identify initial response team

2. **Root Cause Analysis**
   - Investigate technical and business causes
   - Document findings and evidence
   - Identify contributing factors

#### 6.2.3 Containment and Recovery

1. **Immediate Containment**
   - Isolate affected systems if necessary
   - Implement temporary workarounds
   - Preserve evidence for investigation

2. **Recovery Actions**
   - Implement permanent fix
   - Restore services
   - Verify recovery

#### 6.2.4 Post-Incident Review

1. **Lessons Learned**
   - Conduct post-incident review within 48 hours
   - Document root cause and contributing factors
   - Identify process improvements

2. **Follow-Up Actions**
   - Assign action items with owners and deadlines
   - Track completion of action items
   - Update procedures and training as needed

### 6.3 Security Incident Response

#### 6.3.1 Security Breach Protocol

1. **Immediate Actions**
   - Contain the breach
   - Preserve evidence
   - Notify security team lead

2. **Investigation**
   - Determine scope and impact
   - Identify affected data and users
   - Preserve forensic evidence

3. **Notification**
   - Notify legal and compliance teams
   - Assess regulatory notification requirements
   - Notify affected parties as required by law

4. **Remediation**
   - Implement security fixes
   - Update security controls
   - Conduct security review

---

## 7. Compliance and Audit

### 7.1 SOX Compliance

#### 7.1.1 Key Controls

| Control Area | Control Description | Oracle Feature |
|---|---|---|
| **Access Controls** | Proper segregation of duties | Oracle Risk Management Cloud SoD |
| **Transaction Controls** | Proper authorization and recording | Workflow approvals, audit trails |
| **Financial Reporting** | Accurate and complete reporting | Consolidation, reconciliation |
| **IT General Controls** | Change management, access management | Configuration controls, monitoring |

#### 7.1.2 Continuous Monitoring

1. **Automated Testing**
   - Daily testing of key controls
   - Automated remediation for certain violations
   - Exception reporting for manual review

2. **Manual Testing**
   - Quarterly manual control testing
   - Annual comprehensive control assessment
   - External auditor coordination

### 7.2 Audit Trail Requirements

#### 7.2.1 Logging Requirements

| Event Type | Required Information | Retention Period |
|---|---|---|
| **User Access** | User ID, timestamp, IP address, success/failure | 7 years |
| **Data Changes** | User ID, timestamp, before/after values | 7 years |
| **Configuration Changes** | User ID, timestamp, changes made | 7 years |
| **Financial Transactions** | User ID, timestamp, transaction details | 7 years |
| **System Events** | Event type, timestamp, severity | 1 year |

#### 7.2.2 Audit Report Requirements

1. **Regular Reports**
   - Daily: Security events, system availability
   - Weekly: Access changes, configuration changes
   - Monthly: Compliance status, KPI dashboard
   - Quarterly: Comprehensive audit report

2. **On-Demand Reports**
   - User access report
   - SoD conflict report
   - Transaction audit trail
   - System change log

---

## 8. Training and Awareness

### 8.1 Security Training Requirements

| Role | Training | Frequency | Duration |
|---|---|---|---|
| **All Users** | Security awareness | Annual | 1 hour |
| **Administrative Users** | Advanced security | Annual | 4 hours |
| **Developers** | Secure development | Annual | 8 hours |
| **Management** | Security governance | Annual | 2 hours |

### 8.2 Policy Acknowledgment

1. **Initial Acknowledgment**
   - All users must acknowledge security policy upon access provisioning
   - Acknowledgment recorded in Oracle HCM
   - Access provisioned only after acknowledgment

2. **Annual Re-Acknowledgment**
   - Annual policy review and re-acknowledgment required
   - Tracking of acknowledgment completion
   - Escalation for non-compliance

---

## 9. Roles and Responsibilities

### 9.1 Security Governance

| Role | Responsibilities |
|---|---|
| **CTO** | Overall security accountability, policy approval |
| **Security Director** | Security program management, incident response |
| **Security Administrators** | Day-to-day security operations |
| **Business Process Owners** | Access approvals, SoD risk acceptance |
| **Managers** | User access certification, training compliance |
| **All Users** | Policy compliance, incident reporting |

### 9.2 Oracle Cloud Operations

| Role | Responsibilities |
|---|---|
| **Oracle CoE Lead** | Overall Oracle operations management |
| **Application Administrators** | Module configuration, user support |
| **Integration Administrators** | Integration monitoring and maintenance |
| **Database Administrators** | Performance tuning, backup management |

---

## 10. Policy Enforcement

### 10.1 Compliance Monitoring

1. **Automated Compliance Checks**
   - Daily compliance scanning
   - Real-time policy violation detection
   - Automated reporting and alerting

2. **Manual Compliance Reviews**
   - Quarterly policy compliance review
   - Annual comprehensive assessment
   - External audit coordination

### 10.2 Violations and Consequences

| Violation Type | Severity | Potential Consequence |
|---|---|---|
| **Policy Non-Compliance** | Low-Medium | Training, warning |
| **Access Control Violations** | Medium-High | Suspension, termination |
| **Data Security Violations** | High | Termination, legal action |
| **Fraud or Theft** | Critical | Immediate termination, legal action |

### 10.3 Waiver Process

1. **Policy Exception Request**
   - Business justification required
   - Risk assessment and mitigation plan
   - Time-limited exception

2. **Approval Requirements**
   - Low-risk exceptions: Security Director approval
   - High-risk exceptions: CTO approval
   - All exceptions documented and reviewed

---

## 11. AI and Agent Security

### 11.1 AI Security Framework

#### 11.1.1 AI-Specific Security Risks

| Risk Category | Description | Controls |
|---|---|---|
| **Model Poisoning** | Malicious data corrupts AI models | Input validation, model monitoring, anomaly detection |
| **Adversarial Attacks** | Manipulated inputs cause AI errors | Robust model design, input sanitization, human review |
| **Data Leakage** | AI models leak sensitive training data | Differential privacy, data anonymization, access controls |
| **Bias Exploitation** | AI biases are exploited for unfair advantage | Bias testing, fairness monitoring, diverse training data |
| **Over-reliance** | Associates blindly trust AI recommendations | Training on AI limitations, human oversight requirements |

#### 11.1.2 AI Security Controls

1. **Model Governance**
   - All AI models must be approved by AI Ethics Committee
   - Models must be tested for security vulnerabilities before deployment
   - Regular security audits of AI models and training data
   - Version control and rollback capabilities for all AI models

2. **Data Protection for AI**
   - Training data must follow data classification policies
   - Personal data anonymized for AI training where possible
   - Encryption of AI training data and model artifacts
   - Access controls for AI development and production environments

3. **AI Access Controls**
   - Role-based access to AI agent capabilities
   - Audit logging of all AI agent interactions
   - Approval workflows for sensitive AI decisions
   - Monitoring for unusual AI agent behavior

### 11.2 AI Agent Security Configuration

#### 11.2.1 Agent Authentication and Authorization

| Security Control | Requirement | Implementation |
|---|---|---|
| **Agent Identity** | Each AI agent has unique identity | Oracle AI agent service accounts |
| **Authentication** | Agents authenticate before actions | API keys, OAuth tokens |
| **Authorization** | Agents authorized for specific actions | RBAC applied to AI agents |
| **Audit Logging** | All agent actions logged | AI agent audit logs in Oracle |

#### 11.2.2 AI Decision Security

1. **Critical Decision Controls**
   - Financial transactions > $10,000 require human approval
   - Supplier contract decisions > $100,000 require human review
   - Hiring decisions require human final approval
   - Termination recommendations require HR review

2. **Override and Escalation**
   - Associates can override AI recommendations with documented reason
   - Escalation paths for AI decisions requiring higher approval
   - Manual process alternatives for critical functions
   - Regular review of AI override patterns

### 11.3 AI Incident Response

#### 11.3.1 AI Security Incident Types

| Incident Type | Examples | Response Priority |
|---|---|---|
| **AI Malfunction** | Incorrect recommendations, system errors | High |
| **AI Bias Detection** | Discriminatory outcomes, unfair treatment | Critical |
| **AI Data Breach** | Sensitive data exposed through AI | Critical |
| **AI Manipulation** | Adversarial attacks, model poisoning | Critical |
| **AI Over-reliance** | Business disruption due to AI failure | High |

#### 11.3.2 AI Incident Response Process

1. **Detection and Reporting**
   - AI monitoring systems detect anomalies
   - Associates report AI issues through standard channels
   - Regular AI performance reviews identify issues

2. **Assessment and Containment**
   - AI Ethics Committee assesses severity
   - Malfunctioning AI agents may be disabled
   - Manual processes activated as backup
   - Affected users notified

3. **Investigation and Remediation**
   - Root cause analysis of AI issue
   - Model retraining or replacement if needed
   - Process improvements to prevent recurrence
   - Documentation and lessons learned

4. **Recovery and Monitoring**
   - AI agent restored with fixes
   - Enhanced monitoring for recurrence
   - User communication about resolution
   - Post-incident review

### 11.4 AI Compliance Requirements

#### 11.4.1 Regulatory Compliance for AI

| Regulation | AI Requirements | BuildRight Controls |
|---|---|---|
| **EU AI Act** | Risk-based AI regulation | AI risk assessment, transparency requirements |
| **SOX** | AI controls over financial reporting | AI model validation, audit trails |
| **GDPR** | AI processing of personal data | Privacy by design, consent management |
| **EEOC** | AI in employment decisions | Bias testing, fairness monitoring |

#### 11.4.2 AI Audit Requirements

1. **Model Audits**
   - Annual audit of AI models for bias and fairness
   - Validation of AI decision logic and outputs
   - Review of training data and methodologies
   - Documentation of model changes and updates

2. **Process Audits**
   - Review of AI governance processes
   - Assessment of AI security controls
   - Evaluation of AI ethics compliance
   - Testing of AI incident response procedures

---

## 12. Appendices

### Appendix A: Security Contact Information

| Role | Contact | Phone |
|---|---|---|
| **Security Incident Hotline** | security@buildright.com | 1-800-BUILD-SEC |
| **Help Desk** | helpdesk@buildright.com | 1-800-BUILD-IT |
| **Security Director** | security.director@buildright.com | 404-555-0301 |
| **CTO** | cto@buildright.com | 404-555-0102 |

### Appendix B: Related Policies

- Information Security Policy (BRHI-SEC-002)
- Data Classification Policy (BRHI-SEC-003)
- Privacy Policy (BRHI-SEC-004)
- Acceptable Use Policy (BRHI-SEC-005)
- Incident Response Policy (BRHI-SEC-006)
- Business Continuity Policy (BRHI-BCM-001)

### Appendix C: Definitions

| Term | Definition |
|---|---|
| **RBAC** | Role-Based Access Control |
| **SoD** | Segregation of Duties |
| **MFA** | Multi-Factor Authentication |
| **SIEM** | Security Information and Event Management |
| **DLP** | Data Loss Prevention |
| **TDE** | Transparent Data Encryption |
| **RTO** | Recovery Time Objective |
| **RPO** | Recovery Point Objective |

---

*This document is the property of BuildRight Home Improvement, Inc. and is intended for internal use by authorized associates. Unauthorized distribution, reproduction, or disclosure is prohibited. For questions regarding this document, contact the Security and Compliance Team at security@buildright.com or extension 4-0003.*