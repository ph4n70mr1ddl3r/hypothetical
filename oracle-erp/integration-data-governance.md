# Oracle Fusion Cloud ERP Integration and Data Governance Documentation

## BuildRight Home Improvement, Inc. (BRHI)

---

## 1. Document Control

| Field | Detail |
|---|---|
| **Document ID** | BRHI-DG-001 |
| **Version** | 1.0 |
| **Classification** | Internal — Confidential |
| **Effective Date** | April 2, 2026 |
| **Document Owner** | Chief Technology Officer |
| **Approved By** | Executive Leadership Team |
| **Review Cycle** | Quarterly |
| **Next Review Date** | July 2, 2026 |
| **Distribution** | IT Department, Data Governance Council, Oracle CoE, Business Process Owners |

### Revision History

| Version | Date | Author | Description |
|---|---|---|---|
| 1.0 | April 2, 2026 | Data Governance Team | Initial release — comprehensive integration and data governance guide |

---

## 2. Purpose and Scope

### 2.1 Purpose

This document establishes the integration architecture and data governance framework for Oracle Fusion Cloud ERP at BuildRight Home Improvement, Inc. It provides:

- **Integration Standards**: Standardized approaches for integrating Oracle Fusion with existing systems
- **Data Governance Framework**: Policies and procedures for managing data as a strategic asset
- **Data Quality Standards**: Requirements for maintaining accurate, consistent, and trustworthy data
- **Master Data Management**: Approach for managing critical business entities
- **Data Security and Privacy**: Protections for sensitive data across all systems

### 2.2 Scope

This guide covers:

- All integrations with Oracle Fusion Cloud ERP
- All data domains (financial, customer, product, supplier, employee)
- All business units and geographic regions
- All data lifecycle stages (creation, processing, storage, archival, disposal)
- All integration patterns (real-time, batch, event-driven)

### 2.3 Guiding Principles

1. **Data as an Asset**: Treat data with the same care as financial assets
2. **Single Source of Truth**: Establish authoritative sources for each data domain
3. **Quality by Design**: Build data quality into processes, not just monitor it
4. **Security by Design**: Protect data throughout its lifecycle
5. **Compliance by Design**: Ensure regulatory compliance in all data activities

---

## 3. Integration Architecture

### 3.1 Integration Strategy

BuildRight will use Oracle Integration Cloud (OIC) as the enterprise integration platform, supplemented by specialized tools where appropriate.

**Strategic Principles:**
1. **API-First**: All integrations use REST APIs where available
2. **Event-Driven**: Real-time integrations for critical business events
3. **Batch Processing**: Scheduled batch jobs for non-time-sensitive data
4. **Error Handling**: Comprehensive error handling with retry logic and alerts
5. **Monitoring and Alerting**: Real-time monitoring of all integrations

### 3.2 Integration Patterns

| Pattern | Description | Use Cases | Technology |
|---|---|---|---|
| **Synchronous API** | Real-time request-response | POS transactions, customer lookups | REST API |
| **Asynchronous API** | Real-time with callback | Order processing, complex transactions | REST API + Webhooks |
| **Message Queue** | Event-driven messaging | Inventory updates, price changes | Oracle Streaming |
| **Batch File** | Scheduled file transfer | Bank statements, tax reports | SFTP/FTP |
| **Change Data Capture** | Real-time data synchronization | Master data replication | Oracle GoldenGate |

### 3.3 Integration Landscape

#### 3.3.1 Current Systems to Integrate

| System | Vendor | Function | Integration Priority |
|---|---|---|---|
| **NCR Emerald POS** | NCR | Point of Sale | Critical |
| **Manhattan WMS** | Manhattan Associates | Warehouse Management | Critical |
| **Salesforce Commerce Cloud** | Salesforce | E-commerce | Critical |
| **Vertex Tax Engine** | Vertex | Tax Calculation | Critical |
| **Bank of America** | BofA | Banking Services | Critical |
| **Concur** | SAP | Expense Management | High |
| **Kronos** | Kronos | Time Management | High |
| **ServiceNow** | ServiceNow | IT Service Management | High |
| **Adobe Analytics** | Adobe | Web Analytics | Medium |
| **JDA Planning** | Blue Yonder | Demand Planning | Medium |

#### 3.3.2 Future System Retirements

