# Oracle Fusion Cloud ERP Module Mapping Reference

## BuildRight Home Improvement, Inc. (BRHI)

---

## 1. Document Control

| Field | Detail |
|---|---|
| **Document ID** | BRHI-TECH-002 |
| **Version** | 1.0 |
| **Classification** | Internal — Confidential |
| **Effective Date** | April 2, 2026 |
| **Document Owner** | Chief Technology Officer |
| **Approved By** | Executive Leadership Team |
| **Review Cycle** | Quarterly during implementation; Annual post-go-live |
| **Next Review Date** | July 2, 2026 |

### Revision History

| Version | Date | Author | Description |
|---|---|---|---|
| 1.0 | April 2, 2026 | Enterprise Technology Team | Initial release — Oracle module mapping reference |

---

## 2. Purpose

This document provides a comprehensive mapping of Oracle Fusion Cloud ERP modules to:
- Previous SAP modules being replaced
- Business functions at BuildRight
- Key business processes
- Integration points with other systems

This mapping serves as a reference for all documentation updates and system configuration decisions.

---

## 3. SAP to Oracle Module Mapping

### 3.1 Financial Modules

| SAP Module | Oracle Module | Description |
|---|---|---|
| **SAP FI-GL** | Oracle Financials Cloud - General Ledger | Central accounting and financial reporting |
| **SAP FI-AP** | Oracle Financials Cloud - Accounts Payable | Vendor invoice processing and payments |
| **SAP FI-AR** | Oracle Financials Cloud - Accounts Receivable | Customer billing and collections |
| **SAP FI-AA** | Oracle Financials Cloud - Fixed Assets | Asset management and depreciation |
| **SAP FI-CO** | Oracle Financials Cloud - Cash Management | Cash flow management and bank reconciliation |
| **SAP FI-TX** | Oracle Financials Cloud - Tax Management | Tax calculation and compliance |
| **SAP FI-SL** | Oracle Financials Cloud - Subledger Accounting | Detailed subledger accounting rules |
| **SAP FI-EC** | Oracle Financials Cloud - Intercompany | Intercompany accounting and eliminations |

### 3.2 Procurement Modules

| SAP Module | Oracle Module | Description |
|---|---|---|
| **SAP MM-PUR** | Oracle Procurement Cloud - Purchasing | Purchase requisitions and purchase orders |
| **SAP MM-SRV** | Oracle Procurement Cloud - Sourcing | Supplier sourcing and negotiations |
| **SAP MM-SRM** | Oracle Procurement Cloud - Supplier Management | Supplier onboarding and performance |
| **SAP MM-CMS** | Oracle Procurement Cloud - Contracts | Contract lifecycle management |
| **SAP MM-IM** | Oracle Procurement Cloud - Self-Service Procurement | Employee self-service purchasing |
| **SAP Ariba** | Oracle Procurement Cloud - Sourcing / Supplier Portal | Supplier collaboration and e-sourcing |

### 3.3 Supply Chain Modules

| SAP Module | Oracle Module | Description |
|---|---|---|
| **SAP MM-IM** | Oracle SCM Cloud - Inventory Management | Inventory tracking and control |
| **SAP SD** | Oracle SCM Cloud - Order Management | Order processing and fulfillment |
| **SAP LE** | Oracle SCM Cloud - Logistics | Shipping and transportation |
| **SAP PP** | Oracle SCM Cloud - Manufacturing | Production planning (not applicable for BRHI) |
| **SAP PLM** | Oracle SCM Cloud - Product Lifecycle Management | Product data management |
| **SAP EWM** | Oracle SCM Cloud - Warehouse Management | Warehouse operations (integrated with Manhattan WMS) |

### 3.4 Human Capital Management

| SAP Module | Oracle Module | Description |
|---|---|---|
| **SAP HCM-PA** | Oracle HCM Cloud - Core HR | Employee records and organizational management |
| **SAP HCM-PY** | Oracle HCM Cloud - Payroll | Payroll processing and payments |
| **SAP HCM-PT** | Oracle HCM Cloud - Time and Labor | Time tracking and attendance |
| **SAP HCM-TM** | Oracle HCM Cloud - Talent Management | Recruiting, performance, and succession |
| **SAP HCM-LD** | Oracle HCM Cloud - Learning | Training and development |
| **SAP HCM-SS** | Oracle HCM Cloud - Self-Service | Employee and manager self-service |

