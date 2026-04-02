# Oracle Fusion Cloud ERP Implementation and Operations Guide

## BuildRight Home Improvement, Inc. (BRHI)

---

## 1. Document Control

| Field | Detail |
|---|---|
| **Document ID** | BRHI-TECH-001 |
| **Version** | 1.1 |
| **Classification** | Internal — Confidential |
| **Effective Date** | April 2, 2026 |
| **Document Owner** | Chief Technology Officer |
| **Approved By** | Executive Leadership Team |
| **Review Cycle** | Quarterly during implementation; Annual post-go-live |
| **Next Review Date** | July 1, 2026 |
| **Distribution** | Executive Leadership Team, IT Department, Business Process Owners, Oracle CoE Team |

### Revision History

| Version | Date | Author | Description |
|---|---|---|---|
| 1.1 | April 2, 2026 | Enterprise Technology Team | Added AI and Agentic Finance capabilities section |
| 1.0 | April 2, 2026 | Enterprise Technology Team | Initial release — comprehensive implementation guide |

---

## 2. Purpose and Scope

### 2.1 Purpose

This document serves as the authoritative guide for implementing, operating, and optimizing Oracle Fusion Cloud ERP across BuildRight Home Improvement, Inc. It provides:

- **Implementation Roadmap**: Detailed phases, milestones, and deliverables for the enterprise-wide deployment
- **Module Configuration Standards**: Standardized approaches for configuring Oracle modules to meet BuildRight's business requirements
- **Integration Architecture**: Technical specifications for integrating Oracle Fusion with existing systems
- **Operational Procedures**: Day-to-day operational guidance for system administrators, business users, and support teams
- **Optimization Roadmap**: Continuous improvement initiatives to maximize ROI from the Oracle investment

### 2.2 Scope

This guide covers:

- All Oracle Fusion Cloud ERP modules selected for BuildRight deployment
- Integration with existing retail systems (POS, WMS, e-commerce)
- Multi-entity considerations (U.S., Canada, México operations)
- All business units and functional areas
- All 2,312 store locations and 93 distribution facilities
- All 503,000 associates across North America

### 2.3 Guiding Principles

1. **Standardization First**: Configure once, use everywhere. Avoid customization unless absolutely necessary.
2. **Cloud-Native Approach**: Leverage Oracle's quarterly updates and new features rather than building custom solutions.
3. **Business-Led, IT-Supported**: Business process owners drive requirements; IT provides technical expertise.
4. **Phased Value Delivery**: Deliver business value incrementally rather than attempting a "big bang" go-live.
5. **Change Management Investment**: Allocate 15% of project budget to training, communication, and change management.

---

## 3. Implementation Roadmap

### 3.1 Phase 1: Foundation (FY2026)

#### 3.1.1 Oracle Financials Cloud

**Objective:** Establish the financial backbone of the organization with real-time visibility into financial performance across all entities.

**Key Modules:**
- General Ledger (GL)
- Accounts Payable (AP)
- Accounts Receivable (AR)
- Cash Management (CM)
- Fixed Assets (FA)
- Tax Management

**Configuration Highlights for BuildRight:**

| Configuration Area | BuildRight Requirement | Oracle Solution |
|---|---|---|
| **Chart of Accounts** | Multi-segment structure supporting 2,312 stores, 6 business units, 3 countries | 8-segment COA: Company, Business Unit, Department, Account, Product, Channel, Region, Project |
| **Legal Entities** | 6 legal entities across U.S., Canada, México | Legal entity hierarchy with intercompany accounting automation |
| **Ledgers** | US GAAP (primary), IFRS (Canada), Mexican NIIF (México) | Primary ledger per entity with secondary ledgers for alternate accounting standards |
| **Calendar** | Fiscal year Feb 1 - Jan 31, 13 periods (4-4-5 retail calendar) | Custom accounting calendar with retail-specific period structure |
| **Currencies** | USD (primary), CAD, MXN | Multi-currency ledgers with automated revaluation and translation |

