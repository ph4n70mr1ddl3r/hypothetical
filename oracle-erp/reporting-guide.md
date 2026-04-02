# Oracle Fusion Cloud ERP Reporting and Analytics Guide

## BuildRight Home Improvement, Inc. (BRHI)

---

## 1. Document Control

| Field | Detail |
|---|---|
| **Document ID** | BRHI-TECH-006 |
| **Version** | 1.0 |
| **Classification** | Internal |
| **Effective Date** | April 2, 2026 |
| **Document Owner** | Chief Technology Officer |
| **Approved By** | Executive Leadership Team |
| **Review Cycle** | Quarterly |
| **Next Review Date** | July 2, 2026 |
| **Distribution** | Finance, Operations, Merchandising, HR, IT, Data Governance |

### Revision History

| Version | Date | Author | Description |
|---|---|---|---|
| 1.0 | April 2, 2026 | Enterprise Technology Team | Initial release — comprehensive reporting guide |

---

## 2. Purpose and Scope

### 2.1 Purpose

This guide provides comprehensive instructions for creating, running, and distributing reports and analytics using Oracle Fusion Cloud ERP and Oracle Analytics Cloud. It covers:

- **Standard Reports**: Pre-built reports available to all users
- **Self-Service Reporting**: How to create custom reports without IT assistance
- **AI-Powered Analytics**: Using Oracle AI for predictive and prescriptive insights
- **Dashboard Design**: Creating interactive dashboards for decision-making
- **Distribution and Scheduling**: Automating report delivery

### 2.2 Scope

This guide covers:

- All Oracle Fusion Cloud ERP modules (Financials, Procurement, SCM, HCM, EPM, Risk Management)
- Oracle Analytics Cloud (OAC)
- Oracle Transactional Business Intelligence (OTBI)
- Oracle Enterprise Performance Management (EPM) reporting
- AI-powered analytics features

### 2.3 Guiding Principles

1. **Self-Service First**: Empower business users to create their own reports
2. **Data Governance**: Ensure data quality and security in all reports
3. **AI-Augmented**: Leverage AI for insights, not just data presentation
4. **Mobile-Ready**: Design reports for desktop and mobile consumption
5. **Actionable Insights**: Focus on decisions, not just data

---

## 3. Reporting Architecture

### 3.1 Reporting Tools Overview

| Tool | Purpose | Primary Users | Access |
|---|---|---|---|
| **Oracle Transactional Business Intelligence (OTBI)** | Self-service reporting on real-time transactional data | Business analysts, power users | `https://otbi.buildright.com` |
| **Oracle Analytics Cloud (OAC)** | Advanced analytics, dashboards, and data visualization | Data analysts, executives | `https://analytics.buildright.com` |
| **Oracle Enterprise Performance Management (EPM)** | Financial reporting, consolidation, planning | Finance, FP&A | `https://epm.buildright.com` |
| **Oracle Financial Reporting Studio** | Complex financial statements and regulatory reports | Corporate accounting | Within Oracle Financials |
| **Embedded Analytics** | AI-powered insights within transactions | All users | Within Oracle Fusion modules |

### 3.2 Data Sources

| Data Domain | Source System | Refresh Frequency |
|---|---|---|
| **Financial Transactions** | Oracle Financials Cloud | Real-time |
| **Procurement Data** | Oracle Procurement Cloud | Real-time |
| **Inventory & Orders** | Oracle SCM Cloud | Real-time |
| **HR & Payroll** | Oracle HCM Cloud | Real-time |
| **External Data** | Weather, Market, Competitive | Daily |
| **AI Model Outputs** | Oracle AI Agents | Real-time |

### 3.3 Report Types

| Type | Description | Tools | Examples |
|---|---|---|---|
| **Operational Reports** | Daily transaction monitoring | OTBI, Embedded | Store sales, inventory levels |
| **Financial Reports** | Financial statements, regulatory | EPM, Financial Reporting Studio | Balance sheet, P&L, cash flow |
| **Analytical Reports** | Trend analysis, forecasting | OAC, AI Analytics | Sales trends, demand forecasts |
| **Compliance Reports** | SOX, regulatory compliance | Risk Management, OAC | Control testing, audit trails |
| **Dashboard Reports** | Interactive visualizations | OAC | Executive dashboards, KPI monitors |

---

## 4. Standard Reports Catalog

### 4.1 Financial Reports

| Report | Description | Audience | Access Path |
|---|---|---|---|
| **Store P&L** | Daily profit and loss by store | Store Managers, DMs | Financials → Reports → Store P&L |
| **Accounts Payable Aging** | Outstanding vendor invoices by age | AP Team | Financials → Reports → AP Aging |
| **Accounts Receivable Aging** | Outstanding customer balances by age | AR Team | Financials → Reports → AR Aging |
| **Cash Flow Forecast** | 13-week cash flow projection | Treasury | Financials → Reports → Cash Forecast |
| **Intercompany Reconciliation** | Intercompany balance matching | Corporate Accounting | Financials → Reports → Intercompany |