### 3.5 Enterprise Performance Management

| SAP Module | Oracle Module | Description |
|---|---|---|
| **SAP BPC** | Oracle EPM Cloud - Planning and Budgeting | Financial planning and budgeting |
| **SAP SEM-BCS** | Oracle EPM Cloud - Consolidation | Financial consolidation and reporting |
| **SAP Analytics Cloud** | Oracle EPM Cloud - Strategic Modeling | Scenario planning and modeling |

---

## 4. Business Function to Oracle Module Mapping

### 4.1 Store Operations Functions

| Business Function | Primary Oracle Module | Supporting Modules |
|---|---|---|
| **Point of Sale (POS) Integration** | Oracle Financials Cloud - AR | Oracle SCM Cloud - Inventory |
| **Store Receiving** | Oracle Procurement Cloud - Purchasing | Oracle SCM Cloud - Inventory |
| **Inventory Counts** | Oracle SCM Cloud - Inventory Management | Oracle Financials Cloud - GL |
| **Store Transfers** | Oracle SCM Cloud - Inventory Management | Oracle SCM Cloud - Logistics |
| **Customer Returns** | Oracle Financials Cloud - AR | Oracle SCM Cloud - Inventory |
| **Pro Desk Operations** | Oracle Financials Cloud - AR | Oracle Procurement Cloud |

### 4.2 Distribution Center Functions

| Business Function | Primary Oracle Module | Supporting Modules |
|---|---|---|
| **Receiving from Vendors** | Oracle Procurement Cloud - Purchasing | Oracle SCM Cloud - Inventory |
| **Picking and Packing** | Oracle SCM Cloud - Order Management | Oracle SCM Cloud - Inventory |
| **Shipping to Stores** | Oracle SCM Cloud - Logistics | Oracle SCM Cloud - Inventory |
| **Vendor Direct Ship** | Oracle SCM Cloud - Order Management | Oracle Procurement Cloud |
| **Warehouse Inventory** | Oracle SCM Cloud - Inventory Management | Oracle Financials Cloud - GL |

### 4.3 Corporate Functions

| Business Function | Primary Oracle Module | Supporting Modules |
|---|---|---|
| **Financial Reporting** | Oracle Financials Cloud - GL | Oracle EPM Cloud |
| **Accounts Payable** | Oracle Financials Cloud - AP | Oracle Procurement Cloud |
| **Accounts Receivable** | Oracle Financials Cloud - AR | Oracle Financials Cloud - GL |
| **Treasury** | Oracle Financials Cloud - Cash Management | Oracle Financials Cloud - GL |
| **Tax Compliance** | Oracle Financials Cloud - Tax Management | Oracle Financials Cloud - GL |
| **Fixed Assets** | Oracle Financials Cloud - Fixed Assets | Oracle Financials Cloud - GL |
| **Procurement** | Oracle Procurement Cloud - Purchasing | Oracle Financials Cloud - AP |
| **HR Operations** | Oracle HCM Cloud - Core HR | Oracle HCM Cloud - Payroll |
| **Payroll** | Oracle HCM Cloud - Payroll | Oracle Financials Cloud - AP |
| **Financial Planning** | Oracle EPM Cloud - Planning | Oracle Financials Cloud - GL |

---

## 5. Business Process to Oracle Module Mapping

### 5.1 Order-to-Cash (O2C) Process

| Process Step | Oracle Module | Integration Points |
|---|---|---|
| **Order Entry** | Oracle Financials Cloud - AR | POS, E-commerce, Pro Desk |
| **Inventory Check** | Oracle SCM Cloud - Inventory | Manhattan WMS, Store POS |
| **Order Fulfillment** | Oracle SCM Cloud - Order Management | IBM Sterling OMS, Manhattan WMS |
| **Shipping** | Oracle SCM Cloud - Logistics | Carrier APIs |
| **Invoicing** | Oracle Financials Cloud - AR | Oracle Financials Cloud - GL |
| **Payment Processing** | Oracle Financials Cloud - AR | Adyen, Credit Card Processors |
| **Collections** | Oracle Financials Cloud - AR | Oracle Financials Cloud - GL |
| **Revenue Recognition** | Oracle Financials Cloud - GL | ASC 606 Rules |