| System | Replacement | Timeline |
|---|---|---|
| **SAP ERP** | Oracle Fusion Cloud ERP | Phase 1-2 |
| **Legacy HR Platforms** | Oracle HCM Cloud | Phase 1-2 |
| **Custom Reporting DB** | Oracle Analytics Cloud | Phase 2-3 |
| **Spreadsheets** | Oracle EPM Cloud | Phase 2-3 |

### 3.4 Integration Design Standards

#### 3.4.1 API Design Standards

1. **RESTful API Principles**
   - Use standard HTTP methods (GET, POST, PUT, DELETE)
   - Resource-based URLs (/api/v1/customers/{id})
   - JSON payloads with consistent structure
   - Proper HTTP status codes

2. **API Security**
   - OAuth 2.0 with JWT tokens
   - HTTPS for all API calls
   - Rate limiting to prevent abuse
   - IP whitelisting for internal APIs

3. **API Documentation**
   - OpenAPI/Swagger specifications
   - Sample requests and responses
   - Error codes and handling
   - Versioning strategy

#### 3.4.2 Data Mapping Standards

1. **Canonical Data Model**
   - Define canonical formats for each data domain
   - Map source systems to canonical model
   - Map canonical model to target systems

2. **Data Transformation Rules**
   - Document all transformation logic
   - Handle data type conversions
   - Apply business rules during transformation
   - Log transformation errors

3. **Error Handling**
   - Retry logic with exponential backoff
   - Dead letter queue for failed messages
   - Alerting for persistent failures
   - Manual intervention procedures

### 3.5 Integration Patterns by Business Process

#### 3.5.1 Order-to-Cash (O2C)

| Integration Point | Source | Target | Pattern | Frequency |
|---|---|---|---|---|
| **Sales Transaction** | NCR POS | Oracle Financials | Synchronous API | Real-time |
| **Online Order** | Salesforce | Oracle Order Mgmt | Synchronous API | Real-time |
| **Inventory Update** | Oracle SCM | NCR POS | Message Queue | Near real-time |
| **Customer Data** | Salesforce | Oracle CRM | Asynchronous API | Hourly |
| **Payment Processing** | Oracle Financials | Bank of America | Batch File | Daily |

#### 3.5.2 Procure-to-Pay (P2P)

| Integration Point | Source | Target | Pattern | Frequency |
|---|---|---|---|---|
| **Purchase Order** | Oracle Procurement | Supplier Systems | EDI/API | Real-time |
| **Invoice Receipt** | Supplier Systems | Oracle AP | EDI/API | Real-time |
| **Goods Receipt** | Manhattan WMS | Oracle Inventory | Synchronous API | Real-time |
| **Payment Processing** | Oracle AP | Bank of America | Batch File | Daily |
| **Supplier Master** | Oracle Supplier Mgmt | All systems | Message Queue | Real-time |

#### 3.5.3 Hire-to-Retire (H2R)

| Integration Point | Source | Target | Pattern | Frequency |
|---|---|---|---|---|
| **Employee Data** | Oracle HCM | All systems | Message Queue | Real-time |
| **Time Cards** | Kronos | Oracle HCM | Batch File | Daily |
| **Payroll Processing** | Oracle HCM Payroll | Bank of America | Batch File | Per pay period |
| **Benefits Enrollment** | Benefits Platform | Oracle HCM | Asynchronous API | Per event |
| **Learning Records** | Oracle HCM Learning | All systems | Message Queue | Real-time |

### 3.6 Integration Monitoring and Management

#### 3.6.1 Monitoring Dashboard

| Metric | Target | Monitoring Tool | Alert Threshold |
|---|---|---|---|
| **Integration Success Rate** | 99.5% | Oracle Integration Cloud | < 99% |
| **Average Processing Time** | < 5 seconds | Oracle Integration Cloud | > 10 seconds |
| **Queue Depth** | < 1000 messages | Oracle Streaming | > 5000 messages |
| **Error Rate** | < 0.5% | Custom monitoring | > 1% |
| **System Availability** | 99.9% | Infrastructure monitoring | < 99.9% |

#### 3.6.2 Error Management Process

1. **Automated Retry**
   - Transient errors: 3 retries with exponential backoff
   - Permanent errors: Route to dead letter queue
   - Alert sent for persistent failures

2. **Manual Intervention**
   - Dead letter queue reviewed daily
   - Manual retry or correction as needed
   - Root cause analysis for recurring issues

3. **Escalation**
   - Integration failures escalate after 1 hour
   - Business impact assessment required
   - Resolution documented and monitored