**Key Integrations:**
- NCR Emerald POS → Oracle Financials (daily sales journal)
- Bank of America → Oracle Cash Management (automated reconciliation)
- Vertex Tax Engine → Oracle Tax (sales tax calculation)
- Concur → Oracle Expenses (employee expense management)

#### 3.1.2 Oracle Procurement Cloud

**Objective:** Streamline procurement processes across all locations, capturing $50M+ in annual savings through AI-powered spend analytics.

**Key Modules:**
- Purchasing
- Sourcing
- Supplier Management
- Contract Management
- Self-Service Procurement

**Configuration Highlights for BuildRight:**

| Configuration Area | BuildRight Requirement | Oracle Solution |
|---|---|---|
| **Procurement Organizations** | Separate structures for Store, DC, and Corporate procurement | Multi-org setup with role-based access and approval hierarchies |
| **Catalog Management** | 30,000+ items per store; 1.2M+ SKUs online | Punch-out catalogs integrated with supplier systems; internal catalog for indirect spend |
| **Approval Workflows** | Tiered approval based on amount and category | Configurable approval hierarchies (Store Manager → District → Regional → VP) |
| **Supplier Portal** | 10,000+ global suppliers | Supplier self-service portal for PO management, invoice submission, and payment status |
| **Spend Analytics** | AI-powered classification and savings identification | Embedded Oracle AI for spend classification and opportunity identification |

**Key Integration Points:**
- Existing vendor EDI feeds → Oracle Procurement
- Supplier diversity database → Oracle Supplier Management
- Contract repository → Oracle Contract Management

#### 3.1.3 Oracle Human Capital Management Cloud - Phase 1

**Objective:** Unify HR processes for 503,000 associates with modern, mobile-first experiences.

**Key Modules:**
- Core HR
- Payroll (U.S., Canada, México)
- Absence Management
- Position Management

**Configuration Highlights for BuildRight:**

| Configuration Area | BuildRight Requirement | Oracle Solution |
|---|---|---|
| **Worker Types** | Full-time, part-time, seasonal, temporary, contractor | Flexible worker model with lifecycle management |
| **Pay Groups** | Multiple pay frequencies across entities | Configurable pay groups by country and employment type |
| **Position Hierarchy** | 2,312 store positions plus corporate roles | Position-based staffing model with reporting hierarchy |
| **Absence Plans** | Vacation, sick, personal, bereavement, volunteer | Country-specific absence plans with accrual rules |
| **Union Contracts** | Multiple collective bargaining agreements | Contract tracking with compliance monitoring |

**Key Integrations:**
- Kronos Timekeeping → Oracle HCM (time card data)
- ADP Payroll (legacy) → Oracle HCM Payroll (migration path)
- Benefits platforms → Oracle HCM (benefits enrollment)
- Learning Management System → Oracle HCM Learning (Phase 2)

---

### 3.2 Phase 2: Expansion (FY2027)

#### 3.2.1 Oracle Supply Chain Management Cloud

**Objective:** Achieve end-to-end supply chain visibility from vendor to store shelf to customer doorstep.

**Key Modules:**
- Inventory Management
- Order Management
- Logistics
- Product Lifecycle Management

#### 3.2.2 Oracle Enterprise Performance Management Cloud

**Objective:** Transform financial planning and analysis with driver-based planning and real-time consolidation.

**Key Modules:**
- Financial Consolidation and Close
- Account Reconciliation
- Planning and Budgeting
- Profitability and Cost Management

#### 3.2.3 Oracle Human Capital Management Cloud - Phase 2

**Objective:** Complete the HCM transformation with talent management, learning, and workforce management.

**Key Modules:**
- Talent Management
- Learning Management
- Workforce Management
- Compensation Management

#### 3.2.4 Oracle Risk Management Cloud

**Objective:** Embed continuous controls monitoring and SOX compliance into daily operations.

