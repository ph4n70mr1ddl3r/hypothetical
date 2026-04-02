# Information Security and Data Privacy Policy

## Document Control

| Field | Value |
|---|---|
| **Document ID** | BRHI-POL-004 |
| **Version** | 3.1 |
| **Classification** | Confidential |
| **Effective Date** | April 2, 2026 |
| **Last Reviewed** | April 2, 2026 |
| **Next Review Date** | December 15, 2026 |
| **Document Owner** | Chief Information Security Officer (CISO) |
| **Approved By** | Executive Leadership Team |

### Revision History

| Version | Date | Author | Description of Changes |
|---|---|---|---|
| 1.0 | 2023-01-01 | M. Torres, CISO | Initial publication |
| 2.0 | 2024-06-15 | M. Torres, CISO | Added CCPA/CPRA section, updated encryption standards, revised incident response times |
| 3.0 | 2025-12-15 | M. Torres, CISO | Added Zero Trust roadmap, expanded cloud security, updated PCI DSS v4.0 alignment, revised MFA requirements |
| 3.1 | 2026-04-02 | M. Torres, CISO | Added Oracle Cloud Infrastructure to approved providers, Oracle Fusion Cloud ERP security requirements |

### Distribution

This document is classified as **Confidential** and is available to all BRHI associates on the corporate intranet. Printed copies are uncontrolled. The electronic version on the BRHI Policy Portal is the only controlled copy.

---

## 1. Policy Statement

BuildRight Home Improvement, Inc. (BRHI) is committed to protecting the confidentiality, integrity, and availability of all information assets entrusted to us by our customers, associates, vendors, and business partners. Information security is a foundational element of our business operations and is essential to maintaining the trust our stakeholders place in us.

As Chief Information Security Officer, I affirm that BRHI will:

- Implement and maintain a comprehensive information security program aligned with the NIST Cybersecurity Framework (CSF) 2.0, ISO/IEC 27001:2022, and applicable regulatory requirements.
- Protect customer data, including payment card information, personal identifiable information (PII), and business-sensitive data, with appropriate administrative, technical, and physical safeguards.
- Foster a culture of security awareness and accountability across all levels of the organization.
- Continuously monitor, assess, and improve our security posture to address evolving threats and vulnerabilities.
- Comply with all applicable federal, state, and international laws and regulations governing information security and data privacy.

Every BRHI associate, contractor, and third-party partner is responsible for adhering to this policy. Violations will be addressed through the enforcement procedures outlined in Section 19.

**Signed,**

**Maria Torres**
Chief Information Security Officer
BuildRight Home Improvement, Inc.
December 15, 2025

---

## 2. Scope

This policy applies to:

- **All information systems** owned, leased, or operated by BRHI, including but not limited to: point-of-sale (POS) systems, enterprise resource planning (ERP) platforms, e-commerce infrastructure, data warehouses, cloud environments, and corporate applications.
- **All data** created, collected, processed, stored, transmitted, or disposed of by BRHI, regardless of format (electronic, paper, verbal) or location.
- **All networks** operated by or connected to BRHI infrastructure, including corporate LANs, WANs, wireless networks, VPNs, and software-defined networks.
- **All devices** that access BRHI information systems, including desktop computers, laptops, tablets, smartphones, POS terminals, IoT devices, servers, and removable media.
- **All personnel** including full-time and part-time associates, temporary workers, contractors, consultants, interns, and any individual granted access to BRHI information systems.
- **All third parties** including vendors, suppliers, service providers, business partners, and their personnel who access, process, or store BRHI data.
- **All locations** including BRHI corporate headquarters, regional offices, distribution centers, retail stores, and remote work environments.

---

## 3. Information Classification

All BRHI information assets must be classified into one of four levels. The classification determines the minimum handling, storage, transmission, and disposal requirements.

### 3.1 Classification Levels

#### 3.1.1 Public

**Definition:** Information that has been approved for release to the general public and would not cause harm if disclosed.

**Examples:**
- Press releases and public financial reports
- Marketing materials and product catalogs
- Published store locations and hours
- Publicly available job postings

**Handling Requirements:**
- No special handling required for electronic or physical copies
- May be shared freely with external parties without approval
- No encryption required for storage or transmission
- No special disposal requirements; standard recycling is acceptable
- Published content must still be reviewed by Corporate Communications prior to release

#### 3.1.2 Internal

**Definition:** Information intended for use within BRHI that could cause minor impact if disclosed but would not result in significant financial, legal, or reputational harm.

**Examples:**
- Internal memos and newsletters
- Non-sensitive operational procedures
- Organizational charts and internal phone directories
- General meeting notes and project schedules
- Training materials not containing sensitive data

**Handling Requirements:**
- Sharing with external parties requires manager approval
- Storage on BRHI-managed systems or approved cloud platforms
- Transmission via BRHI email or approved collaboration tools
- Physical copies must be collected for disposal in standard shredding bins
- Access limited to BRHI associates and authorized contractors

#### 3.1.3 Confidential

**Definition:** Information that could cause significant harm to BRHI, its associates, customers, or business partners if disclosed to unauthorized parties.

**Examples:**
- Customer PII (names, addresses, phone numbers, email addresses)
- Associate personnel records and payroll data
- Financial reports prior to public release
- Vendor contracts and pricing agreements
- Internal audit reports and risk assessments
- Security policies and configuration details
- Strategic business plans and product roadmaps
- Customer purchase histories and analytics

**Handling Requirements:**
- Sharing with external parties requires director-level approval and a Non-Disclosure Agreement (NDA)
- Encryption required for electronic storage (AES-256 or equivalent) and transmission (TLS 1.2 or higher)
- Physical copies must be stored in locked cabinets or restricted-access areas
- Disposal must follow NIST SP 800-88 media sanitization guidelines (Clear, Purge, or Destroy)
- Access restricted to authorized personnel on a need-to-know basis
- Must be labeled "CONFIDENTIAL" on documents and in electronic file metadata
- Logging and monitoring of all access events
- Incident reporting required within 4 hours of suspected unauthorized disclosure

#### 3.1.4 Restricted

**Definition:** The most sensitive information requiring the highest level of protection. Unauthorized disclosure could result in severe financial loss, legal liability, regulatory penalties, or existential reputational damage.

**Examples:**
- Payment card data (primary account numbers, CVV, magnetic stripe data)
- Social Security numbers and government-issued identification numbers
- Authentication credentials (passwords, encryption keys, certificates)
- Security audit findings and vulnerability assessments
- Intellectual property, trade secrets, and proprietary algorithms
- Merger and acquisition documentation
- Legal hold materials and litigation-sensitive data
- Cryptographic keys and security token seeds

**Handling Requirements:**
- Sharing with external parties requires vice president-level approval, a executed NDA, and documented justification
- Encryption mandatory for all storage and transmission; AES-256 for data at rest; TLS 1.2+ for data in transit
- Physical copies must be stored in access-controlled, monitored environments with visitor logs
- Disposal must follow NIST SP 800-88 Destroy method (shredding, incineration, or degaussing for media)
- Access restricted to specifically named individuals with documented justification and vice president approval
- Must be labeled "RESTRICTED" on all media
- All access, modification, and transmission events must be logged with tamper-evident audit trails
- Incident reporting required within 1 hour of suspected unauthorized access or disclosure
- Data Loss Prevention (DLP) controls must actively monitor and block unauthorized transfers
- Copying or reproducing requires explicit approval from the data owner

### 3.2 Classification Responsibilities

- **Data Owners** (typically vice presidents or directors) are responsible for classifying data within their business units and reviewing classifications annually.
- **Data Custodians** (IT Operations, Database Administration) are responsible for implementing the technical controls required by the classification level.
- **All Personnel** are responsible for handling information according to its classification and reporting misclassification or mishandling to the Information Security team.

---

## 4. Access Control

### 4.1 Principles

#### 4.1.1 Least Privilege

All access to BRHI information systems must follow the principle of least privilege. Users shall be granted only the minimum level of access rights and permissions necessary to perform their assigned job functions. Access rights must be:

- Granted based on documented business justification
- Scoped to specific resources required for the role
- Time-limited where applicable (e.g., temporary project access)
- Reviewed and adjusted when job responsibilities change
- Revoked immediately when no longer required

#### 4.1.2 Role-Based Access Control (RBAC)

BRHI employs a Role-Based Access Control model for managing access to information systems. Access permissions are assigned to defined roles rather than to individual users. Users are then assigned to one or more roles based on their job function.

- Roles are defined by the business unit in collaboration with IT Security and documented in the BRHI Role Catalog.
- Each role has a predefined set of permissions mapped to specific applications and data classifications.
- New roles or modifications to existing roles must be approved by the role owner (director-level or above) and the Information Security team.
- Role assignments are reviewed quarterly for privileged roles and semi-annually for standard roles.

#### 4.1.3 Unique User Identification

Every individual who accesses BRHI information systems must be assigned a unique user identification (user ID). Shared or generic accounts are prohibited except where explicitly approved by the CISO for specific operational needs (e.g., POS service accounts).

- User IDs follow the standard naming convention: `firstname.lastname` (or `firstname.lastname##` for duplicates).
- User IDs must not reveal the user's privilege level or role.
- Each user is personally accountable for all activities performed under their user ID.
- Service accounts must be documented, assigned to an individual owner, and reviewed quarterly.

### 4.2 Authentication

#### 4.2.1 Password Policy

All BRHI systems must enforce the following password requirements:

| Parameter | Requirement |
|---|---|
| Minimum Length | 14 characters |
| Maximum Length | 128 characters |
| Complexity | Must contain at least three of the following four character types: uppercase letters, lowercase letters, numbers, special characters (!@#$%^&*()-_=+\|[]{};:'",.<>/?`) |
| Password History | Last 24 passwords remembered and cannot be reused |
| Maximum Age | 90 calendar days; system will prompt for change 14 days before expiration |
| Minimum Age | 1 day (passwords cannot be changed again within 24 hours) |
| Account Lockout | After 5 consecutive failed authentication attempts |
| Lockout Duration | 30 minutes (automatic unlock); manual unlock by IT Service Desk after identity verification |
| Default Passwords | Must be changed upon first login; all vendor default passwords must be changed before system deployment |

Additional requirements:

- Passphrases are encouraged and may exceed the 14-character minimum.
- Passwords must not contain the user's name, username, or the word "BRHI."
- Passwords must not be stored in plain text. Only cryptographically secure password storage methods (bcrypt, Argon2, or PBKDF2 with a minimum of 10,000 iterations) are permitted.
- Passwords must not be written down, stored in unprotected files, or shared with anyone, including IT staff.
- BRHI provides an approved enterprise password manager (currently CyberArk Endpoint Privilege Manager) for associates who need to manage multiple credentials.

#### 4.2.2 Multi-Factor Authentication (MFA)

MFA is required for the following systems and scenarios:

- **Remote access:** All VPN connections and remote desktop sessions
- **Privileged accounts:** All administrative accounts (local, domain, cloud)
- **Sensitive systems:** ERP, financial systems, HR systems, PCI-scoped systems
- **E-commerce:** All administrative access to the BRHI e-commerce platform
- **Cloud management consoles:** AWS, Azure, GCP, and SaaS administration
- **Email:** Web-based email access from non-corporate devices
- **Third-party applications:** All externally facing applications

Accepted MFA factors:

- **Approved primary factor:** Push notification via BRHI-approved authenticator app (Microsoft Authenticator, Okta Verify), hardware security key (FIDO2/WebAuthn), or time-based one-time password (TOTP) from approved authenticator app
- **Not approved as a primary factor:** SMS-based one-time passwords (may be used only as a backup factor with CISO approval for specific legacy systems)
- **Approved secondary factor:** Biometric verification (fingerprint, facial recognition) on BRHI-managed devices

MFA tokens and hardware keys must be registered through the IT Service Desk and are bound to the individual user. Sharing of MFA tokens is prohibited.

### 4.3 Privileged Access Management (PAM)

BRHI implements a comprehensive Privileged Access Management program:

- **PAM Vault:** All privileged credentials (root, admin, service accounts) must be stored in the CyberArk Privileged Access Security vault. Direct use of static privileged credentials is prohibited.
- **Session Isolation:** Privileged sessions to critical systems must be initiated through the PAM solution with session isolation and proxy capabilities.
- **Session Recording:** All privileged sessions are recorded (video and keystroke logging) and retained for a minimum of 12 months. Recordings are available for audit and forensic review.
- **Just-in-Time (JIT) Access:** Privileged access is granted on a temporary, as-needed basis with automatic expiration. Standing privileged access is prohibited except where documented and approved by the CISO.
- **Dual Authorization:** Changes to critical infrastructure (firewall rules, DNS records, domain controllers) require approval from a second authorized administrator before execution.
- **Quarterly Access Reviews:** Privileged access rights are reviewed quarterly by the data/system owner and the Information Security team. Findings are reported to the CISO and documented in the Governance, Risk, and Compliance (GRC) system.
- **Break-Glass Procedures:** Emergency access procedures exist for situations where standard PAM workflows cannot be followed. Break-glass access requires post-incident justification, CISO notification within 1 hour, and mandatory review within 24 hours.

### 4.4 Account Provisioning and Deprovisioning

#### 4.4.1 Provisioning

- All new accounts must be requested through the BRHI IT Service Management (ITSM) system with documented business justification and appropriate approvals (manager and system owner).
- Standard user accounts must be provisioned within 24 hours of the associate's start date or role change.
- Privileged accounts require additional approval from the CISO or designated security manager and must be provisioned through the PAM system.
- Contractor and temporary worker accounts must include an expiration date aligned with the contract end date. Extensions require documented re-approval.
- Third-party vendor accounts must be tied to an active contract and include an expiration date not exceeding the contract term.

#### 4.4.2 Deprovisioning

- Access for terminated associates must be disabled within 24 hours of termination notification. For involuntary terminations, access must be disabled within 1 hour of notification from Human Resources.
- The IT Service Desk receives automated termination notifications from the HR system (Workday) and executes the standard deprovisioning workflow, which includes: disabling Active Directory accounts, revoking VPN and remote access, disabling email access, revoking application-specific access, de-registering MFA tokens, collecting physical access badges and hardware tokens, and wiping or reclaiming mobile devices.
- A monthly reconciliation report comparing active HR records against active IT accounts is generated and reviewed by IT Security. Any discrepancies are investigated and resolved within 5 business days.
- Upon role change or transfer, the user's access rights are reviewed and adjusted within 5 business days.

### 4.5 Separation of Duties

BRHI enforces separation of duties for all financial and critical business systems to prevent fraud and errors:

- **Financial Systems:** No single individual may initiate, approve, and execute a financial transaction. At minimum, three separate roles must be involved: requestor, approver, and processor.
- **User Access Management:** Individuals who request user access cannot be the same individuals who approve or provision that access.
- **System Administration:** Developers cannot have production deployment access without separate approval. Production database administrators cannot have application development access in the same system.
- **Audit and Compliance:** Audit functions must be independent of the systems and processes they audit. Auditors cannot have administrative access to the systems under review.
- Violations of separation of duties controls must be reported to the CISO and documented in the GRC system for risk acceptance or remediation.

---

## 5. Data Protection

### 5.1 Encryption

#### 5.1.1 Encryption at Rest

All BRHI data classified as Confidential or Restricted must be encrypted at rest using Advanced Encryption Standard (AES) with a minimum key length of 256 bits (AES-256).

| Data Category | Encryption Standard | Key Management |
|---|---|---|
| Customer PII | AES-256 | Enterprise Key Management System (KMS) |
| Payment Card Data | AES-256 | Hardware Security Module (HSM) - FIPS 140-2 Level 3 |
| Associate Records | AES-256 | Enterprise KMS |
| Financial Data | AES-256 | Enterprise KMS |
| Encryption Keys | RSA-4096 (key wrapping) | HSM - FIPS 140-2 Level 3 |
| Backup Media | AES-256 | Enterprise KMS |

Full-disk encryption must be enabled on all endpoints (laptops, desktops, mobile devices) using BRHI-approved solutions (BitLocker for Windows, FileVault for macOS).

Key management procedures:

- Encryption keys must be stored separately from the data they protect.
- Key rotation must occur at least annually for data encryption keys and semi-annually for key encryption keys.
- Key destruction must follow documented procedures ensuring cryptographic erasure.
- Key recovery procedures must be documented and tested annually.
- All key management operations must be logged and auditable.

#### 5.1.2 Encryption in Transit

All data transmitted over any network must be protected using Transport Layer Security (TLS) version 1.2 or higher. The following protocols are prohibited: SSL 2.0, SSL 3.0, TLS 1.0, and TLS 1.1.

| Transmission Scenario | Minimum Standard |
|---|---|
| Web applications (external) | TLS 1.2+ with HSTS enabled |
| Web applications (internal) | TLS 1.2+ |
| Email (sensitive content) | TLS 1.2+ with message-level encryption (S/MIME or PGP) |
| File transfers | SFTP, SCP, or HTTPS (TLS 1.2+); FTP is prohibited |
| API communications | TLS 1.2+ with mutual TLS (mTLS) for system-to-system |
| Database connections | TLS 1.2+ with certificate-based authentication |
| VPN connections | IKEv2/IPsec or TLS 1.2+ based VPN |

Cipher suite requirements:

- Must use authenticated encryption with associated data (AEAD) cipher suites (e.g., AES-128-GCM, AES-256-GCM).
- RSA key exchange is prohibited; Ephemeral Diffie-Hellman (DHE) or Elliptic Curve Diffie-Hellman Ephemeral (ECDHE) must be used for forward secrecy.
- Certificate must use SHA-256 or higher signature algorithm; SHA-1 certificates are prohibited.

### 5.2 Data Loss Prevention (DLP)

BRHI deploys a comprehensive Data Loss Prevention program covering endpoint, network, and cloud environments:

#### 5.2.1 Endpoint DLP

- All BRHI-managed endpoints must have the DLP agent installed and active.
- DLP policies monitor and control data transfers via USB devices, clipboard operations, print jobs, email, and web uploads.
- Confidential and Restricted data must not be transferred to personal devices, personal cloud storage, or unapproved external media.

#### 5.2.2 Network DLP

- Network-based DLP inspects all outbound traffic including email, web, and file transfers for sensitive data patterns (credit card numbers, SSNs, health information).
- Violations trigger automated blocking for Restricted data and alerting for Confidential data.
- All DLP incidents are logged and routed to the Information Security team for investigation within 4 hours.

#### 5.2.3 Cloud DLP

- Cloud Access Security Broker (CASB) enforces DLP policies across all approved cloud services.
- Shadow IT discovery is enabled to identify and remediate use of unapproved cloud services.
- Cloud DLP policies enforce encryption, access controls, and sharing restrictions on documents containing sensitive data in cloud storage and collaboration platforms.

### 5.3 Data Retention

BRHI retains data only for as long as necessary to fulfill business, legal, and regulatory requirements. The following retention schedules apply:

| Data Category | Retention Period | Legal Basis |
|---|---|---|
| Customer transaction records | 7 years | Tax and financial regulations |
| Customer PII (active customers) | Duration of relationship + 3 years | CCPA/CPRA, business need |
| Customer PII (inactive customers) | 3 years from last transaction | CCPA/CPRA |
| Payment card data (tokenized) | Duration of relationship | PCI DSS |
| Full card numbers / CVV | Prohibited from storage | PCI DSS |
| Associate personnel records | 7 years post-termination | Federal and state employment law |
| Associate medical records | 30 years post-termination | HIPAA (where applicable) |
| Tax and financial records | 7 years | IRS regulations, SOX |
| Security logs and audit trails | 3 years | PCI DSS, SOX, internal policy |
| CCTV surveillance footage | 90 days | Internal policy, state laws |
| Email (business correspondence) | 5 years | Litigation hold policy |
| System backups | 30 days (daily), 13 months (monthly) | Business continuity |
| Vendor contracts | 7 years post-expiration | Contractual, regulatory |
| Litigation hold data | Until released by General Counsel | Legal hold procedures |

Expired data must be securely disposed of in accordance with Section 5.4 within 30 days of the expiration of the retention period, unless subject to a legal hold.

### 5.4 Secure Data Disposal

BRHI follows NIST Special Publication 800-88 Revision 1 (Guidelines for Media Sanitization) for all data disposal:

| Sanitization Method | Description | Applicable Data Classification |
|---|---|---|
| Clear | Overwriting with non-sensitive data | Internal |
| Purge | Degaussing or cryptographic erasure | Confidential |
| Destroy | Physical destruction (shredding, incineration, disintegration) | Restricted; all media being decommissioned |

Procedures:

- All hard drives and solid-state media from decommissioned systems must be either Purged (with documented verification) or Destroyed before leaving BRHI custody.
- Paper documents containing Confidential or Restricted data must be cross-cut shredded (minimum DIN 66399 Level P-4).
- Disposal of electronic media must be documented in the Asset Management system, including: asset tag, serial number, sanitization method, date, and technician name.
- Third-party disposal vendors must be vetted, hold current SOC 2 Type II reports, and provide certificates of destruction within 10 business days.
- Removable media (USB drives, external hard drives) must not be disposed of through standard waste; they must be submitted to IT for secure disposal.

### 5.5 Database Activity Monitoring

- All databases containing Confidential or Restricted data are monitored by Database Activity Monitoring (DAM) tools.
- DAM captures and analyzes all SQL activity, including queries, modifications, administrative actions, and privileged user activity.
- Alerts are configured for: unauthorized access attempts, bulk data extraction, schema changes, privilege escalation, and queries returning excessive records (more than 1,000 rows for non-reporting accounts).
- DAM logs are retained for 3 years and are stored in a tamper-evident, write-once storage system.
- DAM alerts are triaged by the Security Operations Center (SOC) within 1 hour during business hours and within 4 hours outside business hours.

---

## 6. Payment Card Security

### 6.1 PCI DSS Compliance

BRHI is committed to full compliance with the Payment Card Industry Data Security Standard (PCI DSS) version 4.0 for all systems that store, process, or transmit cardholder data.

- BRHI is validated as a PCI DSS Level 1 merchant and undergoes an annual on-site assessment by a Qualified Security Assessor (QSA).
- The QSA produces a Report on Compliance (ROC) and Attestation of Compliance (AOC) annually, submitted to the acquiring bank and card brands by March 31 of each year.
- Interim Self-Assessment Questionnaires (SAQs) may be completed for specific subsystems as determined by the QSA.
- The PCI Compliance Officer, reporting to the CISO, is responsible for coordinating all PCI DSS compliance activities.

### 6.2 Point-to-Point Encryption (P2PE)

- All BRHI retail locations use PCI-validated Point-to-Point Encryption (P2PE) solutions for card-present transactions.
- Cardholder data is encrypted at the point of interaction (POI) device within the payment terminal and remains encrypted until it reaches the secure decryption environment at the payment processor.
- BRHI does not store, process, or transmit clear-text cardholder data within the store environment.
- P2PE solution components, including payment terminals and decryption hardware, are listed on the PCI SSC Approved P2PE Solutions list.

### 6.3 Tokenization

- BRHI uses tokenization to replace primary account numbers (PANs) with non-sensitive tokens for any business purpose requiring post-transaction reference to card data (e.g., returns, loyalty programs, recurring billing).
- Tokens are generated by the payment processor using a PCI DSS-compliant tokenization system.
- The token-to-PAN mapping is maintained solely by the payment processor within their PCI DSS-certified environment.
- BRHI systems store and process only tokens; PANs are never stored in BRHI databases.

### 6.4 Network Segmentation for Cardholder Data Environment (CDE)

- The Cardholder Data Environment is logically and physically segmented from all other BRHI networks using PCI DSS-compliant network segmentation.
- Segmentation is implemented through firewalls, VLANs, and access control lists (ACLs) that restrict traffic flow between the CDE and all other network zones.
- The CDE includes only the systems directly involved in storing, processing, or transmitting cardholder data or that provide security services to the CDE.
- All inbound and outbound traffic to the CDE is restricted to the minimum necessary for business operations and is explicitly documented in firewall rule sets.
- Network segmentation is validated annually by the QSA as part of the PCI DSS assessment and through quarterly internal penetration testing.

### 6.5 Vulnerability Scanning and Penetration Testing

- **Quarterly external vulnerability scans** are performed by an Approved Scanning Vendor (ASV) against all external-facing IP addresses associated with the CDE.
- **Quarterly internal vulnerability scans** are performed by the BRHI Vulnerability Management team against all internal CDE systems.
- **Annual external penetration testing** is performed by a qualified independent third-party penetration testing firm against the CDE and critical e-commerce infrastructure.
- **Semi-annual internal penetration testing** is performed by the BRHI Red Team or an approved third party to test network segmentation and internal controls.
- All critical and high vulnerabilities identified through scanning or testing must be remediated within 30 days. Critical vulnerabilities in the CDE must be remediated within 15 days.
- Penetration testing results, including scope, methodology, findings, and remediation status, are documented and presented to the CISO and the PCI Steering Committee.

---

## 7. Network Security

### 7.1 Firewall Management

- All BRHI network perimeters and internal segment boundaries are protected by next-generation firewalls (NGFWs) deployed in high-availability pairs.
- Firewall rule sets must follow a default-deny posture; only explicitly authorized traffic is permitted.
- All firewall rules must include a business justification, a documented owner, and an expiration date (not to exceed 12 months for temporary rules).
- Firewall rule reviews are conducted quarterly by the Network Security team. Unused, duplicate, expired, or overly permissive rules must be remediated within 30 days of review.
- All firewall configuration changes must follow the BRHI Change Management process, including peer review, testing, and approval.
- Firewall logs must be forwarded to the SIEM and retained for a minimum of 1 year online and 3 years in archive.

### 7.2 Intrusion Detection and Prevention System (IDS/IPS)

- Network IDS/IPS is deployed at all network perimeters and at critical internal segment boundaries.
- IDS/IPS signatures are updated automatically at least every 4 hours from the vendor's threat intelligence feed.
- Custom IDS/IPS rules are developed by the Threat Intelligence team to address BRHI-specific threats.
- IPS is configured in inline mode at the perimeter and in detection mode for internal segments unless a specific threat warrants inline prevention.
- All IDS/IPS alerts are triaged by the SOC within 30 minutes during business hours and within 1 hour outside business hours.
- IDS/IPS events are correlated with other security telemetry in the SIEM for advanced threat detection.

### 7.3 Network Segmentation

BRHI networks are segmented into the following security zones:

| Zone | Description | Security Level |
|---|---|---|
| Cardholder Data Environment (CDE) | POS systems, payment processing | Highest — PCI DSS scoped |
| DMZ | External-facing web servers, email gateways | High |
| Corporate Network | Associate workstations, internal applications | Medium |
| Data Center | Servers, databases, core infrastructure | High |
| Guest WiFi | Customer internet access | Low — fully isolated |
| IoT Network | Smart devices, building management, sensors | Low — fully isolated |
| Management Network | Network and security device management | High — restricted access |
| Development/Test | Non-production development environments | Medium |
| Cloud | Approved cloud environments | Per cloud security policy |

Inter-zone traffic is controlled by firewalls with explicit allow rules. No direct routing exists between the Guest WiFi, IoT, and Corporate networks. All guest traffic is tunneled directly to the internet through a dedicated ISP link.

### 7.4 Wireless Security

- All BRHI corporate wireless networks must use WPA3-Enterprise with 802.1X authentication using RADIUS.
- WPA3-SAE (Simultaneous Authentication of Equals) is used for IoT devices that do not support 802.1X.
- Open (unencrypted) wireless networks are prohibited for any business use.
- Guest WiFi uses a captive portal with terms of service acceptance; guest traffic is fully isolated from all BRHI networks.
- Wireless intrusion detection is deployed to detect rogue access points, unauthorized clients, and wireless attacks.
- All wireless access points must be enterprise-managed and registered in the BRHI asset inventory. Personal or consumer-grade wireless devices are prohibited.
- Bluetooth and other wireless protocols are disabled on POS terminals and payment processing systems.

### 7.5 Virtual Private Network (VPN)

- All remote access to BRHI corporate networks must use the approved VPN solution (currently Palo Alto GlobalProtect).
- VPN connections require MFA authentication before network access is granted.
- Split tunneling is prohibited. All traffic from the remote device must traverse the VPN tunnel to ensure consistent security monitoring and policy enforcement.
- VPN client software must be installed, current, and verified before connection is permitted. Outdated clients are denied connection.
- VPN sessions are logged, monitored, and automatically terminated after 12 hours of continuous use, requiring re-authentication.
- VPN connections from BRHI-managed devices are subject to a posture assessment (current OS patches, active EDR, current antivirus definitions) before full network access is granted.

### 7.6 Zero Trust Architecture Roadmap

BRHI is transitioning to a Zero Trust Architecture aligned with NIST SP 800-207. The following phased roadmap has been established:

- **Phase 1 (2026):** Implement identity-based micro-segmentation for the CDE and data center environments. Deploy certificate-based authentication for all service accounts.
- **Phase 2 (2027):** Extend micro-segmentation to corporate and cloud environments. Implement continuous verification and adaptive access policies based on device posture, user behavior, and risk signals.
- **Phase 3 (2028):** Achieve full Zero Trust maturity with automated policy enforcement, real-time risk scoring, and self-healing network capabilities.

---

## 8. Endpoint Security

### 8.1 Endpoint Detection and Response (EDR)

- All BRHI-managed endpoints (desktops, laptops, servers, POS terminals) must run the approved EDR solution (currently CrowdStrike Falcon).
- EDR agents must be running, active, and reporting to the centralized management console at all times.
- EDR must not be disabled or uninstalled without written CISO approval.
- The SOC monitors EDR alerts 24/7/365 and triages critical alerts within 15 minutes.
- EDR telemetry is integrated with the SIEM for advanced correlation and threat hunting.

### 8.2 Anti-Malware

- All BRHI-managed endpoints must run enterprise anti-malware software with real-time scanning enabled.
- Anti-malware definition updates are deployed automatically every 4 hours from the vendor's cloud update service.
- Daily full-system scans are scheduled for servers; weekly quick scans for workstations.
- On-access (real-time) scanning is mandatory and cannot be disabled by end users.
- Removable media must be scanned automatically upon insertion.
- Anti-malware software must be approved by the Information Security team and listed on the BRHI Approved Software List.

### 8.3 Patch Management

BRHI maintains a structured patch management program to address vulnerabilities in a timely manner:

| Severity | Definition | Patching Deadline |
|---|---|---|
| Critical | Actively exploited, remote code execution, or CVSS score 9.0+ | 72 hours from patch availability |
| High | Significant security impact or CVSS score 7.0-8.9 | 14 calendar days |
| Medium | Moderate security impact or CVSS score 4.0-6.9 | 30 calendar days |
| Low | Limited security impact or CVSS score 0.1-3.9 | 90 calendar days (next scheduled maintenance window) |

- Emergency patches for zero-day vulnerabilities may be deployed outside the standard change management process with CISO approval and post-implementation review within 5 business days.
- POS systems and PCI-scoped systems follow the same patching timelines but are tested in a staging environment before production deployment.
- Patch compliance is reported weekly to IT management and monthly to the CISO. Systems not patched within the required timeframe are escalated per the Vulnerability Management Escalation Policy.
- End-of-life operating systems and applications that no longer receive security patches are prohibited on the BRHI network.

### 8.4 Mobile Device Management (MDM)

- All mobile devices (smartphones, tablets) that access BRHI corporate data must be enrolled in the BRHI MDM solution (currently Microsoft Intune).
- Corporate-owned devices are configured with the following policies: full-disk encryption, device lock (PIN/biometric, auto-lock after 5 minutes), remote wipe capability, application whitelisting, and containerization of corporate data.
- BYOD devices must be enrolled in the MDM before accessing corporate email or applications. MDM policies on BYOD enforce: device lock, encryption, remote wipe of corporate data only (containerized), and block jailbroken/rooted devices.
- Associate personal data on BYOD devices is not accessed, monitored, or wiped by BRHI MDM.
- Lost or stolen devices must be reported to the IT Service Desk within 4 hours. A remote wipe is initiated within 1 hour of the report.

### 8.5 USB Device Controls

- USB removable storage devices are restricted by endpoint DLP and device control policies.
- Only BRHI-approved and encrypted USB devices (purchased through IT) are whitelisted for use.
- Personal USB storage devices are prohibited from connecting to any BRHI-managed endpoint.
- USB mass storage devices are disabled by default on POS terminals, servers, and systems in the CDE.
- Exceptions require written approval from the Information Security team and must include a documented business justification.

### 8.6 Full-Disk Encryption

- Full-disk encryption is mandatory on all BRHI-managed endpoints: laptops, desktops, and mobile devices.
- Windows devices use BitLocker with TPM 2.0 and a minimum of AES-256 encryption.
- macOS devices use FileVault 2.
- Encryption recovery keys are escrowed in the BRHI key management system and are accessible only to authorized IT Security personnel.
- Compliance with full-disk encryption requirements is verified weekly through automated endpoint compliance reporting.

---

## 9. Application Security

### 9.1 Secure Software Development Life Cycle (SSDLC)

All BRHI software development, whether internal or by contracted vendors, must follow the BRHI SSDLC:

1. **Requirements Phase:** Security requirements are defined alongside functional requirements. Threat modeling is performed using STRIDE methodology. Data classification is assigned to all data elements.
2. **Design Phase:** Security architecture review is conducted. Authentication, authorization, and encryption mechanisms are specified. Security design patterns are applied.
3. **Development Phase:** Developers follow the BRHI Secure Coding Standards. IDE security plugins (e.g., SonarLint) provide real-time feedback. Pre-commit hooks scan for secrets and sensitive data.
4. **Testing Phase:** Static Application Security Testing (SAST) is integrated into the CI/CD pipeline. Dynamic Application Security Testing (DAST) is performed against staging environments. Manual penetration testing for high-risk applications.
5. **Deployment Phase:** Security configuration review is completed. Infrastructure-as-Code templates are scanned for misconfigurations. Deployment approval requires security sign-off.
6. **Maintenance Phase:** Ongoing vulnerability scanning, dependency monitoring, and security patch management.

### 9.2 OWASP Top 10 Awareness

All BRHI developers and QA engineers must complete annual training on the OWASP Top 10 security risks. The current OWASP Top 10 (2021 edition) includes:

1. Broken Access Control
2. Cryptographic Failures
3. Injection
4. Insecure Design
5. Security Misconfiguration
6. Vulnerable and Outdated Components
7. Identification and Authentication Failures
8. Software and Data Integrity Failures
9. Security Logging and Monitoring Failures
10. Server-Side Request Forgery (SSRF)

Applications must be assessed against each OWASP Top 10 category during development and testing phases.

### 9.3 Code Review Requirements

- All code changes must be reviewed by at least one peer before merging into any release branch.
- Changes to security-sensitive modules (authentication, authorization, encryption, payment processing, PII handling) require review by a member of the Application Security team.
- Automated code quality and security analysis (SAST) must pass with zero critical or high findings before merge is permitted.
- Open-source dependencies are reviewed against the National Vulnerability Database (NVD) and BRHI-approved component list using Software Composition Analysis (SCA) tools.
- Code review findings must be documented and tracked to resolution in the BRHI application lifecycle management (ALM) system.

### 9.4 Application Vulnerability Scanning

- **Static Application Security Testing (SAST):** Integrated into the CI/CD pipeline and executed on every code commit. SAST scans must produce zero critical or high findings before code promotion.
- **Dynamic Application Security Testing (DAST):** Executed weekly against all internet-facing applications and prior to every production release. DAST scans must produce zero critical findings and no more than 3 medium findings before release.
- **Software Composition Analysis (SCA):** Executed daily to identify vulnerable open-source libraries and dependencies. Critical CVEs in dependencies must be patched within 7 days.
- All vulnerability findings are tracked in the BRHI vulnerability management system with defined owners, remediation timelines, and status tracking.

### 9.5 API Security Standards

- All APIs (internal and external) must require authentication using OAuth 2.0 with short-lived access tokens (maximum 1-hour expiration) and refresh tokens.
- API rate limiting is enforced to prevent abuse: 1,000 requests per minute per authenticated client for standard APIs; 10,000 requests per minute for internal service-to-service APIs.
- API input validation must be performed on all parameters; input must be validated against a strict schema.
- API responses must not expose stack traces, internal error messages, or system details.
- All external-facing APIs must be protected by a Web Application Firewall (WAF) with OWASP Core Rule Set (CRS) enabled.
- API documentation must follow the OpenAPI Specification (OAS) 3.0 standard and include security requirements.
- API keys must be rotated every 90 days and must not be embedded in source code.

---

## 10. Cloud Security

### 10.1 Cloud Security Posture Management (CSPM)

- BRHI deploys a CSPM solution across all cloud environments to continuously monitor for security misconfigurations, compliance violations, and policy drift.
- CSPM policies are aligned with CIS Benchmarks for each cloud provider and BRHI-specific security policies.
- Critical CSPM findings must be remediated within 72 hours; high findings within 14 days.
- CSPM dashboards are reviewed weekly by Cloud Security Engineering and monthly by the CISO.

### 10.2 Approved Cloud Providers

Only the following cloud service providers are approved for BRHI workloads:

| Provider | Approved Services | Approved Workloads |
|---|---|---|
| Microsoft Azure | Compute, Storage, SQL, AD, Sentinel | Enterprise applications, ERP, identity |
| Amazon Web Services (AWS) | EC2, S3, RDS, Lambda, CloudFront | E-commerce, data analytics, DevOps |
| Google Cloud Platform (GCP) | BigQuery, Cloud Storage | Data analytics, machine learning |
| Oracle Cloud Infrastructure (OCI) | Compute, Storage, Database, Fusion Apps | Oracle Fusion Cloud ERP, HCM, SCM, EPM |
| Salesforce | CRM, Service Cloud | Customer relationship management |
| Microsoft 365 | Exchange Online, SharePoint, Teams | Email, collaboration, productivity |

Use of any cloud service not on the approved list requires a security review and approval from the Information Security team before procurement.

### 10.3 Shared Responsibility Model

BRHI documents and maintains a Shared Responsibility Matrix for each approved cloud provider, clearly delineating which security controls are the responsibility of the cloud provider and which are the responsibility of BRHI. Key responsibilities:

- **Cloud Provider:** Physical security of data centers, infrastructure (servers, storage, networking), hypervisor security, global network infrastructure.
- **BRHI:** Identity and access management, data classification and encryption, application security, operating system patching (IaaS), network configuration, compliance validation, security monitoring and incident response.

The Shared Responsibility Matrix is reviewed annually and updated when new services are adopted.

### 10.4 Cloud Access Security Broker (CASB)

- BRHI deploys a CASB solution to provide visibility and control over cloud service usage.
- CASB enforces policies including: data encryption requirements, access control policies, DLP scanning, shadow IT discovery, and user activity monitoring.
- All sanctioned SaaS applications are configured through the CASB with enterprise single sign-on (SSO) and conditional access policies.
- CASB alerts for unsanctioned cloud service usage are triaged by the SOC within 4 hours.

### 10.5 Oracle Fusion Cloud ERP Security Requirements

As BRHI's enterprise platform, Oracle Fusion Cloud ERP requires specific security controls and configurations to protect sensitive financial, employee, and customer data.

#### 10.5.1 Access Control Requirements

1. **Role-Based Access Control (RBAC)**
   - All users must be assigned roles based on job functions
   - Minimum necessary access principle enforced
   - Quarterly access reviews required for all Oracle users
   - Segregation of Duties (SoD) conflicts must be identified and remediated

2. **Multi-Factor Authentication (MFA)**
   - Required for all Oracle Fusion Cloud ERP access
   - Hardware token or authenticator app required for administrative access
   - Session timeout: 30 minutes for standard users, 15 minutes for administrators

3. **Privileged Access Management**
   - Administrative access requires Just-In-Time (JIT) provisioning
   - All administrative actions logged and monitored
   - Break-glass procedures documented for emergency access

#### 10.5.2 Data Protection Requirements

1. **Encryption Standards**
   - All sensitive data encrypted at rest using AES-256
   - All data encrypted in transit using TLS 1.2 or higher
   - Oracle Transparent Data Encryption (TDE) for database encryption
   - Oracle Key Vault for centralized key management

2. **Data Classification**
   - All data in Oracle Fusion must be classified according to BRHI data classification policy
   - Restricted data requires additional access controls and monitoring
   - Data masking required for non-production environments

3. **Data Loss Prevention**
   - DLP policies enforced for Oracle Fusion Cloud ERP
   - Monitoring for bulk data exports
   - Alerting on unusual data access patterns

#### 10.5.3 Monitoring and Audit Requirements

1. **Audit Logging**
   - All user logins and logouts logged
   - All data changes logged with before/after values
   - All administrative actions logged
   - Logs retained for 7 years

2. **Continuous Monitoring**
   - Real-time monitoring of security events
   - Integration with Security Information and Event Management (SIEM)
   - Automated alerting on suspicious activities

3. **Compliance Reporting**
   - Monthly security compliance reports
   - Quarterly access certification campaigns
   - Annual SOX control assessment

#### 10.5.4 Oracle Cloud Infrastructure (OCI) Security

1. **Identity and Access Management**
   - Oracle Cloud IAM integrated with BRHI identity provider
   - Federated authentication using SAML 2.0 or OIDC
   - Conditional access policies based on device, location, and risk

2. **Network Security**
   - Virtual Cloud Network (VCN) with security lists
   - Network segmentation for different environments
   - VPN connectivity for administrative access

3. **Infrastructure Security**
   - Regular vulnerability assessments
   - Compliance with Oracle Cloud security benchmarks
   - Shared responsibility model documented and followed

#### 10.5.5 Integration Security

1. **API Security**
   - OAuth 2.0 with JWT tokens for API authentication
   - API rate limiting and throttling
   - API gateway for centralized security management

2. **Integration Monitoring**
   - Real-time monitoring of all integrations
   - Alerting on integration failures
   - Regular security testing of integration points

---

## 11. Incident Response

### 11.1 Incident Classification

BRHI classifies security incidents into four severity levels:

| Severity | Definition | Examples |
|---|---|---|
| Severity 1 (Critical) | Imminent or active threat to critical systems, large-scale data breach, or significant business disruption | Active ransomware, confirmed breach of payment card data, compromise of domain controllers, widespread service outage caused by attack |
| Severity 2 (High) | Significant security event with potential for substantial impact if not contained promptly | Compromised privileged account, malware on PCI-scoped system, targeted phishing attack with confirmed credential compromise, unauthorized access to Confidential data |
| Severity 3 (Medium) | Security event with moderate potential impact that requires investigation and remediation | Malware on non-critical endpoint, policy violation with security implications, unsuccessful targeted attack, vulnerability exploitation attempt detected by IPS |
| Severity 4 (Low) | Minor security event or policy violation with limited impact | Single phishing email (no compromise), minor policy violation, false positive investigation, low-risk vulnerability discovery |

### 11.2 Response Times

| Severity | Initial Response | Containment Target | Resolution Target |
|---|---|---|---|
| Severity 1 (Critical) | 15 minutes | 4 hours | 24 hours |
| Severity 2 (High) | 1 hour | 8 hours | 72 hours |
| Severity 3 (Medium) | 4 hours | 24 hours | 5 business days |
| Severity 4 (Low) | 24 hours | 5 business days | 10 business days |

Initial response includes acknowledgment, preliminary triage, and activation of the appropriate response procedures.

### 11.3 Incident Response Team

The BRHI Incident Response Team (IRT) includes the following roles:

| Role | Responsible Party | Responsibilities |
|---|---|---|
| Incident Commander | CISO or designee | Overall incident management, executive communication, strategic decisions |
| Technical Lead | Senior SOC Analyst or Security Engineer | Technical investigation, evidence collection, containment and eradication |
| Communications Lead | Director of Corporate Communications | Internal and external communications, media relations |
| Legal Counsel | General Counsel or designee | Legal obligations, regulatory notifications, law enforcement coordination |
| Privacy Officer | VP of Privacy and Compliance | Data privacy impact assessment, regulatory notification requirements |
| IT Operations Lead | Director of IT Operations | System recovery, business continuity coordination |
| Business Unit Liaison | Affected business unit director | Business impact assessment, operational decisions |
| HR Representative | HR Director (for insider threats) | Associate-related investigations, workforce notifications |
| Public Relations | VP of Marketing | Customer communications, brand management |
| External Forensics | Retained third-party forensics firm | Independent forensic investigation, evidence preservation |

The IRT is activated for all Severity 1 and Severity 2 incidents. Severity 3 and 4 incidents are managed by the SOC with escalation to the IRT as needed.

### 11.4 Communication Plan

#### Internal Notification

- **Severity 1:** CISO notifies CEO, CFO, General Counsel, and the Board of Directors (via Board Audit Committee Chair) within 1 hour of incident confirmation. All IRT members are notified within 30 minutes.
- **Severity 2:** CISO notifies VP of IT, General Counsel, and affected business unit VP within 2 hours. IRT members notified within 1 hour.
- **Severity 3 and 4:** SOC notifies CISO and affected system owners within 4 hours.

#### External Notification

External notification is coordinated by Legal Counsel and Communications and follows these requirements:

- **Regulatory notification:** State breach notification laws require notification to affected individuals within the timeframe mandated by the most restrictive applicable state law (currently 30 days for states with defined timelines). Notification to state attorneys general as required.
- **Payment card brands:** Visa and Mastercard must be notified within 24 hours of a confirmed breach involving cardholder data.
- **Federal regulators:** Notification to the FTC as required by the FTC Health Breach Notification Rule or other applicable federal regulations.
- **Law enforcement:** Engagement of law enforcement (FBI, Secret Service) at the direction of General Counsel.
- **Customers:** Customer notification letters are sent via first-class mail and email (where available) within the regulatory timeframe. Notification includes: description of the incident, types of data involved, steps taken, steps customers can take, and contact information for a dedicated incident response call center.
- **Media:** All media inquiries are handled exclusively by the Communications Lead. No other IRT member or BRHI associate is authorized to speak to the media about the incident.

### 11.5 Post-Incident Review

A post-incident review (lessons learned) must be conducted within 5 business days of incident closure for all Severity 1 and Severity 2 incidents, and within 10 business days for Severity 3 incidents. The review must include:

- Timeline reconstruction of the incident from detection to resolution
- Root cause analysis using a structured methodology (e.g., 5 Whys, fishbone diagram)
- Effectiveness of detection, response, and communication
- Identification of gaps in controls, processes, or training
- Specific corrective actions with owners and deadlines (not to exceed 30 days for implementation)
- Update to the Incident Response Plan if procedural improvements are identified

Post-incident review reports are classified as Restricted and distributed to the CISO, IRT members, and the Board Audit Committee (for Severity 1 incidents).

### 11.6 Forensic Investigation Procedures

- Forensic images of affected systems must be captured using forensically sound tools (e.g., FTK Imager, dd with appropriate flags) within 4 hours of Severity 1 incident declaration.
- A chain of custody form must be maintained for all forensic evidence, documenting: item description, serial number, who collected it, date/time of collection, storage location, and every transfer.
- Forensic analysis must be performed on copies of forensic images, never on original evidence.
- For Severity 1 incidents, BRHI engages the pre-retained external forensics firm (currently Mandiant) to conduct or assist with the forensic investigation.
- Forensic evidence is retained for a minimum of 7 years or as directed by Legal Counsel.
- All forensic activities must comply with BRHI legal hold obligations and be documented in the forensic case management system.

### 11.7 Legal and Regulatory Notification Requirements

BRHI maintains a current matrix of breach notification requirements by jurisdiction. Key requirements include:

- **All U.S. states and territories:** All 50 states, D.C., and territories have breach notification laws. Notification timelines range from 30 to 90 days. BRHI targets notification within 30 days to meet the most restrictive requirements.
- **California (CCPA/CPRA):** Notification to the California Attorney General if more than 500 California residents are affected. Annual reporting of breaches affecting California residents.
- **New York:** Notification to the NY Attorney General, Department of State, and Division of State Police. SHIELD Act requirements for reasonable security safeguards.
- **Payment card brands:** Visa, Mastercard, American Express, and Discover must be notified per their respective data breach response procedures.
- **SEC:** If BRHI determines a cybersecurity incident is material, it must be reported on Form 8-K within 4 business days of the materiality determination (per SEC cybersecurity disclosure rules).
- **FTC:** Notification as required under applicable FTC regulations.

The Privacy Officer, in consultation with General Counsel, determines applicable notification requirements for each incident.

---

## 12. Business Continuity and Disaster Recovery

### 12.1 Recovery Objectives

BRHI has defined Recovery Time Objectives (RTO) and Recovery Point Objectives (RPO) for critical business systems:

| System | RTO | RPO | Priority Tier |
|---|---|---|---|
| POS Systems (Retail) | 4 hours | 1 hour | Tier 1 |
| E-commerce Platform | 1 hour | 15 minutes | Tier 1 |
| Payment Processing | 2 hours | 15 minutes | Tier 1 |
| Enterprise Resource Planning (ERP) | 8 hours | 4 hours | Tier 1 |
| Email (Microsoft 365) | 4 hours | 1 hour | Tier 2 |
| Supply Chain Management | 8 hours | 4 hours | Tier 2 |
| Customer Relationship Management | 12 hours | 4 hours | Tier 2 |
| Human Resources (Workday) | 24 hours | 8 hours | Tier 3 |
| Data Warehouse / Analytics | 24 hours | 12 hours | Tier 3 |
| Development Environments | 48 hours | 24 hours | Tier 4 |

### 12.2 Backup Strategy

BRHI follows the 3-2-1 backup rule:

- **3** copies of all data (production + 2 backups)
- **2** different storage media (disk and tape or cloud)
- **1** copy stored offsite (geographically separated minimum 100 miles)

Backup schedule:

| Backup Type | Frequency | Retention | Scope |
|---|---|---|---|
| Incremental | Daily (every 24 hours) | 30 days | All Tier 1 and Tier 2 systems |
| Differential | Daily (every 12 hours) | 14 days | Tier 1 systems only |
| Full | Weekly (Sunday) | 13 months (rolling) | All production systems |
| Monthly Full | Monthly (1st of month) | 7 years | Financial and compliance systems |
| Real-time replication | Continuous | Per RPO | POS transaction logs, e-commerce databases |

Backup integrity is verified through:

- Automated daily backup verification checks (checksum validation)
- Monthly test restores of randomly selected backup sets
- Quarterly full DR testing (see Section 12.4)

All backups are encrypted using AES-256 before leaving the production environment. Backup encryption keys are stored separately from backup media in the enterprise KMS.

### 12.3 Disaster Recovery Site

- BRHI maintains a **hot standby** disaster recovery site for all Tier 1 critical systems located in Dallas, Texas (primary data center: Atlanta, Georgia).
- The DR site includes: replicated production servers with real-time or near-real-time data replication, pre-configured network infrastructure, and sufficient capacity to handle full production load.
- Tier 2 systems are recovered to the DR site using rebuilt infrastructure from documented configurations and restored from backups.
- The DR site is managed by a contracted colocation provider with SOC 2 Type II certification and 24/7 staffing.
- DR site failover can be initiated by the Director of IT Operations or the CISO. Automated failover is configured for the e-commerce platform and payment processing systems.

### 12.4 Disaster Recovery Testing

- **Quarterly tabletop exercises** are conducted for the IT DR team to walk through failure scenarios and response procedures.
- **Annual full DR failover test** is conducted in January, during which all Tier 1 systems are failed over to the DR site and operated from the DR site for a minimum of 24 hours. The test includes: DR site activation, system failover, operational verification, performance testing, and failback to the primary site.
- **Semi-annual partial DR tests** are conducted focusing on specific systems (e.g., POS failover in Q2, e-commerce failover in Q3).
- DR test results are documented, including: test scope, participants, timeline, success criteria, actual results, identified gaps, and corrective action items.
- Corrective actions from DR tests must be completed before the next scheduled test.
- DR test reports are reviewed by the CISO, CIO, and the Board Audit Committee.

---

## 13. Third-Party Risk Management

### 13.1 Vendor Security Assessment

All third-party vendors who access, process, store, or transmit BRHI data or who provide critical services to BRHI must undergo a security assessment before contract execution:

**Tier 1 — Critical Vendors** (access to Confidential/Restricted data, critical infrastructure, or PCI-scoped systems):
- Complete the BRHI Vendor Security Questionnaire (120+ questions covering governance, access control, encryption, incident response, business continuity, and compliance)
- Provide current SOC 2 Type II report (or SOC 1 Type II for financial processing)
- Undergo an on-site security assessment conducted by BRHI Information Security or a designated third-party assessor
- Provide evidence of PCI DSS compliance (if handling payment card data)
- Provide evidence of cyber insurance (minimum $10M coverage)

**Tier 2 — Significant Vendors** (access to Internal/Confidential data or providing important services):
- Complete the BRHI Vendor Security Questionnaire
- Provide current SOC 2 Type II or ISO 27001 certification
- Provide evidence of cyber insurance (minimum $5M coverage)

**Tier 3 — Standard Vendors** (limited access to Internal data):
- Complete an abbreviated Vendor Security Questionnaire (40 questions)
- Self-attestation of security controls

### 13.2 Contractual Security Requirements

All contracts with Tier 1 and Tier 2 vendors must include the following security provisions:

- Information security and privacy obligations aligned with BRHI policies
- Data handling requirements matching BRHI data classification standards
- Encryption requirements for BRHI data at rest and in transit
- Incident notification to BRHI within 24 hours of a security incident affecting BRHI data
- Cooperation with BRHI security assessments and audits
- Prohibition on subcontracting BRHI data processing without prior written consent
- Return or secure destruction of BRHI data upon contract termination within 30 days, with certificate of destruction
- Compliance with applicable data protection laws and regulations
- Indemnification for data breaches caused by vendor negligence
- Cyber insurance requirements as defined by tier

### 13.3 Ongoing Monitoring

- **Continuous monitoring:** Tier 1 vendors are monitored continuously using third-party risk rating services (e.g., SecurityScorecard, BitSight). Significant rating declines trigger a review within 5 business days.
- **Annual re-assessment:** All Tier 1 and Tier 2 vendors undergo annual re-assessment, including an updated questionnaire, review of current SOC 2 reports, and verification of continued compliance with contractual security requirements.
- **Event-driven assessments:** Re-assessment is triggered by: vendor merger or acquisition, publicly reported security incident, significant change in vendor service scope, or material change in vendor security posture.
- Vendor risk scores are maintained in the BRHI Third-Party Risk Management (TPRM) platform and reported quarterly to the CISO and the Risk Committee.

### 13.4 Right to Audit

All Tier 1 and Tier 2 vendor contracts include a right-to-audit clause granting BRHI the right to:

- Conduct or commission security assessments, audits, and penetration tests of vendor systems processing BRHI data
- Access vendor facilities where BRHI data is processed or stored
- Review vendor security policies, procedures, and audit reports
- Access vendor security logs and incident records related to BRHI data

BRHI exercises the right to audit at least once every 24 months for Tier 1 vendors and upon reasonable suspicion of a security issue for all vendors. Audit findings must be remediated by the vendor within agreed-upon timelines, not to exceed 90 days for critical findings.

---

## 14. Security Awareness Training

### 14.1 Annual Training

All BRHI associates must complete annual information security awareness training:

- **Duration:** Minimum 60 minutes
- **Format:** Online interactive training module via the BRHI Learning Management System (LMS)
- **Content:** Information security policies, phishing recognition, social engineering tactics, data classification and handling, physical security, incident reporting procedures, acceptable use policy, privacy obligations, and current threat landscape
- **Assessment:** Post-training quiz with a minimum passing score of 80%. Associates who fail may retake the quiz up to 3 times. Continued failure requires completion of instructor-led remedial training.
- **Completion deadline:** All associates must complete annual training within 30 days of its release. New hires must complete training within 30 days of their start date.

Training completion is tracked by the Information Security team. Non-compliance is escalated as follows:

- 7 days past due: Automated reminder to associate and direct manager
- 14 days past due: Escalation to department director
- 21 days past due: Escalation to VP and HR Business Partner
- 30 days past due: Access restrictions may be applied (e.g., removal of remote access privileges)

### 14.2 Phishing Simulation

- Monthly phishing simulations are conducted by the Information Security team using the approved phishing simulation platform.
- Simulations range in difficulty from basic (obvious phishing indicators) to advanced (sophisticated, targeted campaigns mimicking real-world threats).
- Associates who click on simulated phishing links or enter credentials are automatically enrolled in a 15-minute remedial training module, which must be completed within 48 hours.
- Associates who repeatedly fail simulations (3 or more failures within a 12-month period) are required to complete an in-person coaching session with the Information Security team.
- Department-level phishing simulation results are reported monthly to department heads and quarterly to the CISO. Organization-wide click rates are tracked and targeted for improvement.

### 14.3 Role-Specific Training

In addition to general awareness training, role-specific security training is required for:

| Role | Training Content | Frequency | Duration |
|---|---|---|---|
| Software Developers | OWASP Top 10, SSDLC, secure coding practices, SAST/DAST tools | Annual | 4 hours |
| System Administrators | Privileged access management, hardening standards, incident response, forensics basics | Annual | 4 hours |
| Database Administrators | Database security, encryption, activity monitoring, data masking | Annual | 3 hours |
| IT Security Team | Advanced threat detection, incident response, forensics, cloud security, penetration testing | Annual | 16 hours (plus ongoing) |
| Executives and Board Members | Strategic cybersecurity risks, governance, regulatory landscape, incident response roles | Annual | 2 hours |
| Associates Handling PII | Data privacy, CCPA/CPRA requirements, data handling procedures, breach notification | Annual | 2 hours |
| POS System Operators | Payment card security, skimming detection, physical security of terminals | Annual | 1 hour |
| Third-Party Vendors | BRHI security requirements, data handling procedures, incident reporting | Upon onboarding and annually | 1 hour |

### 14.4 Training Records

- All training completions are recorded in the BRHI LMS and maintained for a minimum of 5 years.
- Training records include: associate name, employee ID, training title, completion date, and assessment score.
- Training completion metrics are reported monthly to the CISO and quarterly to the Board Audit Committee.

---

## 15. Privacy and Data Protection

### 15.1 CCPA/CPRA Compliance

BRHI is committed to full compliance with the California Consumer Privacy Act (CCPA) as amended by the California Privacy Rights Act (CPRA), and extends these protections to all customers nationwide as a matter of policy. BRHI:

- Publishes a clear and comprehensive Privacy Notice on its website and in-store, describing: categories of personal information collected, purposes of collection, categories of third parties with whom data is shared, and consumer rights.
- Maintains a publicly accessible Privacy Policy reviewed and updated at least annually.
- Does not sell personal information. BRHI has not sold and does not sell consumer personal information to third parties.
- Limits the use of sensitive personal information to the purposes for which it was collected or as otherwise permitted by law.
- Provides a clear and conspicuous "Do Not Sell or Share My Personal Information" link on its website, even though BRHI does not engage in these practices.
- Maintains records of consumer requests and responses for a minimum of 24 months.

### 15.2 Privacy Notice for Customers and Associates

BRHI maintains separate privacy notices for customers and associates:

**Customer Privacy Notice** covers:
- Categories of personal information collected (identifiers, commercial information, internet activity, geolocation, inferences)
- Purposes of collection (order fulfillment, customer service, marketing, analytics, fraud prevention, legal compliance)
- Categories of third parties with whom data is shared (service providers, payment processors, analytics providers, law enforcement as required)
- Consumer rights (access, deletion, correction, portability, opt-out, non-discrimination)
- How to exercise rights (toll-free number: 1-800-BRHI-PRV, online form, in-store)
- Data retention practices
- Contact information for the Privacy Officer

**Associate Privacy Notice** covers:
- Categories of personal information collected from associates and applicants
- Purposes of collection (employment administration, benefits, payroll, compliance, security)
- Associate rights under applicable state and federal law
- Monitoring of associate activity on company systems (as described in the Acceptable Use Policy)
- Data security measures protecting associate information

### 15.3 Data Subject Rights

BRHI recognizes and facilitates the following data subject rights for customers and associates:

| Right | Description | Response Time |
|---|---|---|
| Right to Know / Access | Individuals may request a copy of the personal information BRHI has collected about them in the past 12 months | 45 calendar days (extendable by 45 days with notice) |
| Right to Delete | Individuals may request deletion of their personal information, subject to legal exceptions | 45 calendar days |
| Right to Correct | Individuals may request correction of inaccurate personal information | 45 calendar days |
| Right to Data Portability | Individuals may request their data in a portable, machine-readable format (CSV or JSON) | 45 calendar days |
| Right to Opt-Out | Individuals may opt out of the sale or sharing of their personal information (not applicable as BRHI does not sell data) | 15 calendar days |
| Right to Non-Discrimination | BRHI will not discriminate against individuals for exercising their privacy rights | N/A |
| Right to Limit Use of Sensitive PI | Individuals may request that BRHI limit the use of sensitive personal information to what is necessary to perform the services or provide the goods reasonably expected | 45 calendar days |

**Request Handling Process:**

1. Requests are received via the BRHI Privacy Portal (privacy.buildright.com), toll-free number (1-800-BRHI-PRV), email (privacy@buildright.com), or in-store.
2. Identity verification is performed before processing any request. Verification methods include: matching account information, email verification, or, for high-risk requests, identity document verification.
3. Authorized requests are forwarded to the Privacy Operations team within 2 business days.
4. The Privacy Operations team coordinates with relevant business units and IT to fulfill the request.
5. The individual is notified of the outcome within the required timeframe.
6. All requests and responses are logged in the BRHI Privacy Request Management System.

### 15.4 Data Processing Agreements (DPA)

All vendors and service providers who process personal information on behalf of BRHI must execute a Data Processing Agreement that includes:

- Description and purpose of data processing
- Categories of personal information processed
- Duration of processing
- Obligations of the service provider (confidentiality, security measures, sub-processing restrictions)
- Data subject rights assistance obligations
- Breach notification requirements (within 24 hours of discovery)
- Data return and destruction obligations upon termination
- Audit rights and cooperation obligations
- Compliance with applicable privacy laws

DPAs are reviewed and approved by the Privacy Officer and General Counsel before execution.

### 15.5 Privacy Impact Assessments (PIA)

A Privacy Impact Assessment must be completed before:

- Implementing any new system or application that collects, processes, or stores personal information
- Materially changing how personal information is collected, used, or shared in an existing system
- Sharing personal information with a new third party or for a new purpose
- Implementing new surveillance or monitoring technologies
- Launching new marketing programs that use personal information
- Deploying new biometric or location-tracking technologies

The PIA process includes:

1. Description of the data collection, use, and sharing practices
2. Identification of legal basis for processing
3. Assessment of privacy risks to individuals
4. Evaluation of necessity and proportionality
5. Identification of mitigating controls
6. Determination of whether additional consent or notification is required
7. Approval by the Privacy Officer before proceeding

PIA documentation is maintained for the lifetime of the system plus 3 years.

### 15.6 Cross-Border Data Transfer Controls

- BRHI primarily operates within the United States and stores personal information in U.S.-based data centers and cloud regions.
- Transfer of personal information outside the United States requires prior approval from the Privacy Officer and must be based on a valid legal mechanism (e.g., Standard Contractual Clauses, adequacy decision).
- A list of countries where BRHI personal information may be processed is maintained by the Privacy Officer and reviewed quarterly.
- Cloud storage regions are configured to ensure personal information remains within approved jurisdictions. Cloud storage bucket policies and CSPM rules enforce geographic restrictions.
- Cross-border transfers are logged and auditable.

### 15.7 Biometric Data Policy

BRHI may collect biometric data only for specific, documented business purposes and in compliance with applicable state biometric information privacy laws (e.g., Illinois BIPA, Texas CUBI, Washington biometric law):

- **Fingerprint scanners:** Used for time and attendance systems in select distribution centers. Associates are informed and provide written consent before enrollment. Alternative methods are available for associates who decline.
- **Facial recognition:** Not currently deployed. Any future deployment requires completion of a PIA, legal review of applicable state laws, executive approval, and public disclosure.
- **Voice authentication:** Used for select customer service IVR systems. Customers are informed and can opt out.

Biometric data handling requirements:

- Biometric templates (not raw biometric data) are stored in encrypted form using AES-256.
- Biometric data is stored separately from other personal information.
- Biometric data must be deleted within 30 days of the purpose being fulfilled or within the timeframe required by applicable state law, whichever is shorter.
- Biometric data is never sold, shared, or disclosed except as required by law.
- A publicly available biometric data retention schedule is maintained.

---

## 16. Compliance and Audit

### 16.1 Annual Security Audit Program

BRHI conducts a comprehensive annual security audit program that includes:

- **Internal audit:** The BRHI Internal Audit department conducts an independent assessment of the information security program, including policy compliance, control effectiveness, and risk management. Results are reported to the Board Audit Committee.
- **External audit:** An independent external audit firm conducts an annual assessment of IT general controls (ITGCs) and security posture. The external audit program is coordinated with the internal audit program to ensure comprehensive coverage.
- **Audit findings tracking:** All audit findings are categorized by severity (Critical, High, Medium, Low), assigned to responsible owners, and tracked to remediation in the BRHI GRC system. Critical findings must be remediated within 30 days; High findings within 60 days; Medium findings within 90 days; Low findings within 180 days.

### 16.2 SOX IT General Controls Testing

As a publicly traded company, BRHI is subject to Sarbanes-Oxley Act (SOX) requirements. IT General Controls are tested annually in coordination with the external auditor:

- **Access controls:** User provisioning, deprovisioning, and access review processes for all in-scope financial applications
- **Change management:** Application change controls, including development, testing, approval, and implementation processes
- **IT operations:** Job scheduling, backup and recovery, incident management, and problem management processes for in-scope systems
- **Program development:** System development lifecycle controls for new systems and significant modifications to in-scope financial applications

SOX ITGC testing is coordinated by the SOX Compliance Manager in collaboration with Internal Audit and the external auditor. Deficiencies are reported to management and the Board Audit Committee.

### 16.3 SOC 1/SOC 2 Type II Reports

- BRHI engages an independent audit firm to produce annual SOC 1 Type II and SOC 2 Type II reports covering all in-scope systems and services.
- **SOC 1 Type II:** Covers controls relevant to financial reporting for services provided to customers and business partners.
- **SOC 2 Type II:** Covers controls across all Trust Service Criteria (Security, Availability, Processing Integrity, Confidentiality, Privacy) for BRHI's technology operations.
- SOC reports are made available to customers and business partners under NDA through the BRHI Trust Portal.
- SOC report findings and management responses are tracked in the GRC system and remediated according to the timelines specified in the audit findings policy.

### 16.4 Penetration Testing

BRHI conducts penetration testing on the following schedule:

| Type | Frequency | Scope | Performed By |
|---|---|---|---|
| External network penetration test | Annual | All external-facing IP ranges, internet-facing applications | Independent third-party firm (rotated every 2 years) |
| Internal network penetration test | Semi-annual | Internal network, including attempts to breach network segmentation | BRHI Red Team or approved third-party firm |
| Application penetration test | Per release (major) and annual | Internet-facing applications, mobile applications, APIs | Approved third-party firm or BRHI Application Security team |
| Wireless penetration test | Annual | All BRHI facilities with wireless networks | Approved third-party firm |
| Social engineering assessment | Annual | Phishing, vishing, and physical social engineering | Approved third-party firm |

Penetration testing rules of engagement are documented and approved by the CISO before each engagement. Testing is conducted during approved windows to minimize business disruption. All findings are classified, documented, and remediated within the timelines established in the Vulnerability Management Policy.

### 16.5 Continuous Monitoring and SIEM

- BRHI operates a Security Information and Event Management (SIEM) platform (currently Microsoft Sentinel) that aggregates and correlates security telemetry from all critical systems, networks, and endpoints.
- Log sources include: firewalls, IDS/IPS, EDR, DLP, Active Directory, VPN, CASB, cloud platforms, application logs, database audit logs, and physical access systems.
- The SOC monitors SIEM alerts 24/7/365. Alert response times follow the incident classification timelines in Section 11.2.
- Use cases for advanced threat detection are developed and tuned continuously by the Threat Detection Engineering team. A minimum of 12 new or updated detection use cases are deployed quarterly.
- Threat intelligence feeds from multiple sources (industry ISACs, commercial feeds, government advisories) are integrated into the SIEM for automated detection of indicators of compromise (IOCs).
- SIEM logs are retained online for 90 days and in archive for 3 years.
- A monthly SIEM health check ensures log sources are reporting, correlation rules are firing, and alert volumes are within expected ranges. Gaps in log coverage are remediated within 14 days.

---

## 17. Acceptable Use Policy

### 17.1 General Principles

BRHI information systems, networks, and devices are provided for legitimate business purposes. All use of BRHI technology resources is subject to monitoring and auditing. Associates have no expectation of privacy when using BRHI-owned systems, networks, or devices.

### 17.2 Authorized Use

BRHI information systems may be used for:

- Performance of assigned job duties and responsibilities
- BRHI-approved education, training, and professional development
- Limited personal use that does not interfere with work performance, consume excessive resources, or violate any BRHI policy

### 17.3 Prohibited Activities

The following activities are strictly prohibited:

- Accessing, creating, downloading, storing, or distributing content that is illegal, offensive, discriminatory, harassing, or pornographic
- Installing unauthorized software, browser extensions, or applications on BRHI devices
- Circumventing or attempting to circumvent security controls, including firewalls, antivirus, DLP, and access controls
- Sharing BRHI login credentials, MFA tokens, or access badges with anyone
- Using BRHI systems to operate a personal business or engage in activities for personal financial gain (excluding approved BRHI business)
- Connecting personal network equipment (routers, switches, access points) to BRHI networks without IT approval
- Downloading or transmitting BRHI Confidential or Restricted data to personal devices, personal email, or unapproved cloud services
- Using BRHI email for mass unsolicited communications (spam)
- Attempting to access systems, data, or networks without authorization, including scanning or probing BRHI networks
- Engaging in any form of hacking, cracking, or exploitation of systems
- Recording meetings or conversations without proper authorization and consent
- Using BRHI resources for political activities or campaigns
- Disabling, interfering with, or obstructing security software, logging, or monitoring tools

### 17.4 Email and Communications

- BRHI email accounts are provided for business communication. Associates must use BRHI email for all business-related correspondence.
- Associates must not auto-forward BRHI email to personal email accounts.
- Attachments containing Confidential or Restricted data must be encrypted before sending to external recipients.
- Associates must verify the identity of email senders before clicking links, opening attachments, or providing sensitive information. Suspicious emails must be reported to the SOC using the Report Phishing button or by forwarding to phishing@buildright.com.
- Instant messaging and collaboration tools approved by BRHI (currently Microsoft Teams) may be used for business communication. Content shared through these tools is subject to the same classification and handling rules as email.

### 17.5 Remote Work

- Associates working remotely must use BRHI-managed devices or approved BYOD devices enrolled in MDM.
- Remote access must use the BRHI VPN. Split tunneling is prohibited.
- Associates must ensure their home network uses WPA2 or WPA3 encryption and a strong, unique password.
- Confidential or Restricted information must not be displayed or discussed in public places where it may be overheard or observed by unauthorized persons.
- Associates must not store BRHI Confidential or Restricted data on personal devices or personal cloud storage.
- Remote workers must ensure their physical workspace is secure when stepping away (lock screen, secure documents).

### 17.6 Physical Security

- Associates must wear their BRHI identification badge at all times while on BRHI premises.
- Associates must not hold doors open for unknown individuals (tailgating prevention). Visitors must be signed in and escorted at all times.
- Associates must lock their workstations (Ctrl+Alt+Delete, Lock) when leaving them unattended, even briefly.
- Confidential or Restricted paper documents must be stored in locked cabinets and disposed of in designated shredding bins.
- Associates must report lost or stolen badges, devices, or keys to the IT Service Desk and Security Operations immediately.

### 17.7 Social Media

- Associates must not disclose BRHI Confidential or Restricted information on social media platforms.
- Associates who identify themselves as BRHI employees on social media must include a disclaimer that their views are their own and not those of BRHI.
- Associates must not post photographs of BRHI internal facilities, data centers, security equipment, or POS systems without authorization from Corporate Communications.
- Social media accounts used for BRHI business purposes must be authorized by Corporate Communications and managed according to the BRHI Social Media Policy.

---

## 18. Policy Enforcement

### 18.1 Violations

Violations of this policy are categorized as follows:

| Category | Description | Examples |
|---|---|---|
| Minor | Unintentional, first-time violation with no actual security impact | Failure to lock workstation, delayed completion of security training |
| Moderate | Violation with potential security impact or repeated minor violations | Sharing passwords, storing Confidential data on unapproved systems, disabling security software |
| Severe | Violation with actual or significant potential security impact | Unauthorized access to systems, intentional circumvention of security controls, loss of unencrypted Restricted data |
| Gross | Intentional violation resulting in significant harm, or criminal activity | Theft of data, deliberate sabotage, fraud, sale of BRHI data |

### 18.2 Consequences

Violations will be addressed through a progressive discipline process, taking into account the severity of the violation, the associate's role and access level, prior violations, and whether the violation was intentional:

| Category | Potential Consequences |
|---|---|
| Minor | Verbal counseling, documented warning, mandatory remedial training |
| Moderate | Written warning, temporary access restriction, mandatory remedial training, performance improvement plan |
| Severe | Suspension, demotion, termination, civil legal action |
| Gross | Immediate termination, criminal prosecution referral, civil legal action |

### 18.3 Reporting Violations

Associates are required and expected to report suspected policy violations or security concerns through any of the following channels:

- Direct manager or supervisor
- Information Security team: security@buildright.com
- IT Service Desk: 1-800-BRHI-HELP (x4357)
- BRHI Ethics Hotline: 1-800-BRHI-ETHICS (anonymous reporting available)
- SOC via the Report Phishing button in email

BRHI maintains a strict non-retaliation policy. Associates who report suspected violations in good faith are protected from retaliation, regardless of the outcome of the investigation.

### 18.4 Investigation

All reported violations will be investigated by the Information Security team in coordination with Human Resources and Legal Counsel as appropriate. Investigations will be conducted promptly, impartially, and confidentially to the extent possible. The accused associate will be afforded due process.

### 18.5 Third-Party Violations

Third-party vendors, contractors, and business partners who violate this policy are subject to:

- Immediate suspension of access to BRHI systems pending investigation
- Mandatory remediation of the violation within a specified timeframe
- Contractual remedies as specified in the applicable agreement, including potential contract termination
- Recovery of costs associated with the violation, including investigation and remediation expenses

---

## 19. Policy Governance

### 19.1 Policy Review

This policy is reviewed and updated at least annually by the Information Security team. Reviews may be triggered more frequently by:

- Significant changes in the threat landscape
- Changes in applicable laws or regulations
- Material changes to BRHI's business, technology, or organizational structure
- Findings from security incidents, audits, or risk assessments
- Adoption of new technologies or business practices

### 19.2 Exceptions

Requests for exceptions to this policy must be submitted through the BRHI Policy Exception Request process:

1. Submit a written request to the Information Security team detailing: the specific policy requirement, the reason the requirement cannot be met, the proposed compensating controls, and the duration of the exception.
2. The Information Security team conducts a risk assessment of the exception request.
3. Exceptions are approved by the CISO for standard exceptions. Exceptions involving Restricted data or PCI-scoped systems require additional approval from the Chief Information Officer.
4. All approved exceptions are documented in the GRC system with: risk assessment, compensating controls, expiration date (maximum 12 months), and a plan for compliance.
5. Exceptions are reviewed at least quarterly and must be renewed upon expiration.

### 19.3 Related Documents

This policy should be read in conjunction with the following BRHI policies and standards:

| Document ID | Title |
|---|---|
| BRHI-POL-001 | Code of Business Conduct and Ethics |
| BRHI-POL-002 | Human Resources Policy Manual |
| BRHI-POL-003 | Records Retention Policy |
| BRHI-POL-005 | Incident Response Plan |
| BRHI-POL-006 | Business Continuity Plan |
| BRHI-POL-007 | Vendor Management Policy |
| BRHI-POL-008 | Privacy Policy |
| BRHI-STD-001 | Information Security Standards |
| BRHI-STD-002 | Network Security Standards |
| BRHI-STD-003 | Application Security Standards |
| BRHI-STD-004 | Encryption Standards |
| BRHI-STD-005 | Access Management Standards |
| BRHI-STD-006 | Data Classification Guide |
| BRHI-STD-007 | Secure Coding Guidelines |

### 19.4 Acknowledgment

All BRHI associates are required to acknowledge receipt and understanding of this policy upon hire, annually thereafter, and whenever the policy is materially updated. Acknowledgment is recorded electronically in the BRHI LMS and maintained for the duration of employment plus 5 years.

---

*This document is the property of BuildRight Home Improvement, Inc. Unauthorized reproduction or distribution is prohibited. If you have received this document in error, please notify the BRHI Information Security team immediately at security@buildright.com.*