---

## 4. Data Governance Framework

### 4.1 Data Governance Organization

#### 4.1.1 Data Governance Council

**Purpose:** Strategic oversight of data governance program

**Members:**
- Chief Data Officer (Chair)
- Chief Technology Officer
- Chief Financial Officer
- Chief Human Resources Officer
- SVP Store Operations
- SVP Pro Business
- VP Information Technology
- VP Legal and Compliance

**Responsibilities:**
- Set data governance strategy and policies
- Approve data governance standards
- Resolve data governance disputes
- Monitor data governance effectiveness
- Allocate resources for data governance initiatives

**Meeting Frequency:** Quarterly

#### 4.1.2 Data Domain Councils

| Domain | Chair | Key Members | Meeting Frequency |
|---|---|---|---|
| **Financial Data** | CFO | Controllers, FP&A, Treasury | Monthly |
| **Customer Data** | SVP Pro Business | Marketing, Sales, Customer Service | Monthly |
| **Product Data** | CMO | Merchandising, Supply Chain, Store Ops | Monthly |
| **Supplier Data** | VP Procurement | Procurement, Quality, Legal | Monthly |
| **Employee Data** | CHRO | HR, Payroll, Benefits, IT | Monthly |

#### 4.1.3 Data Stewardship

**Data Stewards:**
- Subject matter experts for specific data domains
- Responsible for data quality within their domain
- Make decisions about data definitions and standards
- Resolve data quality issues

**Data Custodians:**
- IT professionals responsible for technical data management
- Implement data security and access controls
- Maintain data infrastructure
- Monitor data quality metrics

### 4.2 Data Governance Policies

#### 4.2.1 Data Quality Policy

**Objective:** Ensure data is accurate, complete, timely, and consistent

**Standards:**

| Quality Dimension | Definition | Measurement | Target |
|---|---|---|---|
| **Accuracy** | Data correctly represents real-world entities | Validation rules, audits | 99% |
| **Completeness** | All required data is present | Completeness checks | 98% |
| **Timeliness** | Data is available when needed | Freshness monitoring | 99% |
| **Consistency** | Data is the same across systems | Cross-system validation | 99% |
| **Uniqueness** | No duplicate records | Deduplication rules | 99.5% |

**Quality Management Process:**
1. **Prevention**: Design processes to prevent quality issues
2. **Detection**: Monitor for quality issues
3. **Correction**: Fix quality issues
4. **Monitoring**: Track quality metrics over time

#### 4.2.2 Data Classification Policy

| Classification | Description | Examples | Protection Requirements |
|---|---|---|---|
| **Public** | Information for public distribution | Marketing materials, press releases | Standard protection |
| **Internal** | Information for internal use only | Process docs, training materials | Access control, encryption in transit |
| **Confidential** | Sensitive business information | Financial data, customer data | Encryption at rest and in transit |
| **Restricted** | Highly sensitive information | PII, payment card data | Strong encryption, strict access control |

#### 4.2.3 Data Retention Policy

| Data Type | Retention Period | Disposal Method | Legal Basis |
|---|---|---|---|
| **Financial Records** | 7 years | Secure deletion | SOX, tax requirements |
| **Employee Records** | Employment + 7 years | Secure deletion | Labor laws |
| **Customer Data** | 7 years after last transaction | Secure deletion | Privacy regulations |
| **Audit Logs** | 7 years | Archive then delete | SOX, compliance |
| **System Logs** | 1 year | Automated purge | Security standards |
| **Email Communications** | 3 years | Secure deletion | Legal requirements |

### 4.3 Master Data Management

#### 4.3.1 Master Data Domains

| Domain | Key Entities | Golden Source | Consumers |
|---|---|---|---|
| **Customer** | Customer, Account, Contact | Oracle CRM + Salesforce | All systems |
| **Product** | Item, Category, Brand | Oracle Product Hub | All systems |
| **Supplier** | Supplier, Vendor, Contractor | Oracle Supplier Hub | All systems |
| **Employee** | Worker, Position, Organization | Oracle HCM | All systems |
| **Financial** | Chart of Accounts, Cost Center | Oracle Financials | All systems |
| **Location** | Store, DC, Office | Oracle Location Hub | All systems |

#### 4.3.2 Master Data Governance Process

**1. Data Creation**
- Request submitted through workflow
- Validation against business rules
- Approval by appropriate authority
- Creation in golden source system