### 4.2 Procurement Reports

| Report | Description | Audience | Access Path |
|---|---|---|---|
| **Spend Analysis** | AI-classified spend by category, supplier | Procurement | Procurement → Reports → Spend Analysis |
| **Purchase Order Status** | Open POs, receipts, invoices | Buyers, Store Ops | Procurement → Reports → PO Status |
| **Supplier Performance** | Scorecards for key suppliers | Vendor Management | Procurement → Reports → Supplier Scorecard |
| **Contract Compliance** | Contract utilization vs. terms | Legal, Procurement | Procurement → Reports → Contract Compliance |

### 4.3 Supply Chain Reports

| Report | Description | Audience | Access Path |
|---|---|---|---|
| **Inventory Health** | Stock levels, turns, shrink by SKU/store | Merchandising, Store Ops | SCM → Reports → Inventory Health |
| **Demand Forecast Accuracy** | AI forecast vs. actual performance | Supply Chain Planning | SCM → Reports → Forecast Accuracy |
| **Order Fulfillment** | BOPIS, ship-to-home, jobsite delivery metrics | Operations, E-Commerce | SCM → Reports → Fulfillment Metrics |
| **Warehouse Efficiency** | DC productivity, throughput, accuracy | DC Managers | SCM → Reports → Warehouse Metrics |

### 4.4 Human Capital Reports

| Report | Description | Audience | Access Path |
|---|---|---|---|
| **Headcount by Department** | Current employee count by role, location | HR Business Partners | HCM → Reports → Headcount |
| **Turnover Analysis** | Voluntary/involuntary turnover trends | HR Leadership | HCM → Reports → Turnover |
| **Payroll Summary** | Payroll costs by department, location | Store Managers, Finance | HCM → Reports → Payroll Summary |
| **Training Completion** | Mandatory training compliance | HR, Department Managers | HCM → Reports → Training Compliance |

### 4.5 Risk and Compliance Reports

| Report | Description | Audience | Access Path |
|---|---|---|---|
| **SOX Control Testing** | Internal control test results | Internal Audit, Management | Risk → Reports → SOX Controls |
| **Segregation of Duties (SoD)** | SoD conflict analysis | Security, Audit | Risk → Reports → SoD Conflicts |
| **Access Certification** | User access review status | Managers, Security | Risk → Reports → Access Certification |
| **AI Model Monitoring** | AI performance, bias, drift detection | Data Governance, IT | Risk → Reports → AI Monitoring |

---

## 5. Self-Service Reporting

### 5.1 Creating a Simple Report (OTBI)

**Step-by-Step Guide:**

1. **Access OTBI**: Navigate to `https://otbi.buildright.com`
2. **New Analysis**: Click "New" → "Analysis"
3. **Select Subject Area**: Choose data domain (e.g., "Sales - Real Time")
4. **Select Columns**: Drag and drop desired fields from subject area
5. **Apply Filters**: Click "Filters" tab, add criteria (e.g., "Store = 1234")
6. **Sort and Group**: Arrange columns, add totals
7. **Format**: Choose table, pivot, or visualization
8. **Save**: Name report and save to appropriate folder
9. **Share**: Set permissions for other users

**Example: Store Sales by Department**
- Subject Area: "Sales - Real Time"
- Columns: Store, Department, Sales Amount, Units Sold, Average Price
- Filters: Transaction Date = Today, Store = User's Store
- Visualization: Bar chart by department

### 5.2 Creating an Advanced Dashboard (OAC)

**Step-by-Step Guide:**

1. **Access OAC**: Navigate to `https://analytics.buildright.com`
2. **New Project**: Click "Create" → "Project"
3. **Add Data**: Upload file or connect to Oracle data source
4. **Build Visualizations**: Drag and drop fields to create charts
5. **Create Dashboard**: Add visualizations to canvas, arrange layout
6. **Add Interactivity**: Create filters, drill-downs, tooltips
7. **Publish**: Save and publish to appropriate catalog folder
8. **Schedule**: Set up automated data refresh

**Example: Executive Sales Dashboard**
- **KPIs**: Total Sales, Comp Sales, Gross Margin, Customer Count
- **Charts**: Sales Trend (line), Sales by Region (map), Top 10 Products (bar)
- **Filters**: Date Range, Region, Store Format
- **Drill-Down**: Click any metric to see underlying details

### 5.3 AI-Powered Reporting

**Narrative Insights:**
- AI generates written summaries of report data
- Example: "Sales increased 5% primarily driven by lumber category (+12%) and paint (+8%), offset by appliances (-3%)."