**Key Modules:**
- Financial Reporting Compliance
- Access Certification
- Continuous Control Monitoring
- Advanced Access Controls

---

### 3.3 Phase 3: Optimization (FY2028)

#### 3.3.1 Oracle Customer Experience Cloud

**Objective:** Unify customer interactions across all channels for a seamless omnichannel experience.

**Key Modules:**
- Oracle Sales Cloud
- Oracle Service Cloud
- Oracle Marketing Cloud

#### 3.3.2 Advanced Analytics and AI

**Objective:** Leverage embedded AI and analytics across all modules for predictive insights.

**Key Capabilities:**
- Predictive demand forecasting
- Dynamic pricing optimization
- Customer lifetime value analytics
- Workforce planning analytics

---

## 4. Integration Architecture

### 4.1 Integration Strategy

BuildRight will use Oracle Integration Cloud (OIC) as the enterprise integration platform, with the following principles:

1. **API-First**: All integrations use REST APIs where available
2. **Event-Driven**: Real-time integrations for critical business events
3. **Batch Processing**: Scheduled batch jobs for non-time-sensitive data
4. **Error Handling**: Comprehensive error handling with retry logic and alerts

### 4.2 Key Integrations

| Source System | Target Oracle Module | Integration Type | Frequency |
|---|---|---|---|
| NCR Emerald POS | Oracle Financials | API (REST) | Real-time |
| Manhattan WMS | Oracle SCM | EDI/API | Near real-time |
| Salesforce Commerce | Oracle Order Management | API (REST) | Real-time |
| Bank of America | Oracle Cash Management | SFTP/API | Daily |
| Vertex Tax | Oracle Tax | API (REST) | Real-time |
| Concur | Oracle Expenses | API (REST) | Batch |
| Kronos | Oracle HCM | API (SOAP) | Daily |
| ServiceNow | Oracle Risk Management | API (REST) | Real-time |

### 4.3 Data Migration Strategy

**Legacy Systems to Retire:**
- SAP ERP (Financials, Procurement)
- Legacy HR platforms (multiple)
- Custom reporting databases
- Spreadsheets and manual processes

**Migration Approach:**
1. **Data Cleansing**: Cleanse master data before migration
2. **Parallel Run**: Run legacy and Oracle in parallel for 30-60 days
3. **Cutover Plan**: Detailed cutover plan with rollback procedures
4. **Validation**: Automated data validation checks

---

## 5. Security and Access Control

### 5.1 Security Model

Oracle Fusion Cloud ERP uses a role-based access control (RBAC) model:

**Role Types:**
- **Job Roles**: Based on job functions (e.g., Store Manager, AP Clerk)
- **Duty Roles**: Functional permissions (e.g., Invoice Processing)
- **Privileges**: Specific actions (e.g., Create Invoice)

**Key Security Policies:**
1. **Segregation of Duties (SoD)**: Enforced via Oracle Risk Management Cloud
2. **Sensitive Data**: Encrypted at rest and in transit
3. **Multi-Factor Authentication**: Required for all administrative access
4. **Session Management**: Automatic timeout after 30 minutes of inactivity

### 5.2 Access Request Process

1. User submits access request via Oracle Self-Service Portal
2. Manager approves request
3. SoD check performed automatically
4. Security administrator provisions access
5. User receives notification with training requirements

---

## 6. Change Management and Training

### 6.1 Change Management Strategy

**Organizational Change Management (OCM) Team:**
- OCM Lead (dedicated role)
- Change Champions (25 regional leads)
- Training Coordinators (10 district-level)

**Communication Plan:**
- Monthly Oracle Fusion newsletter
- Quarterly town halls with executive updates
- Weekly "Tip of the Week" for store associates
- Dedicated intranet portal for Oracle information

### 6.2 Training Program

**Training Tiers:**