**2. Data Modification**
- Change request with justification
- Impact assessment
- Approval by data steward
- Update in golden source system

**3. Data Deletion/Deactivation**
- Deletion request with business case
- Impact analysis
- Legal/compliance review
- Soft delete or archival

**4. Data Quality Monitoring**
- Daily automated quality checks
- Weekly quality reports
- Monthly quality reviews
- Quarterly quality assessments

#### 4.3.3 Master Data Integration Patterns

| Pattern | Description | Use Case | Technology |
|---|---|---|---|
| **Golden Source** | Single authoritative source | Customer, Product | Oracle Integration Cloud |
| **Data Hub** | Central repository for matching | Supplier, Location | Oracle Customer Data Management |
| **Registry** | Reference without consolidation | Product across channels | Custom integration |
| **Coexistence** | Multiple systems, synchronized | Employee across HCM and Payroll | Oracle HCM Integration |

### 4.4 Data Security and Privacy

#### 4.4.1 Data Security Controls

**Access Controls:**
- Role-based access to data
- Attribute-based access control for sensitive data
- Multi-factor authentication for sensitive data access
- Regular access reviews and certifications

**Data Protection:**
- Encryption at rest (AES-256)
- Encryption in transit (TLS 1.2+)
- Data masking for non-production environments
- Tokenization for sensitive data

**Monitoring and Auditing:**
- Real-time monitoring of sensitive data access
- Audit logging of all data changes
- Alerting on suspicious activities
- Regular security assessments

#### 4.4.2 Privacy Compliance

**GDPR Compliance:**
- Data mapping and inventory
- Privacy impact assessments
- Consent management
- Data subject rights processing
- Breach notification procedures

**CCPA Compliance:**
- Consumer rights management
- Opt-out processing
- Data inventory and mapping
- Privacy policy compliance

**Other Regulations:**
- PCI DSS for payment card data
- HIPAA for employee health data (if applicable)
- Industry-specific regulations

### 4.5 Data Analytics and Reporting

#### 4.5.1 Analytics Architecture

| Layer | Technology | Purpose |
|---|---|---|
| **Data Warehouse** | Oracle Autonomous Data Warehouse | Consolidated analytics data |
| **Data Lake** | Oracle Object Storage | Raw data storage |
| **ETL/ELT** | Oracle Data Integrator | Data transformation |
| **BI/Analytics** | Oracle Analytics Cloud | Business intelligence |
| **Advanced Analytics** | Oracle Machine Learning | Predictive analytics |

#### 4.5.2 Reporting Standards

**Report Types:**

| Type | Description | Audience | Frequency |
|---|---|---|---|
| **Operational Reports** | Day-to-day operational metrics | Managers, supervisors | Daily/Weekly |
| **Tactical Reports** | Performance analysis and trends | Directors, VPs | Weekly/Monthly |
| **Strategic Reports** | Executive dashboards, KPIs | C-Suite, Board | Monthly/Quarterly |
| **Ad-hoc Reports** | Custom analysis as needed | Various | As needed |

**Report Development Process:**
1. **Requirements Gathering**: Define business requirements
2. **Data Source Identification**: Identify required data sources
3. **Report Design**: Design report layout and logic
4. **Development**: Build report in Oracle Analytics
5. **Testing**: Validate data accuracy and usability
6. **Deployment**: Publish to appropriate audiences
7. **Maintenance**: Ongoing updates and improvements

---

## 5. Data Quality Management

### 5.1 Data Quality Framework

#### 5.1.1 Data Quality Dimensions

| Dimension | Measurement | Target | Monitoring |
|---|---|---|---|
| **Accuracy** | % of records passing validation rules | 99% | Daily automated checks |
| **Completeness** | % of required fields populated | 98% | Daily automated checks |
| **Consistency** | % of records consistent across systems | 99% | Weekly cross-system validation |
| **Timeliness** | % of records updated within SLA | 99% | Real-time monitoring |
| **Uniqueness** | % of records without duplicates | 99.5% | Weekly deduplication analysis |

#### 5.1.2 Data Quality Rules

**Validation Rules:**
- Format validation (email, phone, address)
- Range validation (dates, amounts)
- Referential integrity (foreign keys)
- Business rule validation (credit limits, tax codes)
- Cross-field validation (start date before end date)