### 5.2 Procure-to-Pay (P2P) Process

| Process Step | Oracle Module | Integration Points |
|---|---|---|
| **Requisition** | Oracle Procurement Cloud - Purchasing | Budget System |
| **Approval** | Oracle Procurement Cloud - Purchasing | Workflow Engine |
| **PO Creation** | Oracle Procurement Cloud - Purchasing | Oracle Procurement Cloud - Contracts |
| **PO Transmission** | Oracle Procurement Cloud - Purchasing | EDI, Ariba Network |
| **Goods Receipt** | Oracle Procurement Cloud - Purchasing | Manhattan WMS |
| **Invoice Processing** | Oracle Procurement Cloud - Purchasing | Oracle Financials Cloud - AP |
| **3-Way Match** | Oracle Procurement Cloud - Purchasing | Oracle Financials Cloud - AP |
| **Payment** | Oracle Financials Cloud - AP | Bank Systems |
| **Accounting** | Oracle Financials Cloud - GL | Oracle Financials Cloud - AP |

### 5.3 Hire-to-Retire Process

| Process Step | Oracle Module | Integration Points |
|---|---|---|
| **Recruiting** | Oracle HCM Cloud - Talent Management | Job Boards, Background Checks |
| **Onboarding** | Oracle HCM Cloud - Core HR | Oracle HCM Cloud - Learning |
| **Time and Attendance** | Oracle HCM Cloud - Time and Labor | Time Clocks, Scheduling |
| **Payroll** | Oracle HCM Cloud - Payroll | Oracle Financials Cloud - AP |
| **Benefits** | Oracle HCM Cloud - Benefits | Benefit Carriers |
| **Performance** | Oracle HCM Cloud - Talent Management | 360 Feedback |
| **Learning** | Oracle HCM Cloud - Learning | BuildRight University |
| **Offboarding** | Oracle HCM Cloud - Core HR | IT Systems |

---

## 6. Integration Architecture

### 6.1 Key Integrations

| Source System | Target Oracle Module | Integration Method | Data Flow |
|---|---|---|---|
| **NCR Emerald POS** | Oracle Financials Cloud - AR | Real-time API | Sales transactions, returns |
| **Manhattan WMS** | Oracle SCM Cloud - Inventory | Real-time API | Inventory movements, receipts |
| **IBM Sterling OMS** | Oracle SCM Cloud - Order Management | Real-time API | Order routing, status updates |
| **Salesforce Commerce Cloud** | Oracle Financials Cloud - AR | Real-time API | Online orders, customer data |
| **Adyen Payment Gateway** | Oracle Financials Cloud - AR | Batch + Real-time | Payment processing, settlement |
| **Vertex Tax Engine** | Oracle Financials Cloud - Tax | Real-time API | Tax calculation |
| **Concur Expense** | Oracle Financials Cloud - AP | Batch | Employee expenses |
| **SPS Commerce EDI** | Oracle Procurement Cloud | EDI (850, 855, 856, 810) | PO, ASN, Invoice exchange |
| **Bank of America** | Oracle Financials Cloud - Cash Management | Bank File | Bank statements, payments |
| **Carrier Systems** | Oracle SCM Cloud - Logistics | Real-time API | Shipping rates, tracking |

### 6.2 Integration Standards

| Standard | Description |
|---|---|
| **Real-time APIs** | REST/SOAP web services for transactional data |
| **Batch Processing** | Scheduled ETL for non-critical data |
| **EDI Standards** | ANSI X12 transactions for vendor communications |
| **Oracle Integration Cloud (OIC)** | Primary integration platform for Oracle modules |
| **Data Quality** | Master Data Management (MDM) for customer, vendor, product |

---

## 7. Key Configuration Differences

### 7.1 Chart of Accounts

| Aspect | SAP Approach | Oracle Approach |
|---|---|---|
| **Structure** | Fixed segment structure | Flexible segment structure |
| **Segments** | Company Code, GL Account, Cost Center, etc. | Company, Business Unit, Department, Account, etc. |
| **Flexibility** | Limited post-go-live changes | Dynamic segment addition |
| **Reporting** | Multiple reporting views | Single ledger, multiple reporting currencies |