| Tier | Audience | Training Method | Duration |
|---|---|---|---|
| **Tier 1** | Executive Leadership | Instructor-led workshops | 2 days |
| **Tier 2** | Business Process Owners | Instructor-led + hands-on labs | 5 days |
| **Tier 3** | Power Users | Virtual instructor-led | 3 days |
| **Tier 4** | End Users | eLearning + microlearning | 4-8 hours |
| **Tier 5** | Store Associates | Mobile microlearning | 1-2 hours |

**Oracle Learning Resources:**
- Oracle University courses
- Oracle Help Center documentation
- Internal knowledge base with BuildRight-specific scenarios
- Video library with step-by-step guides

---

## 7. Governance and Support

### 7.1 Governance Structure

**Executive Steering Committee:**
- Chair: Chief Financial Officer
- Members: CTO, COO, CHRO, SVP Operations, SVP Pro Business, VP IT
- Frequency: Monthly

**Program Management Office (PMO):**
- Director, Oracle Program Management
- 4 Project Managers (one per workstream)
- 2 Business Analysts
- 1 Change Management Lead

**Center of Excellence (CoE):**
- Oracle Financials Lead
- Oracle Procurement Lead
- Oracle SCM Lead
- Oracle HCM Lead
- Integration Architect
- Security Administrator
- Reporting/Analytics Specialist

### 7.2 Support Model

**Tiered Support:**

| Level | Team | Scope | Response Time |
|---|---|---|---|
| **Tier 0** | Self-Service | Knowledge base, FAQs, chatbot | Immediate |
| **Tier 1** | Help Desk | Initial triage, basic troubleshooting | 15 minutes |
| **Tier 2** | Business Support | Functional issues, process questions | 2 hours |
| **Tier 3** | Oracle CoE | Technical issues, configuration changes | 4 hours |
| **Tier 4** | Oracle ACS | Product bugs, enhancement requests | Next business day |

**Escalation Matrix:**
1. Help Desk → Business Support (if unresolved in 30 minutes)
2. Business Support → Oracle CoE (if unresolved in 4 hours)
3. Oracle CoE → Oracle Support (if product bug confirmed)
4. Critical issues → Executive Steering Committee notification

---

## 8. Performance and Optimization

### 8.1 Key Performance Indicators (KPIs)

| KPI | Target | Measurement Frequency |
|---|---|---|
| **System Availability** | 99.9% | Monthly |
| **User Adoption Rate** | 95% within 6 months | Monthly |
| **Invoice Processing Time** | < 3 days (from 7 days) | Weekly |
| **Period-End Close Time** | 5 days (from 15 days) | Monthly |
| **Procurement Cycle Time** | < 7 days | Weekly |
| **Employee Self-Service Usage** | 80% | Monthly |
| **System Response Time** | < 2 seconds | Daily |
| **Training Completion Rate** | 100% | Monthly |

### 8.2 Continuous Improvement Process

1. **Monthly Optimization Reviews**: Review KPIs and identify improvement opportunities
2. **Quarterly Feature Adoption**: Evaluate new Oracle features for adoption
3. **Annual Business Process Review**: Assess process efficiency and optimization
4. **User Feedback Loop**: Regular surveys and focus groups for user input

---

## 9. Risk Management

### 9.1 Implementation Risks

| Risk | Likelihood | Impact | Mitigation |
|---|---|---|---|
| **Scope Creep** | High | High | Strict change control process; clear requirements freeze |
| **Resource Constraints** | Medium | High | Dedicated resources; backfill plan for key personnel |
| **Integration Complexity** | High | Medium | Phased integration approach; early prototyping |
| **User Resistance** | Medium | High | Robust change management; executive sponsorship |
| **Data Quality Issues** | Medium | High | Data cleansing initiative before migration |
| **Vendor Dependencies** | Low | Medium | SLA with Oracle; backup support options |

### 9.2 Operational Risks (Post-Go-Live)