**Anomaly Detection:**
- AI flags unusual patterns in reports
- Example: "Inventory shrink in Store 5678 is 2x district average"

**Predictive Analytics:**
- AI forecasts future trends based on historical data
- Example: "Based on current trends, Q4 sales are projected to increase 8%"

**Prescriptive Analytics:**
- AI recommends actions based on data
- Example: "Based on forecast, recommend increasing paint inventory by 15% for spring season"

---

## 6. Financial Reporting

### 6.1 Oracle Financial Reporting Studio

**Access**: Within Oracle Financials Cloud → Reports → Financial Reporting Studio

**Key Features:**
- **Multi-GAAP Reporting**: Simultaneous reporting under US GAAP, IFRS, Mexican NIIF
- **Consolidation**: Automatic intercompany eliminations, minority interest
- **Drill-Down**: From consolidated numbers to transaction details
- **Cellular Reporting**: Secure cell-level access for sensitive data

**Standard Financial Reports:**

| Report | Description | Frequency |
|---|---|---|
| **Balance Sheet** | Assets, liabilities, equity | Daily, Monthly |
| **Income Statement** | Revenue, expenses, net income | Daily, Monthly |
| **Cash Flow Statement** | Operating, investing, financing activities | Monthly |
| **Trial Balance** | General ledger account balances | Daily |
| **Budget vs. Actual** | Variance analysis by department | Monthly |

### 6.2 EPM Cloud Reporting

**Planning and Budgeting Reports:**
- **Budget vs. Actual**: Track performance against plan
- **Scenario Analysis**: Compare best case, worst case, most likely
- **Long-Range Planning**: 5-year financial projections

**Consolidation Reports:**
- **Consolidated Financial Statements**: Multi-entity, multi-currency
- **Intercompany Eliminations**: Automated elimination entries
- **Currency Translation**: Automatic translation to reporting currency

**Account Reconciliation Reports:**
- **Reconciliation Status**: Track completion of monthly reconciliations
- **AI-Assisted Matching**: AI suggests matches for reconciling items
- **Exception Reports**: Items requiring manual review

---

## 7. AI and Advanced Analytics

### 7.1 Oracle AI Analytics Capabilities

| Capability | Description | Use Cases |
|---|---|---|
| **Natural Language Query** | Ask questions in plain English | "Show me top 10 stores by sales last month" |
| **Smart Insights** | AI identifies key drivers in data | "What factors contributed to sales increase?" |
| **What-If Analysis** | Model scenarios with AI | "What if we increase marketing spend by 10%?" |
| **Cluster Analysis** | AI groups similar items | "Which stores have similar sales patterns?" |
| **Outlier Detection** | AI identifies anomalies | "Which transactions are unusual?" |

### 7.2 AI-Powered Dashboards

**Example: AI Inventory Dashboard**

**Components:**
1. **Current Stock Levels**: Real-time inventory across network
2. **AI Demand Forecast**: 13-week forecast by SKU/store
3. **Replenishment Recommendations**: AI-suggested orders
4. **Risk Alerts**: Stockouts, overstocks, slow movers
5. **Optimization Actions**: One-click to execute AI recommendations

**Example: AI Financial Dashboard**

**Components:**
1. **Financial Health Score**: AI-calculated score based on multiple metrics
2. **Cash Flow Prediction**: 13-week cash forecast with confidence intervals
3. **Anomaly Detection**: AI-flagged transactions for review
4. **Optimization Opportunities**: AI-identified cost savings
5. **Scenario Planning**: What-if analysis for strategic decisions

---

## 8. Report Distribution and Scheduling

### 8.1 Scheduling Reports

**Step-by-Step:**
1. Open any report → "Schedule"
2. Set frequency: Once, Daily, Weekly, Monthly, Quarterly
3. Set time: Choose delivery time
4. Set recipients: Users, groups, email addresses
5. Set format: PDF, Excel, CSV, HTML
6. Set filters: Dynamic filters (e.g., "Previous Month")
7. Save schedule

**Example Schedules:**

| Report | Frequency | Recipients | Format |
|---|---|---|---|
| Store P&L | Daily 6 AM | Store Manager, DM | PDF |
| Payroll Summary | Bi-weekly | Store Manager, HR | Excel |
| AI Forecast Accuracy | Weekly Monday | Supply Chain Planning | PDF |
| SOX Control Testing | Monthly | Internal Audit, CFO | PDF |

### 8.2 Distribution Channels

| Channel | Description | Security |
|---|---|---|
| **Email** | Attachments to email | Secure attachment |
| **Oracle Content Management** | Store in secure repository | Role-based access |
| **SFTP** | Secure file transfer | Encrypted |
| **Dashboard Publishing** | Publish to OAC catalog | Role-based access |
| **API Distribution** | Programmatic access | OAuth secured |