**Cleansing Rules:**
- Standardization (names, addresses)
- Deduplication (fuzzy matching, survivorship)
- Enrichment (third-party data sources)
- Normalization (units, codes)

### 5.2 Data Quality Monitoring

#### 5.2.1 Automated Quality Checks

| Check Type | Frequency | Scope | Action on Failure |
|---|---|---|---|
| **Pre-load Validation** | Real-time | Incoming data | Reject and alert |
| **Post-load Validation** | Daily | Loaded data | Quarantine and alert |
| **Cross-system Validation** | Weekly | Integrated data | Alert and investigate |
| **Master Data Validation** | Daily | Golden sources | Alert and correct |

#### 5.2.2 Quality Dashboard

**Key Metrics:**
- Overall data quality score
- Quality by domain (Customer, Product, etc.)
- Quality by system
- Trend over time
- Top quality issues

**Reporting:**
- Daily quality summary to data stewards
- Weekly quality report to domain councils
- Monthly quality dashboard to Data Governance Council
- Quarterly quality assessment to Executive Leadership

### 5.3 Data Quality Improvement

#### 5.3.1 Improvement Process

1. **Issue Identification**
   - Automated detection
   - User reports
   - Audit findings
   - Business process analysis

2. **Root Cause Analysis**
   - Process analysis
   - System analysis
   - People analysis
   - Policy analysis

3. **Solution Design**
   - Process improvements
   - System enhancements
   - Training and awareness
   - Policy updates

4. **Implementation**
   - Solution deployment
   - Monitoring effectiveness
   - Adjust as needed
   - Document changes

#### 5.3.2 Continuous Improvement

**Monthly Reviews:**
- Review quality metrics
- Identify improvement opportunities
- Prioritize improvement initiatives
- Track progress on initiatives

**Quarterly Assessments:**
- Comprehensive quality assessment
- Benchmark against industry standards
- Strategic improvement planning
- Resource allocation for improvements

---

## 6. Integration and Data Governance Operations

### 6.1 Operational Procedures

#### 6.1.1 Daily Operations

| Task | Responsible | Frequency | Duration |
|---|---|---|---|
| **Integration Monitoring** | Integration Team | Continuous | 8 hours |
| **Data Quality Checks** | Data Stewards | Daily | 2 hours |
| **Error Resolution** | Integration Team | As needed | Variable |
| **Daily Status Report** | Integration Lead | Daily | 30 minutes |

#### 6.1.2 Weekly Operations

| Task | Responsible | Frequency | Duration |
|---|---|---|---|
| **Quality Metrics Review** | Data Stewards | Weekly | 2 hours |
| **Integration Performance Review** | Integration Lead | Weekly | 1 hour |
| **Master Data Reconciliation** | Data Custodians | Weekly | 4 hours |
| **Weekly Operations Report** | Integration Lead | Weekly | 1 hour |

#### 6.1.3 Monthly Operations

| Task | Responsible | Frequency | Duration |
|---|---|---|---|
| **Data Quality Assessment** | Data Governance Team | Monthly | 8 hours |
| **Integration Health Check** | Integration Team | Monthly | 4 hours |
| **Security Access Review** | Security Team | Monthly | 8 hours |
| **Monthly Governance Report** | Data Governance Lead | Monthly | 4 hours |

### 6.2 Incident Management

#### 6.2.1 Integration Incidents

**Severity Levels:**

| Severity | Description | Response Time | Resolution Time |
|---|---|---|---|
| **Critical** | Business-critical integration down | 15 minutes | 4 hours |
| **High** | Major integration impaired | 1 hour | 8 hours |
| **Medium** | Minor integration issue | 4 hours | 24 hours |
| **Low** | Cosmetic or enhancement request | 24 hours | 72 hours |

**Incident Process:**
1. **Detection**: Automated monitoring or user report
2. **Triage**: Assess severity and impact
3. **Investigation**: Identify root cause
4. **Resolution**: Implement fix
5. **Communication**: Update stakeholders
6. **Closure**: Document and close

#### 6.2.2 Data Quality Incidents

**Incident Types:**
- Data validation failures
- Duplicate records
- Inconsistent data across systems
- Missing required data
- Data security breaches

**Response Process:**
1. **Identification**: Automated or manual detection
2. **Assessment**: Evaluate impact and urgency
3. **Containment**: Prevent further issues
4. **Correction**: Fix the data
5. **Prevention**: Implement controls to prevent recurrence
6. **Documentation**: Record incident and resolution