| Risk | Mitigation |
|---|---|
| **System Downtime** | Oracle's 99.9% SLA; disaster recovery plan |
| **Security Breach** | Role-based access; encryption; monitoring |
| **Process Non-Compliance** | Continuous controls monitoring; regular audits |
| **Skill Gaps** | Ongoing training; knowledge base; Oracle support |
| **Quarterly Updates** | Test environment; opt-in process; regression testing |

---

## 10. AI and Agentic Finance Capabilities

### 10.1 Oracle's Agentic Finance Vision

Oracle Fusion Cloud ERP 2026 introduces a paradigm shift with "Agentic Finance" - over 50+ role-based AI agents embedded directly into the Fusion platform. Unlike simple chatbots, these agents can autonomously identify anomalies in general ledgers, recommend supply chain pivots during disruptions, and automate complex close processes without human intervention.

### 10.2 Key AI Agents for BuildRight

| AI Agent | Business Function | Key Capabilities | Implementation Phase |
|---|---|---|---|
| **Ledger Agent** | General Ledger | AI-powered anomaly detection, automated journal entries, intelligent reconciliation | Phase 1 (FY2026) |
| **Payables Agent** | Accounts Payable | Invoice ingestion automation, compliance monitoring, supplier validation | Phase 1 (FY2026) |
| **Payments Agent** | Treasury | Payment optimization, fraud detection, cash flow forecasting | Phase 1 (FY2026) |
| **Expenses Agent** | Employee Expenses | Touchless expense completion, policy compliance, receipt matching | Phase 1 (FY2026) |
| **Procurement Agent** | Purchasing | Intelligent sourcing, spend analytics, contract optimization | Phase 2 (FY2027) |
| **Inventory Agent** | Supply Chain | Demand forecasting, stock optimization, replenishment automation | Phase 2 (FY2027) |
| **Risk Agent** | Compliance | Business process risk analysis, security briefings, access recommendations | Phase 2 (FY2027) |
| **HCM Agent** | Human Resources | Talent acquisition, employee engagement, workforce planning | Phase 2 (FY2027) |

### 10.3 AI-Powered Business Process Enhancements

#### 10.3.1 Financial Close Automation
- **Autonomous Close**: AI agents can autonomously perform 80%+ of period-end close tasks
- **Anomaly Detection**: Real-time identification of unusual transactions and variances
- **Predictive Reconciliation**: AI suggests reconciliation entries based on historical patterns
- **Target**: Reduce period-end close from 15 days to 3 days

#### 10.3.2 Intelligent Procurement
- **Spend Classification**: AI automatically classifies spend across 10,000+ suppliers
- **Savings Identification**: AI identifies $50M+ in annual savings opportunities
- **Supplier Risk Monitoring**: Real-time assessment of supplier financial health and performance
- **Contract Optimization**: AI suggests contract terms based on market benchmarks

#### 10.3.3 Supply Chain Intelligence
- **Demand Forecasting**: Machine learning models predict demand with 95%+ accuracy
- **Inventory Optimization**: AI balances service levels with carrying costs
- **Disruption Response**: AI agents recommend supply chain pivots during disruptions
- **Logistics Optimization**: AI optimizes delivery routes and warehouse operations

#### 10.3.4 Human Capital Intelligence
- **Talent Acquisition**: AI screens candidates and predicts success factors
- **Employee Engagement**: AI analyzes sentiment and recommends interventions
- **Workforce Planning**: Predictive models for staffing needs based on seasonality
- **Learning Recommendations**: AI personalizes training based on role and performance

### 10.4 AI Governance and Ethics

#### 10.4.1 Responsible AI Principles
1. **Transparency**: AI decisions are explainable and auditable
2. **Fairness**: AI models are tested for bias and discrimination
3. **Privacy**: AI respects data privacy and consent requirements
4. **Human Oversight**: Critical decisions maintain human-in-the-loop controls
5. **Accountability**: Clear ownership for AI outcomes and decisions