### 7.2 Workflow

| Aspect | SAP Approach | Oracle Approach |
|---|---|---|
| **Approval Workflows** | SAP Workflow | Oracle BPM |
| **Notification** | SAP Connect | Oracle Notifications |
| **Mobile Approvals** | Limited mobile support | Native mobile app approvals |
| **Delegation** | Complex delegation setup | Simple delegation rules |

### 7.3 Reporting

| Aspect | SAP Approach | Oracle Approach |
|---|---|---|
| **Financial Reports** | SAP Financial Statements | Oracle Financial Reporting Studio |
| **Ad-hoc Analysis** | SAP Query, Report Writer | Oracle Smart View, OTBI |
| **Embedded Analytics** | Limited | Oracle Transactional Business Intelligence |
| **AI/ML Capabilities** | Limited | Oracle AI agents for anomaly detection, predictions |

---

## 8. User Roles and Permissions

### 8.1 Key Oracle Roles

| Role | Description | Modules Access |
|---|---|---|
| **Accounts Payable Specialist** | Processes vendor invoices and payments | Oracle Financials Cloud - AP |
| **Accounts Receivable Specialist** | Manages customer billing and collections | Oracle Financials Cloud - AR |
| **General Ledger Accountant** | Maintains GL and performs period close | Oracle Financials Cloud - GL |
| **Procurement Specialist** | Creates and manages purchase orders | Oracle Procurement Cloud |
| **Inventory Manager** | Manages inventory levels and movements | Oracle SCM Cloud - Inventory |
| **HR Administrator** | Maintains employee records and processes payroll | Oracle HCM Cloud |
| **Store Associate** | Uses Oracle for basic transactions | Oracle Financials Cloud - AR (limited) |
| **Store Manager** | Manages store operations via Oracle | Oracle Financials Cloud, Oracle SCM Cloud |

### 8.2 Segregation of Duties (SoD)

| Critical SoD Conflict | Oracle Control |
|---|---|
| **Create PO and Approve PO** | Role separation enforced |
| **Create Vendor and Pay Vendor** | Role separation enforced |
| **Create Employee and Process Payroll** | Role separation enforced |
| **Create Asset and Depreciate Asset** | Role separation enforced |

---

## 9. Migration Considerations

### 9.1 Data Migration Scope

| Data Type | SAP Source | Oracle Target | Migration Method |
|---|---|---|---|
| **Master Data** | SAP Master Data | Oracle Fusion Data | ETL with data cleansing |
| **Open Transactions** | SAP Open Items | Oracle Open Items | Balances migration |
| **Historical Data** | SAP Historical | Oracle Historical | Selective migration |
| **Configuration** | SAP Config | Oracle Config | Manual configuration |

### 9.2 Testing Strategy

| Test Type | Scope | Oracle Module |
|---|---|---|
| **Unit Testing** | Individual functions | All modules |
| **Integration Testing** | End-to-end processes | Multiple modules |
| **User Acceptance Testing** | Business scenarios | All modules |
| **Performance Testing** | System performance | All modules |

---

## 10. Support and Training

### 10.1 Training Approach

| User Group | Training Method | Oracle Modules |
|---|---|---|
| **Finance Users** | Instructor-led + Oracle University | Oracle Financials Cloud |
| **Procurement Users** | Instructor-led + Oracle University | Oracle Procurement Cloud |
| **HR Users** | Instructor-led + Oracle University | Oracle HCM Cloud |
| **Store Associates** | E-learning + Quick Reference | Oracle Financials Cloud (limited) |
| **Managers** | Blended learning + Coaching | All applicable modules |

### 10.2 Support Model

| Support Tier | Description | Contact |
|---|---|---|
| **Tier 1** | Help Desk | 1-800-BUILD-IT |
| **Tier 2** | Oracle CoE Team | oracle-support@buildright.com |
| **Tier 3** | Oracle Advanced Customer Services | Oracle Support Portal |

---

*This document is the property of BuildRight Home Improvement, Inc. and is intended for internal use by authorized associates. Unauthorized distribution, reproduction, or disclosure is prohibited. For questions regarding this document, contact the Enterprise Technology Team at oracle-program@buildright.com or extension 4-0002.*