### 6.3 Change Management

#### 6.3.1 Integration Changes

**Change Types:**

| Type | Description | Approval Required | Testing Required |
|---|---|---|---|
| **Emergency** | Critical fix for production issue | CTO or designee | Minimal |
| **Standard** | Planned enhancement or fix | Integration Lead | Full regression |
| **Major** | Significant architectural change | Steering Committee | Full testing cycle |

**Change Process:**
1. **Request**: Submit change request with details
2. **Assessment**: Evaluate impact and risk
3. **Approval**: Obtain required approvals
4. **Implementation**: Deploy during maintenance window
5. **Verification**: Validate successful deployment
6. **Documentation**: Update integration documentation

#### 6.3.2 Data Model Changes

**Change Types:**
- New data fields
- Modified data structures
- Changed business rules
- New data domains

**Change Process:**
1. **Impact Analysis**: Assess downstream impacts
2. **Design**: Design data model changes
3. **Development**: Implement changes
4. **Testing**: Test with sample data
5. **Deployment**: Deploy to production
6. **Communication**: Notify stakeholders

---

## 7. Metrics and Reporting

### 7.1 Integration Metrics

| Metric | Target | Current | Trend |
|---|---|---|---|
| **Integration Success Rate** | 99.5% | TBD | TBD |
| **Average Processing Time** | < 5 seconds | TBD | TBD |
| **Error Rate** | < 0.5% | TBD | TBD |
| **System Availability** | 99.9% | TBD | TBD |
| **Incident Resolution Time** | < 4 hours | TBD | TBD |

### 7.2 Data Quality Metrics

| Metric | Target | Current | Trend |
|---|---|---|---|
| **Overall Quality Score** | 98% | TBD | TBD |
| **Duplicate Rate** | < 0.5% | TBD | TBD |
| **Completeness Rate** | 98% | TBD | TBD |
| **Accuracy Rate** | 99% | TBD | TBD |
| **Timeliness Rate** | 99% | TBD | TBD |

### 7.3 Governance Metrics

| Metric | Target | Current | Trend |
|---|---|---|---|
| **Data Steward Coverage** | 100% | TBD | TBD |
| **Policy Compliance** | 95% | TBD | TBD |
| **Quality Initiative Completion** | 90% | TBD | TBD |
| **Stakeholder Satisfaction** | 4.0/5.0 | TBD | TBD |

---

## 8. Appendices

### Appendix A: Integration Specifications

**API Specifications:**
- Oracle Financials API Specification
- Salesforce Commerce API Specification
- NCR POS Integration Specification
- Manhattan WMS Integration Specification
- Vertex Tax Integration Specification

**Data Mapping Documents:**
- Customer Data Mapping
- Product Data Mapping
- Supplier Data Mapping
- Employee Data Mapping
- Financial Data Mapping

### Appendix B: Data Quality Rules

**Customer Data Quality Rules:**
- Email format validation
- Phone number format validation
- Address standardization
- Duplicate detection rules

**Product Data Quality Rules:**
- SKU format validation
- Category hierarchy validation
- Price range validation
- Inventory accuracy rules

### Appendix C: Glossary of Terms

| Term | Definition |
|---|---|
| **OIC** | Oracle Integration Cloud |
| **EDI** | Electronic Data Interchange |
| **API** | Application Programming Interface |
| **ETL** | Extract, Transform, Load |
| **ELT** | Extract, Load, Transform |
| **MDM** | Master Data Management |
| **DQ** | Data Quality |
| **DQC** | Data Quality Control |
| **PII** | Personally Identifiable Information |
| **PCI DSS** | Payment Card Industry Data Security Standard |

### Appendix D: Contact Information

| Role | Name | Email | Phone |
|---|---|---|---|
| **Data Governance Lead** | [To be appointed] | data-governance@buildright.com | 404-555-0401 |
| **Integration Architect** | [To be appointed] | integration-team@buildright.com | 404-555-0402 |
| **Data Quality Manager** | [To be appointed] | data-quality@buildright.com | 404-555-0403 |
| **Master Data Manager** | [To be appointed] | master-data@buildright.com | 404-555-0404 |

---

*This document is the property of BuildRight Home Improvement, Inc. and is intended for internal use by authorized associates. Unauthorized distribution, reproduction, or disclosure is prohibited. For questions regarding this document, contact the Data Governance Team at data-governance@buildright.com or extension 4-0005.*