### 8.3 Report Security

**Access Control:**
- **Folder Security**: Reports organized by department, role
- **Row-Level Security**: Users see only their data (store, region, department)
- **Column-Level Security**: Sensitive columns hidden based on role
- **Data Masking**: Sensitive data masked (SSN, salary, etc.)

**Audit Trail:**
- All report runs logged
- Data access tracked
- Distribution logged
- Modifications tracked

---

## 9. Best Practices

### 9.1 Report Design Principles

1. **Start with the Question**: What decision will this report support?
2. **Know Your Audience**: Tailor complexity and detail level
3. **One Report, One Purpose**: Don't overload reports with multiple objectives
4. **Use Visualization Wisely**: Choose appropriate chart types
5. **Include Context**: Benchmarks, trends, comparisons
6. **Make It Actionable**: Include recommended actions
7. **Test with Users**: Get feedback before publishing

### 9.2 Performance Optimization

1. **Use Indexed Fields**: Filter on indexed columns for speed
2. **Limit Data Volume**: Use appropriate time ranges
3. **Schedule Heavy Reports**: Run complex reports overnight
4. **Use Caching**: Cache frequently accessed data
5. **Archive Old Data**: Move historical data to archive

### 9.3 Data Quality

1. **Validate Sources**: Ensure data sources are correct
2. **Check Timeliness**: Verify data freshness
3. **Monitor Anomalies**: Set up alerts for data quality issues
4. **Document Data Lineage**: Track data from source to report
5. **Regular Audits**: Periodically audit report accuracy

---

## 10. Getting Help

### 10.1 Self-Help Resources

| Resource | Location | Description |
|---|---|---|
| **Report Gallery** | OAC → Catalog → Report Gallery | Pre-built reports by category |
| **Video Tutorials** | OAC → Help → Learning | Step-by-step video guides |
| **Sample Reports** | OTBI → Shared Folders → Samples | Example reports to copy |
| **AI Assistant** | OAC → Digital Assistant | Ask "How do I create a report?" |

### 10.2 Support Channels

| Issue Type | Contact | Response Time |
|---|---|---|
| **Report Access Issues** | Data Governance: oracle-data-gov@buildright.com | 4 hours |
| **Data Quality Issues** | Data Governance: oracle-data-gov@buildright.com | 2 hours |
| **Performance Issues** | Oracle CoE: oracle-support@buildright.com | 1 hour |
| **Training Requests** | Oracle Training: oracle-training@buildright.com | 1 business day |
| **Custom Report Requests** | Oracle CoE: oracle-support@buildright.com | 3 business days |

### 10.3 Report Request Process

**For Custom Reports:**
1. Submit request via ServiceNow → Reporting Request
2. Include: Business justification, data requirements, audience
3. Data Governance reviews for feasibility
4. Oracle CoE estimates effort (2 hours - 2 weeks)
5. Approval by requestor's manager
6. Development, testing, deployment

---

## 11. Appendices

### Appendix A: Report Glossary

| Term | Definition |
|---|---|
| **OTBI** | Oracle Transactional Business Intelligence |
| **OAC** | Oracle Analytics Cloud |
| **EPM** | Oracle Enterprise Performance Management |
| **Subject Area** | Logical grouping of data fields |
| **Dashboard** | Collection of visualizations on a single page |
| **KPI** | Key Performance Indicator |
| **Drill-Down** | Navigate from summary to detail |
| **Narrative** | AI-generated text summary of data |

### Appendix B: Common Report Formulas

| Formula | Description |
|---|---|
| **Inventory Turnover** | COGS / Average Inventory |
| **Gross Margin %** | (Sales - COGS) / Sales |
| **Days Sales Outstanding** | (AR / Sales) × Days in Period |
| **Forecast Accuracy** | 1 − (|Forecast − Actual| / Actual) |
| **Shrink %** | Shrink $ / Net Sales |

### Appendix C: Document References

| Document | ID | Location |
|---|---|---|
| Oracle Implementation Guide | BRHI-TECH-001 | oracle-erp/implementation-guide.md |
| Oracle Integration & Data Governance | BRHI-DG-001 | oracle-erp/integration-data-governance.md |
| Oracle AI Capabilities | BRHI-TECH-004 | oracle-erp/ai-agentic-capabilities.md |
| Oracle User Guide | BRHI-TECH-005 | oracle-erp/user-guide.md |

---

*This document is the property of BuildRight Home Improvement, Inc. and is intended for internal use by authorized associates. Unauthorized distribution, reproduction, or disclosure is prohibited. For questions regarding this document, contact the Enterprise Technology Team at oracle-support@buildright.com or extension 4-0002.*