#### 10.4.2 AI Risk Management
- **Model Validation**: All AI models validated before deployment
- **Performance Monitoring**: Continuous monitoring of AI model performance
- **Bias Testing**: Regular testing for algorithmic bias
- **Explainability Requirements**: AI decisions must be explainable to auditors

### 10.5 Implementation Roadmap for AI

#### Phase 1 (FY2026): Foundation
- Deploy Ledger, Payables, Payments, and Expenses AI agents
- Establish AI governance framework
- Train users on AI agent interactions
- Monitor AI performance and accuracy

#### Phase 2 (FY2027): Expansion
- Deploy Procurement, Inventory, Risk, and HCM AI agents
- Implement predictive analytics across modules
- Expand AI automation to additional business processes
- Refine AI models based on usage patterns

#### Phase 3 (FY2028): Optimization
- Full integration of AI across all modules
- Advanced predictive and prescriptive analytics
- AI-driven continuous improvement processes
- Industry-leading AI capabilities

### 10.6 Success Metrics for AI Implementation

| Metric | Target | Current | Owner |
|---|---|---|---|
| **AI Adoption Rate** | 80% of eligible users | TBD | Change Management |
| **Automation Rate** | 70% of routine tasks | TBD | Process Owners |
| **Accuracy Rate** | 95%+ for AI recommendations | TBD | Quality Team |
| **Time Savings** | 40% reduction in manual work | TBD | Business Units |
| **Cost Savings** | $25M+ annually from AI optimizations | TBD | Finance |

---

## 11. Appendices

### Appendix A: Glossary of Terms

| Term | Definition |
|---|---|
| **O2C** | Order-to-Cash |
| **P2P** | Procure-to-Pay |
| **R2R** | Record-to-Report |
| **SoD** | Segregation of Duties |
| **SOX** | Sarbanes-Oxley Act |
| **ASC 606** | Revenue Recognition Standard |
| **BOPIS** | Buy Online, Pick Up In-Store |
| **BODFS** | Buy Online, Deliver from Store |
| **OIC** | Oracle Integration Cloud |
| **OCI** | Oracle Cloud Infrastructure |
| **EPM** | Enterprise Performance Management |
| **HCM** | Human Capital Management |
| **SCM** | Supply Chain Management |
| **CX** | Customer Experience |
| **CoE** | Center of Excellence |
| **PMO** | Program Management Office |

### Appendix B: Oracle Module Mapping to Business Processes

| Business Process | Primary Oracle Module | Supporting Modules |
|---|---|---|
| **Order-to-Cash** | Oracle Financials (AR), Oracle SCM (Order Management) | Oracle CX, Oracle Risk Management |
| **Procure-to-Pay** | Oracle Procurement, Oracle Financials (AP) | Oracle SCM, Oracle Risk Management |
| **Record-to-Report** | Oracle Financials (GL), Oracle EPM | Oracle Risk Management |
| **Hire-to-Retire** | Oracle HCM | Oracle Financials (Payroll) |
| **Plan-to-Produce** | Oracle SCM, Oracle EPM | Oracle Financials |
| **Lead-to-Cash** | Oracle CX, Oracle Financials | Oracle SCM |

### Appendix C: Contact Information

| Role | Name | Email | Phone |
|---|---|---|---|
| **Executive Sponsor** | Thomas R. Johansson, CFO | t.johansson@buildright.com | 404-555-0101 |
| **Program Director** | [To be appointed] | oracle-program@buildright.com | 404-555-0202 |
| **IT Help Desk** | [Service Desk] | helpdesk@buildright.com | 1-800-BUILD-IT |
| **Oracle ACS Support** | [Oracle Account Team] | oracle-support@buildright.com | 1-800-ORACLE |

---

*This document is the property of BuildRight Home Improvement, Inc. and is intended for internal use by authorized associates. Unauthorized distribution, reproduction, or disclosure is prohibited. For questions regarding this document, contact the Enterprise Technology Team at oracle-program@buildright.com or extension 4-0002.*