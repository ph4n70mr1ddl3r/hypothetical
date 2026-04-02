# Procure-to-Pay (P2P) Business Process

## Document Control

| Field | Value |
|---|---|
| **Document ID** | BRHI-BP-002 |
| **Version** | 1.1 |
| **Classification** | Internal |
| **Effective Date** | April 1, 2026 |
| **Process Owner** | Chief Financial Officer (CFO) |
| **Process Steward** | Director, Procure-to-Pay Operations |
| **Author** | Procurement Process Excellence Team |
| **Reviewed By** | VP Merchandising, VP Finance, VP Supply Chain |
| **Approved By** | Chief Financial Officer |
| **Last Reviewed** | April 2, 2026 |
| **Next Review Date** | March 15, 2027 |

### Revision History

| Version | Date | Author | Description |
|---|---|---|---|
| 1.1 | April 2, 2026 | Enterprise Technology Team | Updated to replace SAP references with Oracle Fusion Cloud ERP |
| 1.0 | April 1, 2026 | Procurement Process Excellence Team | Initial release |

---

## 1. Process Overview

The Procure-to-Pay (P2P) cycle encompasses the complete end-to-end business process at BuildRight Home Improvement, Inc. (BRHI) from the initial identification of demand for goods or services through the final payment to the supplier. This process covers all procurement categories including merchandise inventory replenishment, non-merchandise operating supplies, maintenance-repair-operations (MRO), professional services, and capital expenditures.

The P2P process is designed to ensure that BRHI procures the right goods and services, at the right price, from the right suppliers, at the right time, while maintaining robust financial controls, regulatory compliance, and operational efficiency. The process integrates merchandising strategy, store operations, supply chain logistics, and financial management into a unified workflow.

### Scope

This document covers all procurement and payment activities across all BRHI locations, including:

- Corporate headquarters procurement
- Distribution center (DC) procurement and receiving
- Store-level procurement and receiving
- E-commerce fulfillment center procurement

### Process Objectives

- Ensure timely and cost-effective procurement of goods and services
- Maintain accurate financial records and strong internal controls
- Maximize early payment discount capture
- Minimize maverick (off-contract) spending
- Achieve high levels of three-way match automation
- Maintain positive supplier relationships through prompt, accurate payment
- Comply with SOX requirements and company policies

---

## 2. SIPOC Analysis

### Suppliers

| Supplier Category | Description |
|---|---|
| Merchandising Department | Buyers and category managers initiating merchandise replenishment and new item purchases |
| Store Operations | Store managers and associates initiating non-merchandise and supply requisitions |
| Distribution Centers | DC operations teams requesting MRO, packaging, and operational supplies |
| Corporate Departments | Marketing, IT, Facilities, HR and other departments requesting services and supplies |
| Capital Planning | Facilities and real estate teams initiating capital expenditure requests |
| Finance Department | Treasury and AP teams providing budget data, payment terms, and vendor master information |
| Supply Chain Planning | Demand forecasting and inventory planning systems generating replenishment signals |

### Inputs

| Input | Description | Source |
|---|---|---|
| Demand Signals | Automated replenishment triggers, manual buy decisions, seasonal plans | Oracle Procurement Cloud / Merchandising |
| Approved Budgets | Open-to-buy allocations, department operating budgets, capital budgets | Finance / Oracle Financials Cloud |
| Vendor Catalogs | Contract pricing, item master data, vendor product listings | Vendor Portal / Oracle Procurement Cloud - Sourcing/Supplier Portal |
| Vendor Master Data | Vendor banking details, payment terms, tax IDs, remit-to addresses | Oracle Procurement Cloud Vendor Master |
| Contracts and Agreements | Blanket purchase orders, framework agreements, negotiated terms | Procurement / Legal |
| Goods Receipt Confirmations | Physical receipt data, quality inspection results, putaway confirmations | WMS / Oracle Procurement Cloud |
| Invoices | Vendor invoices in EDI, portal, or paper format | Vendors |
| Approval Authority Matrix | Spending authority thresholds and approval routing rules | Finance Policy |

### Process

The P2P process consists of five sequential phases:

1. **Phase 1** — Demand Identification and Requisition
2. **Phase 2** — Purchase Order Processing
3. **Phase 3** — Goods Receipt
4. **Phase 4** — Invoice Processing
5. **Phase 5** — Payment Processing

### Outputs

| Output | Description |
|---|---|
| Approved Purchase Requisitions | Authorized requests for procurement converted to PO drafts |
| Purchase Orders (POs) | Legally binding documents transmitted to vendors |
| Goods Receipts | System records of physical goods received, triggering inventory and liability updates |
| Three-Way Match Results | Automated comparison of PO, goods receipt, and invoice data |
| Vendor Payments | ACH, wire, check, or virtual card payments remitted to vendors |
| Remittance Advices | Payment notifications sent to vendors (EDI 820, email, portal) |
| AP Reports | Aging reports, payment registers, discount capture reports |
| GL Postings | Financial journal entries for accruals, payments, and adjustments |

### Customers

| Customer | Description |
|---|---|
| Vendors / Suppliers | Receive POs, payment, and remittance communications |
| Stores | Receive merchandise and supplies for sale and operations |
| Finance / Accounting | Receive GL postings, accruals, payment records, and compliance reports |
| Merchandising | Receive procurement status updates and vendor performance data |
| Treasury | Receive payment execution instructions and bank reconciliation data |
| Internal Audit | Receive control evidence and audit trail data |

---

## 3. Process Steps

### Swimlane Roles

| Role | Abbreviation | Department |
|---|---|---|
| Requesting Associate | RA | Any Department |
| Buyer / Category Manager | BUY | Merchandising |
| Department Manager | DM | Any Department |
| Divisional Merchandise Manager | DMM | Merchandising |
| Vice President | VP | Various |
| Senior Vice President | SVP | Various |
| Chief Financial Officer | CFO | Finance |
| Chief Merchandising Officer | CMO | Merchandising |
| Accounts Payable Specialist | APS | Finance |
| AP Manager | APM | Finance |
| Receiving Associate | RCV | DC / Store Operations |
| Warehouse Associate | WHA | DC Operations |
| Treasury Analyst | TRS | Finance |
| Procurement Specialist | PRS | Procurement |

---

### Phase 1: Demand Identification and Requisition

#### Step 1.1 — Demand Signal Identification

| Attribute | Detail |
|---|---|
| **Swimlane** | BUY / RA |
| **Trigger** | Inventory level falls below safety stock, buyer identifies opportunity, or planned allocation becomes available |

Demand for procurement is triggered through one of three mechanisms:

**Automated Replenishment (System-Generated)**
- Oracle Procurement Cloud monitors on-hand inventory levels across all DCs and stores in real time
- When the available quantity (on-hand minus allocated minus in-transit) falls below the calculated safety stock level, the system automatically generates a replenishment proposal
- Safety stock levels are maintained per SKU per location and are recalculated monthly based on demand variability, lead time variability, and target service level (97.5% for A-items, 95% for B-items, 90% for C-items)
- The replenishment proposal includes the suggested order quantity (calculated as EOQ or lot-size multiple), the target DC or store, and the suggested delivery date based on vendor lead time
- Replenishment proposals are reviewed by the assigned buyer daily during the morning buying session (8:00 AM – 10:00 AM ET)

**Manual Buyer Decision**
- Buyers and category managers initiate purchase requisitions for non-replenishment scenarios including:
  - **New Item Introduction**: When a new product is added to the assortment plan, the buyer creates a requisition for the initial buy quantity. The initial buy quantity is determined by the category business plan and launch projection.
  - **Promotional Buy**: When a promotional event is planned (e.g., Spring Sale, Black Friday), the buyer creates a requisition for the promotional quantity, referencing the promotional plan number and event dates.
  - **Seasonal Buy**: When seasonal merchandise needs to be ordered ahead of the selling season (e.g., holiday decorations, garden supplies), the buyer initiates a requisition based on the seasonal merchandise plan.
  - **Opportunity Buy**: When a vendor offers a limited-time deal, closeout, or special purchase opportunity, the buyer may create a requisition with justification for the off-cycle purchase.
  - **Test Order**: When a new vendor or product line is being evaluated, the buyer creates a requisition for a test quantity, referencing the test plan.

**Planned (Open-to-Buy Allocation)**
- The merchandise planning team establishes open-to-buy (OTB) budgets by category, by month, as part of the annual and seasonal merchandise financial plans
- As OTB becomes available within the plan, the buyer initiates requisitions to allocate the budget to specific purchase orders
- OTB allocations are tracked in the merchandise planning system and reconciled weekly
- Requisitions referencing OTB must include the OTB plan number and category code for budget validation

#### Step 1.2 — Budget Verification

| Attribute | Detail |
|---|---|
| **Swimlane** | BUY / RA |
| **System** | Oracle Procurement Cloud / Oracle Financials Cloud |

Before a requisition can be submitted, the requestor must verify that funds are available against the appropriate budget:

**Merchandise Purchases**
- The system checks the requisition value against the current open-to-buy (OTB) balance for the relevant merchandise category and period
- OTB is calculated as: Planned Purchases − (On-Order + Committed + Received MTD)
- If the requisition value exceeds available OTB, the system blocks submission and displays the current OTB position
- The buyer may request OTB reallocation from the category manager or merchandise planner to free up budget
- OTB overrides above $25,000 require VP Merchandising approval

**Non-Merchandise Purchases (Operating Expenses)**
- The system checks the requisition value against the department's annual operating budget, less year-to-date committed and actual spend
- Budgets are maintained at the cost center level and mapped to GL accounts
- If the requisition would cause the cost center to exceed its budget, the system blocks submission
- Budget override requests must be submitted to the department VP and Finance Business Partner for approval

**Capital Expenditures (CapEx)**
- Capital requisitions are checked against the approved capital budget for the fiscal year
- Each capital project has an approved budget with line-item detail
- Capital requisitions must reference the approved project number (CPWBS element in Oracle Financials Cloud)
- Requisitions exceeding the approved project budget are blocked and require CFO approval to proceed

All budget checks are performed in real time within Oracle Procurement Cloud at the point of requisition entry. The system enforces hard blocks — no requisition may be submitted that exceeds an available budget without documented override approval.

#### Step 1.3 — Purchase Requisition Created

| Attribute | Detail |
|---|---|
| **Swimlane** | BUY / RA |
| **System** | Oracle Procurement Cloud |

The requestor creates a formal purchase requisition in Oracle Procurement Cloud containing the following data elements:

**Header Information**
- Requisition type (Standard, Stock, Non-Stock, Service, or Capital)
- Requestor name and employee ID
- Requesting department and cost center
- Requisition date (system date, non-editable)
- Delivery location (DC, store, or office address)
- Required delivery date (requested date, must be ≥ vendor lead time from current date)
- Project reference (for capital requisitions, linked to approved CapEx project)
- Business justification (free-text field, mandatory for non-replenishment requisitions)

**Line Item Detail (one or more per requisition)**
- Material number (for stocked items, linked to material master)
- Short description (free-text for non-stocked items)
- Quantity and unit of measure (each, case, pallet, etc.)
- Preferred vendor (optional — buyer may specify; if blank, system suggests based on source list)
- Estimated unit price (auto-populated from contract/purchase info record if available)
- Estimated extended price (quantity × unit price)
- GL account assignment (auto-derived from material type and cost center)
- Cost center or WBS element for charge-back
- Material group (for spend classification and reporting)

**Account Assignment**
- The system automatically derives the GL account from the material type and valuation class
- For merchandise inventory: Account Assignment Category "Stock" — charges to inventory GL
- For non-stock items: Account Assignment Category "Cost Center" — charges to requesting department
- For services: Account Assignment Category "Service" — charges to operating expense GL
- For capital: Account Assignment Category "WBS Element" — charges to capital project

Upon saving, the system assigns a unique requisition number and routes the requisition to the appropriate approval workflow based on the spending authority matrix.

#### Step 1.4 — Requisition Approval

| Attribute | Detail |
|---|---|
| **Swimlane** | DM / VP / SVP / CFO |
| **System** | Oracle Procurement Cloud Workflow |

Purchase requisitions are routed for approval based on the following authority matrix:

| Total Requisition Value | Required Approver(s) |
|---|---|
| Less than $5,000 | Requesting Associate + Direct Supervisor |
| $5,000 – $25,000 | Department Manager |
| $25,001 – $100,000 | Vice President (VP) of requesting area |
| Greater than $100,000 | Senior Vice President (SVP) + CFO dual approval |

**Approval Workflow Rules**
- Requisitions are routed via Oracle BPM to the designated approver's inbox and email notification
- Approvers may approve, reject (with reason), or return to requestor for modification
- Approval must be completed within 3 business days; otherwise the requisition auto-escalates to the approver's manager
- Approvers review the requisition for completeness, accuracy, budget availability, and business justification
- Segregation of duties is enforced: the requestor cannot be the approver on the same requisition
- All approvals are electronically timestamped and stored in the Oracle document flow for audit trail

**Emergency / Expedited Requisitions**
- For urgent purchases (e.g., emergency facility repair, critical stock-out), a requisition may be flagged as "Expedited"
- Expedited requisitions bypass the standard approval workflow and route directly to the department VP or, if unavailable, the AP Manager as delegate
- Expedited requisitions are reviewed retroactively by the Procurement Compliance team within 5 business days
- Use of the expedited flag is limited to 5% of requisitions per department per month; exceeding the threshold triggers a review by the Finance Business Partner

#### Step 1.5 — Approved Requisition Converts to PO Draft

| Attribute | Detail |
|---|---|
| **Swimlane** | System (Oracle Procurement Cloud) |
| **System** | Oracle Procurement Cloud |

Upon final approval, the system automatically converts the requisition into a Purchase Order (PO) draft:

- The system performs an automatic source determination: if a valid contract, scheduling agreement, or purchase info record exists for the material-vendor combination, it is referenced and pricing is auto-populated
- The PO draft inherits all data from the approved requisition: material, quantity, price, vendor, delivery date, account assignment
- For merchandise items with a source list, the system validates that the vendor is on the approved source list for the material
- The PO draft is assigned a unique PO number in Oracle Procurement Cloud but remains in "Draft" (not yet released) status
- The PO draft is routed to the buyer for review and completion of order-level details (vendor selection confirmation, terms and conditions, shipping instructions) before proceeding to Phase 2

---

### Phase 2: Purchase Order Processing

#### Step 2.1 — PO Creation

| Attribute | Detail |
|---|---|
| **Swimlane** | BUY |
| **System** | Oracle Procurement Cloud |

Purchase orders are created through one of two methods:

**System-Generated from Approved Requisition**
- For the majority of merchandise purchases, the PO is automatically created from the approved requisition as described in Step 1.5
- The buyer reviews the auto-generated PO draft for accuracy, confirms or adjusts vendor selection, and verifies pricing against the current contract or purchase info record
- The buyer may consolidate multiple approved requisitions for the same vendor into a single PO to optimize shipping and receiving efficiency

**Direct Buyer Entry**
- For merchandise purchases managed directly by the buying team (e.g., initial stock orders, seasonal buys, promotional orders), the buyer may create a PO directly in Oracle Procurement Cloud without a preceding requisition
- Direct-entry POs still require approval per the authority matrix in Step 2.5
- The buyer enters all PO data manually: vendor, material(s), quantity, price, delivery date, shipping terms, and account assignment
- Direct-entry POs are typically used for merchandise items where the buyer has full authority within their OTB and the purchase is part of the established merchandise plan

**PO Header Data**
- PO type (Standard PO, Framework Order, or Scheduling Agreement Release)
- Vendor number and name
- Company code (BRHI entity)
- Purchasing organization and group
- Currency (USD for domestic, vendor currency for import with exchange rate)
- Payment terms
- Incoterms
- Shipping conditions and receiving location

#### Step 2.2 — Vendor Selection

| Attribute | Detail |
|---|---|
| **Swimlane** | BUY / PRS |
| **System** | Oracle Procurement Cloud / Oracle Procurement Cloud - Sourcing/Supplier Portal |

Vendor selection follows a structured process based on the procurement category:

**Existing Vendor per Contract (Preferred)**
- For all merchandise categories with active vendor contracts or blanket purchase orders, the contracted vendor is selected automatically by the system via the source determination function
- The system's source list maintains the preferred vendor for each material, and the buyer selects the valid source record
- Contract pricing, minimum order quantities, and lead times are referenced from the contract

**Competitive Bid (>3 Quotes for Non-Contract Items >$10K)**
- For non-contract items with an estimated value exceeding $10,000, the buyer must obtain at least three competitive quotations from qualified vendors
- Requests for Quotation (RFQs) are issued through Oracle Procurement Cloud or Oracle Procurement Cloud - Sourcing/Supplier Portal Sourcing
- Vendors are given a minimum of 5 business days to respond to RFQs
- Quotations are evaluated on: price (weighted 50%), quality/specification compliance (25%), delivery lead time (15%), and vendor performance scorecard (10%)
- The winning bid is documented with a bid tabulation summary stored in the purchasing info record
- Single-source or sole-source justification must be documented in writing and approved by the VP of the requesting area when competitive bidding is not feasible

**Catalog Punch-Out for MRO Supplies**
- For maintenance, repair, and operations (MRO) supplies, requestors use Oracle Procurement Cloud - Sourcing/Supplier Portal catalog punch-out to select items from approved vendor catalogs
- Catalog pricing is pre-negotiated and displayed in real time
- The punch-out requisition auto-populates item descriptions, prices, and vendor information
- Catalog orders are consolidated daily and transmitted to the vendor as a single PO

#### Step 2.3 — Price Verification

| Attribute | Detail |
|---|---|
| **Swimlane** | BUY |
| **System** | Oracle Procurement Cloud |

**Contract Price (Auto-Populated)**
- For items covered by an active vendor contract, the price is automatically populated from the contract or purchase info record
- The system validates that the contract price has not expired and that the order quantity meets any minimum order requirements
- If the contract price has changed since the last PO, the system alerts the buyer to review the updated pricing

**Non-Contract Price Verification**
- For non-contract items, the buyer verifies the price against available market data:
  - **Items >$10,000**: Three competitive quotes are required as described in Step 2.2. The buyer selects the best-value price and documents the bid comparison.
  - **Items $500 – $10,000**: The buyer verifies the price against at least two sources: historical purchase price, published price lists, or a single competitive quote.
  - **Items <$500**: The buyer uses the catalog or quoted price without additional verification, relying on the vendor's standard terms.

**Price Change Alert**
- If the current vendor price exceeds the last paid price by more than 5%, the system generates a price change alert requiring buyer review and approval before the PO can be released
- The buyer must document the reason for the price increase (vendor notification, raw material surcharge, market conditions) in the PO header text

#### Step 2.4 — Terms and Conditions

| Attribute | Detail |
|---|---|
| **Swimlane** | BUY / APM |
| **System** | Oracle Procurement Cloud |

**Standard BRHI Terms and Conditions**
- All purchase orders include BRHI's standard terms and conditions of purchase, which are attached to every PO document automatically
- Standard T&Cs cover: acceptance, delivery, inspection, warranty, indemnification, insurance requirements, intellectual property, and dispute resolution
- In the event of a conflict between BRHI's T&Cs and vendor terms, BRHI's T&Cs govern unless a negotiated override is documented in the vendor agreement

**Negotiated Terms for Strategic Vendors**
- For strategic and preferred vendors (top 100 vendors representing approximately 80% of spend), individually negotiated terms are documented in vendor agreements maintained in Oracle Procurement Cloud - Sourcing/Supplier Portal
- Negotiated terms may include: volume rebates, marketing allowances, return-to-vendor provisions, consignment inventory terms, and extended warranty periods
- The buyer references the negotiated agreement number on the PO, and the system validates that the agreement is active

**Incoterms**

| Shipping Type | Incoterm | Responsibility |
|---|---|---|
| Domestic shipments | DDP (Delivered Duty Paid) | Vendor responsible for all freight, insurance, and delivery to BRHI receiving dock |
| Import shipments (ocean) | FOB Port of Loading | BRHI assumes risk at port of origin; freight forwarder arranged by BRHI logistics team |
| Import shipments (air) | FOB Origin | BRHI assumes risk at vendor's shipping dock |

**Payment Terms**

| Purchase Type | Standard Terms | Early Payment Discount |
|---|---|---|
| Merchandise | Net 60 | 2/10 (2% discount if paid within 10 days) |
| Services | Net 30 | Negotiated per contract |
| Construction | Net 45 | Negotiated per contract |
| Capital Equipment | Net 60 | Negotiated per contract |

#### Step 2.5 — PO Approval

| Attribute | Detail |
|---|---|
| **Swimlane** | BUY / DMM / VP / SVP / CMO / CFO |
| **System** | Oracle Procurement Cloud Release Strategy |

Purchase orders are approved (released) per the following authority matrix:

**Merchandise POs**

| PO Value | Required Approver |
|---|---|
| $0 – $5,000 | Buyer (self-release within OTB) |
| $5,001 – $50,000 | Divisional Merchandise Manager (DMM) |
| $50,001 – $250,000 | VP Merchandising |
| $250,001 – $1,000,000 | SVP Merchandising |
| Greater than $1,000,000 | Chief Merchandising Officer (CMO) |

**Capital POs**

| PO Value | Required Approver |
|---|---|
| $0 – $50,000 | Department VP |
| $50,001 – $250,000 | Department VP + CFO |
| $250,001 – $1,000,000 | SVP + CFO |
| Greater than $1,000,000 | CEO + CFO |

**Release Strategy Rules**
- Oracle Procurement Cloud release strategy is configured to route POs to the appropriate approver(s) based on the total PO value and purchasing group
- Each approver in the release chain must approve sequentially; dual approvals for capital >$50K require both signatures
- Approvers receive Oracle inbox notifications and email alerts for pending approvals
- Approval must be completed within 2 business days; overdue approvals escalate to the next-level approver
- The approver reviews: PO accuracy, budget compliance, vendor selection justification, pricing reasonableness, and contract alignment
- Rejection requires a written reason, and the PO is returned to the buyer for revision or cancellation

#### Step 2.6 — PO Transmitted to Vendor

| Attribute | Detail |
|---|---|
| **Swimlane** | System (Oracle Procurement Cloud / EDI) |
| **System** | Oracle Procurement Cloud / SPS Commerce EDI |

Upon final approval (release), the PO is transmitted to the vendor through one of the following channels:

| Transmission Method | Transaction Set | Volume | Use Case |
|---|---|---|---|
| EDI 850 | ANSI X12 850 | 80% of PO volume | Preferred method for all EDI-capable vendors |
| Vendor Portal (Oracle Procurement Cloud - Sourcing/Supplier Portal) | Ariba Network Order | 15% of PO volume | For vendors enrolled in Ariba but not EDI-capable |
| Email / Fax | PDF attachment | 5% of PO volume | For small vendors without EDI or portal capability |

**EDI 850 Processing**
- The system maps the Oracle PO data to the EDI 850 transaction set via SPS Commerce
- The EDI 850 includes: PO number, PO date, vendor number, ship-to address, requested delivery date, item details (SKU, description, quantity, unit price, unit of measure), and payment terms
- EDI transmission is attempted immediately upon PO release; failed transmissions are retried automatically up to 3 times at 30-minute intervals
- If EDI transmission fails after 3 attempts, the system generates an alert to the buyer and falls back to email transmission

**Vendor Portal Processing**
- For vendors on the Oracle Procurement Cloud - Sourcing/Supplier Portal Network, the PO is transmitted as an Ariba Network Order
- The vendor receives notification within the Ariba portal and by email
- The vendor can acknowledge, propose changes, or reject the order within the portal

**Email / Fax Processing**
- For non-EDI, non-portal vendors, the system generates a PDF of the PO and emails it to the vendor's ordering contact
- The buyer confirms vendor receipt by requesting a read receipt or follow-up confirmation email

#### Step 2.7 — Vendor Acknowledgment

| Attribute | Detail |
|---|---|
| **Swimlane** | BUY / Vendor |
| **System** | Oracle Procurement Cloud / EDI |

**Acknowledgment Requirements**
- The vendor must acknowledge the PO within 48 hours of receipt, confirming:
  - Acceptance or rejection of the order
  - Confirmed quantities per line item
  - Confirmed prices per line item
  - Confirmed (or revised) delivery date per line item

**EDI 855 (Purchase Order Acknowledgment)**
- EDI-capable vendors respond with an EDI 855 transaction
- The system automatically updates the PO in Oracle Procurement Cloud with the acknowledged quantities, prices, and dates
- If the vendor proposes changes (e.g., different quantity or delivery date), the system generates a discrepancy alert for the buyer

**Manual Acknowledgment**
- Non-EDI vendors acknowledge via email, phone, or the Ariba portal
- The buyer manually updates the PO acknowledgment status in Oracle Procurement Cloud

**Escalation Process**
- If a vendor does not acknowledge within 48 hours, the system generates an escalation alert to the buyer
- The buyer contacts the vendor directly (phone or email) to obtain acknowledgment
- If the vendor cannot be reached within 72 hours of PO transmission, the buyer evaluates alternative sourcing and escalates to the DMM if the item is critical
- Unacknowledged POs are included in the daily buyer action report until resolved

---

### Phase 3: Goods Receipt

#### Step 3.1 — Pre-Receipt Preparation

| Attribute | Detail |
|---|---|
| **Swimlane** | RCV / WHA |
| **System** | WMS / Oracle Procurement Cloud |

**Advance Shipment Notice (ASN) Review**
- EDI-capable vendors transmit an ASN (EDI 856) prior to shipment, typically 24–48 hours before arrival
- The ASN includes: shipment date, carrier, number of pallets/cartons, BOL number, PO reference, item detail (SKU, quantity per carton), and estimated arrival date
- The WMS receives the ASN and creates an expected receipt record, linking it to the corresponding PO(s)
- The receiving supervisor reviews the ASN daily to plan dock door assignments, labor scheduling, and staging area allocation

**Dock Appointment Verification**
- For full-truckload (FTL) shipments, the carrier must have a confirmed dock appointment scheduled through the BRHI transportation management system
- Dock appointments are scheduled in 2-hour windows between 6:00 AM and 4:00 PM local time, Monday through Friday
- The receiving supervisor confirms that the appointment is active and the dock door is available

**Labor Scheduling**
- Based on the ASN volume (pallet count, carton count, weight) and the day's receipt schedule, the receiving supervisor assigns receiving associates to dock doors
- Standard productivity targets: 150 cartons/hour for floor-loaded containers, 25 pallets/hour for palletized shipments

#### Step 3.2 — Carrier Check-In

| Attribute | Detail |
|---|---|
| **Swimlane** | RCV |
| **System** | WMS |

- The carrier arrives at the distribution center and reports to the guard shack or receiving office
- The driver presents the Bill of Lading (BOL) which includes: shipper name, consignee (BRHI DC), PO number(s), number of pallets, total cartons, total weight, and carrier PRO number
- The receiving clerk verifies the BOL against the scheduled dock appointment and expected ASN in the WMS
- If no appointment or ASN is on file, the receiving clerk contacts the buyer or transportation team for authorization to accept the shipment
- The driver is assigned a dock door and given a check-in time stamp; standard dwell time allowance is 2 hours for unload (detention charges apply after 2 hours per carrier contract)
- The BOL is scanned and attached to the receipt record in the WMS

#### Step 3.3 — Physical Receipt and Unload

| Attribute | Detail |
|---|---|
| **Swimlane** | RCV / WHA |
| **System** | WMS |

**Unload Process**
- Receiving associates unload the shipment from the trailer using forklifts (palletized) or conveyor systems (floor-loaded)
- All pallets and cartons are staged in the designated receiving lane adjacent to the dock door

**Count and Verification**
- The receiving associate counts all cartons and pallets and compares the physical count to the BOL and ASN quantities
- Each pallet is checked for visible damage (crushed, water-stained, shrink-wrap compromised)
- The receiving associate records the count in the WMS using a radio-frequency (RF) handheld scanner
- If the physical count matches the BOL and ASN within tolerance (±2% carton count), the receipt proceeds to quality inspection
- If the physical count is outside tolerance, the receiving supervisor is notified and an OS&D (Overage/Shortage/Damage) report is initiated (see Step 3.6)

#### Step 3.4 — Quality Inspection

| Attribute | Detail |
|---|---|
| **Swimlane** | RCV / WHA |
| **System** | WMS |

**Sampling Protocol**
- All inbound merchandise is subject to quality inspection using Acceptable Quality Level (AQL) Level II sampling per ANSI/ASQ Z1.4
- A minimum of 10% of cartons in each shipment are opened and inspected
- For new vendors (first 3 shipments) or vendors with quality issues on the watch list, 100% inspection is performed

**Inspection Criteria**

| Defect Category | Reject Threshold |
|---|---|
| Damaged packaging (crushed, torn, water-damaged) | >5% of inspected cartons |
| Wrong item (SKU mismatch) | Any occurrence |
| Quality defects (cosmetic, functional, safety) | >2% of inspected units |
| Labeling errors (barcode not scanning, wrong label) | >5% of inspected cartons |
| Expiration date non-compliance (shelf life <60% remaining) | Any occurrence |

**Disposition**
- **Pass**: Cartons pass inspection and proceed to goods receipt entry and putaway
- **Fail — Partial**: Defective cartons are segregated and dispositioned (return to vendor, destroy, or markdown); non-defective cartons proceed
- **Fail — Full**: Entire shipment is placed on quality hold; buyer and vendor are notified immediately; shipment is not received into inventory until disposition is determined

#### Step 3.5 — Goods Receipt Entry in Oracle Procurement Cloud/WMS

| Attribute | Detail |
|---|---|
| **Swimlane** | RCV |
| **System** | Oracle Procurement Cloud / WMS Manhattan Associates |

**Scanning and Receipt**
- The receiving associate scans each pallet's license plate barcode or each carton's barcode using an RF handheld device
- The scan links the physical item to the PO line item in Oracle Procurement Cloud
- For each PO line, the receiving associate enters the received quantity (in the PO unit of measure)
- The system performs a real-time validation: received quantity cannot exceed PO quantity by more than the configured over-delivery tolerance (10% for A-items, 5% for B/C-items)

**Oracle Procurement Cloud Goods Receipt (Movement Type 101)**
- Upon confirmation of all scanned items, the system posts a goods receipt (GR) in Oracle Procurement Cloud with movement type 101
- The GR posting triggers the following updates in Oracle Procurement Cloud:
  - **Inventory Update**: Quantity is added to unrestricted stock at the receiving location (DC or store)
  - **Value Update**: Inventory value is increased at the material's standard or moving average price
  - **GR/IR Account**: The GR/IR (Goods Receipt / Invoice Receipt) clearing account is debited, creating a liability accrual
  - **Material Document**: A material document is created as the audit trail for the physical movement
- The WMS receipt record is updated to "Received" status and the items become available for putaway

#### Step 3.6 — Discrepancy Handling (OS&D)

| Attribute | Detail |
|---|---|
| **Swimlane** | RCV / BUY / APM |
| **System** | WMS / Oracle Procurement Cloud |

When physical receipt quantities do not match expected quantities, an OS&D (Overage, Shortage, and Damage) report is created:

**Tolerance Thresholds**

| Variance Type | Tolerance | Action |
|---|---|---|
| Carton count | ±2% | Within tolerance — receipt at actual; variance noted |
| Unit count | ±5% | Within tolerance — receipt at actual; variance noted |
| Damage | Any visible damage | Damage documented; claim process initiated |

**OS&D Process**

1. **Report Creation (within 24 hours)**: The receiving associate creates an OS&D report in the WMS documenting:
   - PO number, item, expected quantity, actual quantity, variance amount
   - Type of variance: overage, shortage, or damage
   - Photos of damaged goods (minimum 4 photos: overview, close-up of damage, label, and packaging)
   - Carrier name, PRO number, and BOL number

2. **Vendor Notification (within 24 hours)**: The buyer is notified of the discrepancy via an automated alert. The buyer contacts the vendor to report the issue and request resolution.

3. **Carrier Claim (within 48 hours for freight damage)**: For shipments where damage occurred during transit, the transportation team files a freight claim with the carrier within 48 hours of delivery. The claim includes: OS&D report, photos, BOL, and invoice value of damaged goods.

4. **Resolution**: The buyer and vendor agree on resolution, which may include:
   - Replacement shipment (vendor ships replacement at no charge)
   - Credit memo (vendor issues credit for missing/damaged goods)
   - Price adjustment (discount on future order)
   - Rejection and return (goods returned to vendor at vendor's expense)

5. **System Adjustment**: The receiving supervisor adjusts the goods receipt in Oracle Procurement Cloud to reflect the actual accepted quantity. Rejected quantities are posted as returns to vendor (movement type 122) or scrap (movement type 551) as appropriate.

#### Step 3.7 — Putaway

| Attribute | Detail |
|---|---|
| **Swimlane** | WHA |
| **System** | WMS Manhattan Associates |

**WMS-Directed Putaway**
- After goods receipt is confirmed, the WMS generates putaway tasks directing warehouse associates to move received goods from the receiving lane to the designated storage location
- Putaway must be completed within 24 hours of receipt to ensure timely inventory availability for order fulfillment
- The WMS determines the optimal putaway location based on: item dimensions, storage type (rack, floor, mezzanine), zone (fast-mover vs. slow-mover), and current capacity

**FIFO Rotation Enforced**
- The WMS enforces First-In, First-Out (FIFO) inventory rotation for all perishable and date-sensitive merchandise
- For non-perishable merchandise, the system enforces FIFO at the lot level to ensure older inventory is picked before newer inventory
- The system assigns a receipt date stamp to each license plate and tracks the date through the putaway and picking processes

**Location Confirmation**
- The warehouse associate scans the destination location barcode to confirm the putaway
- The WMS validates that the correct location was used and updates the inventory record to reflect the item's new storage location
- If the scanned location does not match the directed location, the system prompts the associate to confirm or redirect
- Upon successful putaway confirmation, the inventory is fully available for allocation to customer orders, store replenishment, or intercompany transfer

---

### Phase 4: Invoice Processing

#### Step 4.1 — Invoice Receipt

| Attribute | Detail |
|---|---|
| **Swimlane** | APS / System |
| **System** | Oracle Procurement Cloud / SPS Commerce EDI / Oracle Procurement Cloud - Sourcing/Supplier Portal |

Invoices are received from vendors through the following channels:

| Receipt Method | Transaction / Format | Volume | Processing |
|---|---|---|---|
| EDI 810 | ANSI X12 810 Invoice | 80% of invoices | Automatic ingestion into Oracle Procurement Cloud; header and line item data parsed and mapped to PO |
| Vendor Portal (Oracle Procurement Cloud - Sourcing/Supplier Portal) | Ariba Network Invoice | 15% of invoices | Vendor uploads invoice in the portal; data flows into Oracle Procurement Cloud via integration |
| Email / Mail | PDF or paper | 5% of invoices | AP specialist manually enters invoice header and line data into Oracle Procurement Cloud |

**EDI 810 Processing**
- The EDI 810 invoice is received via SPS Commerce and automatically parsed into Oracle Procurement Cloud
- Key fields extracted: vendor number, invoice number, invoice date, PO number, line item details (material, quantity, unit price, extended price), tax amount, freight amount, and total invoice amount
- The system performs initial validation: vendor active in master data, valid PO reference, invoice not previously processed (duplicate check)
- Validated invoices are staged for three-way matching; invoices failing initial validation are routed to an AP specialist for manual review

#### Step 4.2 — Invoice Validation

| Attribute | Detail |
|---|---|
| **Swimlane** | System / APS |
| **System** | Oracle Procurement Cloud |

Before three-way matching, each invoice is validated against the following criteria:

| Validation Check | Rule | Failure Action |
|---|---|---|
| Vendor active in master data | Vendor number exists and is not blocked | Route to AP specialist; contact vendor or procurement |
| Valid PO reference | Invoice references an active, released PO | Route to AP specialist; if no PO, return to vendor |
| Invoice not a duplicate | Invoice number + vendor number combination is unique | Auto-block as duplicate; route to AP specialist |
| Amount within tolerance | Invoice total is within reasonable range of PO value | Flag for review if variance >10% |
| Correct tax calculation | Tax rate and amount are consistent with ship-to location | Route to AP specialist for tax verification |
| Invoice date within range | Invoice date is not more than 120 days after PO date | Route to buyer for confirmation of validity |

Invoices that pass all validation checks proceed to three-way matching. Invoices that fail any check are placed on hold with a descriptive block reason code and assigned to the appropriate AP specialist for resolution.

#### Step 4.3 — Three-Way Match

| Attribute | Detail |
|---|---|
| **Swimlane** | System (Oracle Procurement Cloud) |
| **System** | Oracle Procurement Cloud Automatic Invoice Verification |

The system performs an automatic three-way match comparing the invoice against the purchase order and the goods receipt:

**Match Point 1: PO Price vs. Invoice Price**
- The system compares the invoiced unit price to the PO unit price for each line item
- Tolerance: $50 absolute or 2% per line item (whichever is greater)
- If the variance is within tolerance, the line is marked as "matched"
- If the variance exceeds tolerance, the line is flagged as a "price variance" exception

**Match Point 2: PO Quantity vs. Goods Receipt Quantity**
- The system compares the total goods receipt quantity to the PO quantity
- Tolerance: 5% over-delivery allowed per line item
- If goods receipt quantity exceeds PO quantity by more than 5%, the excess is flagged as an "over-delivery" exception
- If goods receipt quantity is less than PO quantity (partial delivery), the invoice may still be matched for the received portion

**Match Point 3: Goods Receipt Quantity vs. Invoice Quantity**
- The system compares the invoiced quantity to the goods receipt quantity for each line item
- Tolerance: 5% per line item
- If the invoiced quantity exceeds the goods receipt quantity by more than 5%, the line is flagged as a "quantity variance — no GR" or "quantity variance — partial GR" exception
- If the invoiced quantity is less than goods receipt quantity, the invoice is processed for the invoiced amount (partial invoice)

**Match Outcome**
- **Full Match**: All three match points are within tolerance — invoice is auto-approved for payment
- **Partial Match**: Some lines match, others have exceptions — matched lines are approved; exception lines are routed for resolution
- **No Match**: No valid goods receipt exists for the PO referenced — invoice is blocked pending GR

#### Step 4.4 — Match Resolution

| Attribute | Detail |
|---|---|
| **Swimlane** | BUY / RCV / APS |
| **System** | Oracle Procurement Cloud |

Exceptions identified during three-way matching are resolved according to the following rules:

**Price Variance >$50 or >2%**
- The invoice line is auto-routed to the buyer who placed the PO
- The buyer reviews the variance and determines the cause:
  - Vendor invoiced at a different price than PO (unauthorized price change)
  - Contract price update not reflected on PO
  - Promotional or retroactive pricing adjustment
- Resolution options: accept variance with justification (requires buyer supervisor approval), request vendor credit memo, or reject invoice line
- **SLA**: 5 business days from routing to buyer to resolution

**Quantity Variance (Invoiced ≠ Received)**
- The invoice line is routed to the DC or store receiving team for verification
- Receiving confirms whether the full quantity was physically received but not entered in the system, or if there is a genuine shortage
- If quantity was received but not entered, receiving posts the missing goods receipt retroactively
- If genuine shortage, the buyer negotiates with the vendor for a credit or replacement
- **SLA**: 3 business days from routing to receiving to resolution

**No Goods Receipt Found**
- The invoice is routed to the DC or store receiving team with the PO detail and carrier/shipping information
- Receiving investigates whether the goods were received but not entered, still in transit, or never shipped
- If goods were received, the GR is posted retroactively and the invoice is re-matched
- If goods are in transit, the invoice is placed on hold pending receipt (maximum hold: 30 days)
- If goods were never shipped, the invoice is rejected and returned to the vendor
- **SLA**: 5 business days from routing to receiving to initial investigation response

**Duplicate Invoice**
- The system auto-blocks any invoice where the vendor number + invoice number combination matches a previously processed invoice
- The AP specialist reviews the block to determine if the invoice is truly a duplicate or a re-submission (e.g., corrected invoice)
- If duplicate, the invoice is rejected and the vendor is notified
- If not a duplicate (e.g., different invoice number format, re-issued invoice), the AP specialist releases the block and the invoice proceeds to matching
- **SLA**: 2 business days for AP specialist review

#### Step 4.5 — Invoice Approval

| Attribute | Detail |
|---|---|
| **Swimlane** | System / BUY / DM / VP |
| **System** | Oracle Procurement Cloud Workflow |

**Auto-Approval (Target: 90% of Invoices)**
- Invoices that achieve a complete three-way match within all configured tolerances are automatically approved for payment without manual intervention
- The auto-approval is logged in the Oracle document flow with the match results for audit purposes
- The target auto-approval rate is 90% of all invoices, measured monthly

**Exception Approval**
- Invoices with resolved exceptions that required manual intervention are routed for approval based on the following matrix:

| Invoice Amount | Approver |
|---|---|
| $0 – $5,000 | AP Specialist (with exception resolution documentation) |
| $5,001 – $25,000 | AP Manager |
| $25,001 – $100,000 | Director of Finance or VP |
| Greater than $100,000 | CFO |

- The approver reviews the exception documentation, verifies the resolution, and approves or rejects the invoice
- Rejection requires a written reason and the invoice is returned to the AP specialist for further action

#### Step 4.6 — Approved Invoice Routed to Payment Queue

| Attribute | Detail |
|---|---|
| **Swimlane** | System (Oracle Procurement Cloud / Oracle Financials Cloud) |
| **System** | Oracle Financials Cloud |

Upon approval, the system performs the following:

- The invoice is posted to Oracle Financials Cloud, creating a journal entry that debits the GR/IR clearing account (or expense account for non-inventory items) and credits the vendor's AP subledger account
- The payment due date is calculated based on the invoice date and the vendor's payment terms:
  - Net 60: Due date = Invoice date + 60 calendar days
  - Net 30: Due date = Invoice date + 30 calendar days
  - 2/10 Net 60: Discount eligible if paid by Invoice date + 10 days; otherwise due at Invoice date + 60 days
- The system evaluates early payment discount eligibility and flags invoices where the annualized ROI of taking the discount exceeds 15% (calculation: discount percentage × 365 ÷ (days beyond discount period); e.g., 2/10 Net 60 = 2% × 365 ÷ 50 = 14.6% annualized)
- The invoice is placed in the payment queue with the calculated due date, discount eligibility flag, and discount deadline date
- The AP subledger is updated and the vendor's balance reflects the open invoice

---

### Phase 5: Payment Processing

#### Step 5.1 — Payment Selection

| Attribute | Detail |
|---|---|
| **Swimlane** | APS / System |
| **System** | Oracle Financials Cloud Automatic Payment Program |

**Daily Payment Proposal**
- The Oracle Financials Cloud Payment Program (APP) generates a daily payment proposal at 10:00 AM ET
- The payment proposal selects invoices for payment based on the following criteria:
  - Invoices due within the next 5 business days (to allow for processing and delivery time)
  - Invoices eligible for early payment discount where the discount deadline falls within the next 5 business days and the annualized ROI exceeds 15%
  - Invoices on manual payment hold are excluded unless the hold is released
  - Invoices under dispute are excluded until the dispute is resolved

**Discount Optimization**
- For invoices with 2/10 Net 60 terms, the system calculates the annualized ROI of taking the discount: (0.02 × 365) ÷ (60 − 10) = 14.6%
- When the annualized ROI exceeds BRHI's 15% threshold (or is within 0.5% of the threshold), the discount is taken and the invoice is scheduled for payment within the discount window
- For strategic vendors where BRHI has negotiated enhanced early payment programs (e.g., 2/10 Net 90 = 9.1% annualized), the discount is taken only if the annualized ROI exceeds the 15% threshold

**Payment Proposal Review**
- The AP Manager reviews the daily payment proposal before execution, checking for:
  - Unusual payment amounts or vendors
  - Invoices that should be on hold but were not excluded
  - Duplicate payments flagged by the system
- The AP Manager approves or modifies the payment proposal (removing or adding invoices) and submits it for execution

#### Step 5.2 — Payment Method Selection

| Attribute | Detail |
|---|---|
| **Swimlane** | System / APS |
| **System** | Oracle Financials Cloud |

Payment methods are determined based on vendor preferences, payment amount, and vendor location:

| Payment Method | Volume | Use Case | Processing Time |
|---|---|---|---|
| ACH (Automated Clearing House) | 75% of payments | Preferred method for all domestic vendors with US bank accounts | Same-day or next-day settlement |
| Virtual Card | 5% of payments | For vendors enrolled in BRHI's virtual card program; BRHI earns cashback rebate (1.5% typical) | Same-day authorization |
| Check | 15% of payments | For vendors who do not accept ACH or virtual card; also used for one-time payments and legal settlements | Mailed next business day; 5–7 business days delivery |
| Wire Transfer | 5% of payments | For international vendors, large payments (>$250K), or time-critical payments | Same-day settlement (if initiated before wire cutoff) |

**Method Selection Logic**
- The system selects the payment method based on the vendor master data (maintained payment method preference) and the following rules:
  1. If vendor accepts ACH and has valid bank details on file → ACH
  2. If vendor is enrolled in virtual card program → Virtual Card
  3. If vendor is international or payment >$250K → Wire Transfer
  4. If none of the above → Check

#### Step 5.3 — Payment Execution

| Attribute | Detail |
|---|---|
| **Swimlane** | System / TRS |
| **System** | Oracle Financials Cloud / Banking Portal |

**Batch Processing**
- Payments are processed in a daily batch after the payment proposal is approved by the AP Manager
- **Cutoff time**: 2:00 PM ET — all approved payment proposals submitted before 2:00 PM are processed same-day
- Payment files are generated in the appropriate format:

| Payment Method | File Format | Transmission |
|---|---|---|
| ACH | NACHA CCD+ / CTX | Transmitted to BRHI's bank via secure file transfer (SFTP) |
| Virtual Card | Card network API | Transmitted to card processor for authorization |
| Check | AFP X9.37 / Positive Pay file | Transmitted to bank for positive pay; checks printed on-site |
| Wire Transfer | SWIFT MT103 / FedWire | Transmitted to bank via secure banking portal |

**Settlement Timelines**
- ACH: Same-day (if submitted before bank's ACH cutoff) or next-business-day settlement
- Virtual Card: Same-day authorization and settlement
- Check: Printed and mailed next business day; funds drawn when check is presented (typical float: 5–7 business days)
- Wire Transfer: Same-day settlement if submitted before 3:00 PM ET bank cutoff

**Segregation of Duties**
- The AP specialist who creates the payment proposal cannot be the same person who approves the payment proposal
- The treasury analyst who transmits the payment file to the bank cannot be the same person who created or approved the payment proposal
- Payment file transmission requires dual authentication (maker-checker) in the banking portal for wire transfers

#### Step 5.4 — Payment Confirmation

| Attribute | Detail |
|---|---|
| **Swimlane** | System / APS |
| **System** | Oracle Financials Cloud / SPS Commerce EDI |

**Remittance Advice Transmission**
- After payment execution, remittance advice is sent to the vendor through the following channels:

| Transmission Method | Transaction | Volume |
|---|---|---|
| EDI 820 | ANSI X12 820 Remittance Advice | 75% (EDI-capable vendors) |
| Email | PDF remittance advice emailed to vendor's AR contact | 15% |
| Vendor Portal | Remittance posted to Oracle Procurement Cloud - Sourcing/Supplier Portal vendor portal | 10% |

**EDI 820 Content**
- The EDI 820 includes: payment reference number, payment date, payment amount, payment method, and detail of invoices paid (invoice number, invoice date, gross amount, discount taken, net amount paid)

**Internal Confirmation**
- The system updates the vendor's AP subledger in Oracle Financials Cloud, clearing the paid invoices against the payment document
- The payment status is updated to "Paid" in the PO history and invoice document flow
- The treasury team receives confirmation from the bank (bank statement or API notification) that the payment was successfully processed

#### Step 5.5 — Bank Reconciliation

| Attribute | Detail |
|---|---|
| **Swimlane** | TRS |
| **System** | Oracle Financials Cloud / Bank Statement Import |

**Daily Reconciliation**
- Bank statements are imported into Oracle Financials Cloud daily (electronic bank statement format: BAI2 or MT940)
- The system performs automatic reconciliation (clearing) of:
  - ACH payments: matched on payment reference and amount
  - Wire transfers: matched on wire reference and amount
  - Checks: matched on check number and amount when presented
  - Virtual card payments: matched on card authorization reference and amount

**Exception Resolution**
- Items that do not auto-reconcile are flagged as exceptions and assigned to the treasury analyst for manual investigation:
  - **Unmatched bank debit**: Payment shown on bank statement but not in Oracle Financials Cloud — investigate if payment was processed outside the normal workflow
  - **Unmatched Oracle payment**: Payment recorded in Oracle Financials Cloud but not on bank statement — investigate bank processing delay or rejection
  - **Amount mismatch**: Bank amount differs from Oracle amount — investigate bank fees, partial payments, or processing errors
- **SLA**: All reconciliation exceptions resolved within 5 business days
- The treasury analyst resolves exceptions by posting manual clearing entries or coordinating with the bank

#### Step 5.6 — Vendor Statement Reconciliation

| Attribute | Detail |
|---|---|
| **Swimlane** | APS / APM |
| **System** | Oracle Financials Cloud |

**Monthly Reconciliation**
- Vendor statements are requested from all strategic vendors (top 200 by spend) and all vendors with open balances, on a monthly basis
- The AP team reconciles the vendor's statement balance to BRHI's AP subledger balance for that vendor:
  1. Match all payments made by BRHI to payments shown on the vendor statement
   2. Match all invoices received and posted in Oracle Financials Cloud to invoices shown on the vendor statement
  3. Identify discrepancies: invoices on vendor statement but not in BRHI AP ledger (unreceived invoices), invoices in BRHI AP ledger but not on vendor statement (vendor processing lag), and amount differences

**Discrepancy Investigation and Resolution**
- All discrepancies are logged in the vendor reconciliation workbook and investigated:
  - **Unreceived invoices**: Vendor contacted for copy; invoice processed upon receipt
  - **Unapplied payments**: Vendor contacted to confirm application; BRHI payment details provided
  - **Amount differences**: Root cause identified (pricing dispute, freight charge, tax calculation); buyer or AP specialist resolves with vendor
- **SLA**: All discrepancies investigated and resolved within 10 business days of receipt of the vendor statement
- Unresolved items aging beyond 30 days are escalated to the AP Manager and the buyer for joint resolution

**Reconciliation Reporting**
- Monthly reconciliation status is reported to the Director of Finance, including:
  - Number of vendors reconciled
  - Number and dollar value of discrepancies
  - Aging of unresolved items
  - Root cause analysis and process improvement recommendations

---

## 4. System Landscape

| System | Module / Function | Purpose in P2P Process |
|---|---|---|
| **Oracle Fusion Cloud ERP** | MM (Materials Management) | Purchase requisition, purchase order creation and approval, source determination, goods receipt, invoice verification, vendor master data |
| **Oracle Fusion Cloud ERP** | FI (Financial Accounting) | AP subledger, payment processing, GL posting, bank reconciliation, financial reporting |
| **Manhattan Associates WMS** | Warehouse Management | Pre-receipt planning, physical receipt confirmation, putaway direction, inventory location management |
| **Oracle Procurement Cloud - Sourcing/Supplier Portal** | Vendor Portal | Vendor onboarding, catalog management, PO transmission, invoice submission, vendor communication |
| **SPS Commerce** | EDI Gateway | EDI 850 (PO), EDI 855 (PO Acknowledgment), EDI 856 (ASN), EDI 810 (Invoice), EDI 820 (Remittance) |
| **Oracle EPM Cloud - Analytics** | Procurement Analytics | KPI dashboards, spend analysis, vendor scorecards, P2P cycle time reporting, maverick spend detection |
| **Oracle BI** | Reporting | Historical reporting, trend analysis, audit data extraction |

### System Integration Map

```
Demand Signal → Oracle Procurement Cloud (Requisition) → Oracle Procurement Cloud (PO) → EDI 850 → Vendor
Vendor → EDI 856 (ASN) → Manhattan WMS (Pre-Receipt)
Carrier → Manhattan WMS (Physical Receipt) → Oracle Procurement Cloud (Goods Receipt)
Vendor → EDI 810 (Invoice) → Oracle Procurement Cloud (Invoice Verification) → Oracle Financials Cloud (AP Posting)
Oracle Financials Cloud (Payment Program) → Bank → EDI 820 (Remittance) → Vendor
Oracle Financials Cloud → Bank Statement → Oracle Financials Cloud (Bank Reconciliation)
All Systems → Oracle EPM Cloud - Analytics (Reporting)
```

---

## 5. Business Rules

| Rule ID | Rule Description |
|---|---|
| BR-P2P-001 | A purchase order is mandatory for all purchases exceeding $500. Purchases under $500 may be made via P-Card per the P-Card policy. |
| BR-P2P-002 | Three-way match (PO, goods receipt, and invoice) is required for all merchandise purchases regardless of value. |
| BR-P2P-003 | Two-way match (PO and invoice) is acceptable for service purchases under $5,000 with department manager approval. The manager must confirm service delivery via email or system acknowledgment before invoice approval. |
| BR-P2P-004 | Vendor invoices must be received within 120 days of the PO date. Invoices received after 120 days are placed on hold and the buyer is contacted to confirm whether the obligation is still valid. If confirmed, the invoice is processed with buyer and AP Manager approval. |
| BR-P2P-005 | Early payment discount of 2/10 Net 60: BRHI will take the early payment discount when the annualized ROI exceeds 15%. The annualized ROI is calculated as: (Discount % × 365) ÷ (Days beyond discount period). |
| BR-P2P-006 | Standard payment terms: Net 60 for merchandise purchases, Net 30 for services, Net 45 for construction. Non-standard terms require CFO approval during vendor contract review. |
| BR-P2P-007 | Debit balances (overpayments, credit memos exceeding open invoices) are automatically applied to the vendor's next scheduled payment. The AP system identifies debit balances daily and applies them before payment execution. |
| BR-P2P-008 | Vendor credit memos must be applied within 90 days of receipt. Credit memos aging beyond 90 days are escalated to the AP Manager for resolution and reported to the Director of Finance. |
| BR-P2P-009 | New vendor setup requires dual approval: the AP Manager must approve the vendor master data creation, and the Procurement Manager must approve the vendor's qualifications, insurance, and business terms. Both approvals must be documented in the vendor master record. |
| BR-P2P-010 | Vendor bank detail changes (adding, modifying, or removing bank account information) require dual approval (AP Manager + Treasury Manager) and callback verification. The AP specialist must call the vendor's verified phone number (on file, not from the change request) and verbally confirm the bank detail change before it is activated in the system. |

---

## 6. Key Performance Indicators (KPIs)

| KPI | Definition | Target | Measurement Frequency | Data Source |
|---|---|---|---|---|
| PO Cycle Time | Average business days from requisition creation to PO release (approval) | 3 business days | Weekly | Oracle Procurement Cloud |
| Three-Way Match Auto-Match Rate | Percentage of invoices that achieve automatic three-way match without manual intervention | 90% | Monthly | Oracle Procurement Cloud / Oracle Financials Cloud |
| On-Time Payment Percentage | Percentage of invoices paid by the due date (or within discount window) | 98% | Monthly | Oracle Financials Cloud |
| Early Payment Discount Capture | Percentage of available early payment discounts actually captured | 85% | Monthly | Oracle Financials Cloud |
| Cost Per Invoice Processed | Total AP department cost (labor + technology + overhead) divided by total invoices processed | < $5.00 | Monthly | Finance / Oracle Financials Cloud |
| Maverick Spend (Off-Contract) | Percentage of total procurement spend made outside of contracted/preferred vendors | < 5% | Monthly | Oracle Procurement Cloud / Oracle EPM Cloud - Analytics |
| Supplier On-Time Delivery | Percentage of PO lines delivered on or before the confirmed delivery date | 95% | Monthly | Oracle Procurement Cloud / WMS |
| Days Payable Outstanding (DPO) | Average number of days from goods receipt to payment: (Accounts Payable ÷ Cost of Goods Sold) × Days in Period | 55 days | Monthly | Oracle Financials Cloud |
| AP Aging (>90 Days) | Percentage of total AP balance that is older than 90 days | < 5% | Monthly | Oracle Financials Cloud |
| Invoice Processing Time | Average business days from invoice receipt to invoice approval (ready for payment) | 3 business days | Monthly | Oracle Procurement Cloud |

### KPI Reporting and Governance

- KPIs are reported monthly via the Oracle EPM Cloud - Analytics Procurement Dashboard
- The Director of Procure-to-Pay Operations reviews KPIs weekly with the AP and Procurement teams
- The CFO reviews P2P KPIs monthly as part of the financial operations review
- KPIs that fall below target for two consecutive months trigger a root cause analysis and corrective action plan, documented and reviewed with the process owner

---

## 7. Controls and Compliance

### 7.1 SOX Controls — Segregation of Duties

The following segregation of duties (SoD) rules are enforced across the P2P process to comply with Sarbanes-Oxley (SOX) requirements:

| Control | Rule | Enforced By |
|---|---|---|
| Requisition-to-Approval | The associate who creates a purchase requisition cannot be the same person who approves that requisition or the resulting purchase order. | Oracle Procurement Cloud workflow configuration (role-based exclusion) |
| Receipt-to-Invoice | The associate who enters the goods receipt in Oracle Procurement Cloud cannot be the same person who approves the corresponding vendor invoice. | Oracle Procurement Cloud role design (mutually exclusive roles) |
| Invoice-to-Payment | The associate who approves an invoice cannot be the same person who executes the payment (creates or approves the payment proposal). | Oracle Financials Cloud role design (mutually exclusive roles) |
| Vendor Master | The associate who creates a new vendor master record cannot be the same person who approves it. Dual approval required. | Oracle Procurement Cloud vendor master workflow |

SoD conflicts are monitored quarterly by Internal Audit using Oracle Risk Management Cloud. Any identified conflicts are remediated within 30 days.

### 7.2 Duplicate Payment Detection

| Control | Description |
|---|---|
| Automated Daily Scan | The Oracle system performs a daily scan of all posted invoices to identify potential duplicates based on: vendor number + invoice number, vendor number + invoice amount + invoice date, and PO number + invoice amount. Potential duplicates are flagged and routed to the AP specialist for review. |
| Monthly Manual Review | The AP Manager performs a monthly manual review of high-risk payments (invoices >$10,000, vendors with high invoice volume, and payments made outside normal terms) to identify duplicates that may not have been caught by the automated scan. |
| Recovery | Confirmed duplicate payments are reported to the vendor with a request for refund or credit memo. Recovery is tracked in the duplicate payment register and reported to the Director of Finance monthly. |

### 7.3 Vendor Master Data Controls

| Control | Description |
|---|---|
| New Vendor Setup — Dual Approval | All new vendor master records require approval from both the AP Manager (validating financial and compliance data) and the Procurement Manager (validating business qualifications). Approvals are captured electronically in the vendor master workflow. |
| Bank Detail Changes — Dual Approval + Callback | Any change to vendor banking details (new bank account, changed account number, changed routing number) requires: (1) dual approval by AP Manager and Treasury Manager in Oracle Financials Cloud, and (2) callback verification by the AP specialist calling the vendor's verified phone number on file to verbally confirm the change. The callback must be documented with date, time, and name of vendor representative confirmed. |
| Quarterly Vendor Master Review | The AP Manager conducts a quarterly review of the vendor master file to identify and remediate: duplicate vendor records (based on tax ID, name, or address matching), inactive vendors (no transactions in 24 months — flagged for deactivation), and vendors with incomplete or outdated information (missing tax ID, expired insurance, outdated contacts). Results are documented and remediation actions tracked. |

### 7.4 P-Card Controls

| Control | Limit / Rule |
|---|---|
| Per-Transaction Limit | $2,500 maximum per transaction |
| Monthly Spending Limit | $10,000 maximum per cardholder per calendar month |
| Restricted MCC Codes | Transactions blocked for the following Merchant Category Codes: gambling (7995), jewelry (5094), travel/airlines (unless pre-approved by VP), and any MCC flagged on the restricted list maintained by Treasury |
| Monthly Reconciliation | Each cardholder must reconcile all transactions in the P-Card system within 10 business days of the monthly statement date. Reconciliation includes matching each transaction to a receipt and assigning a valid GL account and cost center. |
| Supervisor Approval | The cardholder's direct supervisor must review and approve all reconciled transactions within 5 business days of the cardholder's reconciliation completion. |
| Audit Sampling | Internal Audit samples 10% of P-Card transactions monthly for detailed review, including verification of receipts, business purpose, and policy compliance. |

### 7.5 Continuous Monitoring

| Control | Description |
|---|---|
| Monthly AP Audit Sampling | Internal Audit samples 10% of all payments exceeding $10,000 each month. The sample is reviewed for: proper approval, accurate three-way match, correct account coding, compliance with payment terms, and adherence to SoD rules. Findings are reported to the CFO and Audit Committee. |
| Quarterly Analytics for Anomalous Patterns | The Internal Audit team uses data analytics tools to perform quarterly analysis of AP data for anomalous patterns including: vendor addresses matching employee addresses, vendors with payments to multiple bank accounts, rapid succession payments to the same vendor near period-end, unusual payment terms or methods, and vendors with invoice volumes or amounts significantly above historical averages. Anomalous findings are investigated and reported to the CFO. |

---

## 8. Exception Handling

| Exception | Description | Resolution Steps | Responsible Party | SLA |
|---|---|---|---|---|
| **Price Variance** | Invoice unit price exceeds PO price by >$50 or >2% per line | 1. System auto-routes to buyer. 2. Buyer reviews PO contract pricing vs. invoiced price. 3. Buyer contacts vendor for explanation. 4. Resolution: accept with justification (supervisor approval), request credit memo, or reject line. | Buyer | 5 business days |
| **Quantity Variance** | Invoiced quantity differs from goods receipt quantity by >5% | 1. System routes to receiving team. 2. Receiving verifies physical count vs. system entry. 3. If under-received, GR is corrected. 4. If genuine shortage, buyer contacts vendor for credit or replacement. | Receiving Associate / Buyer | 3 business days |
| **No Goods Receipt** | Invoice references a PO for which no goods receipt exists in Oracle Procurement Cloud | 1. System routes to DC/store receiving. 2. Receiving investigates shipment status (in transit, not shipped, received but not entered). 3. If received, GR posted retroactively. 4. If in transit, invoice held (max 30 days). 5. If never shipped, invoice rejected. | Receiving Associate / Buyer | 5 business days |
| **Duplicate Invoice** | Invoice number + vendor number matches a previously processed invoice | 1. System auto-blocks invoice. 2. AP specialist reviews to confirm duplicate vs. re-submission. 3. If duplicate, invoice rejected and vendor notified. 4. If re-submission, block released and invoice processed. | AP Specialist | 2 business days |
| **Vendor Dispute** | Vendor disputes a payment, short payment, or deduction taken by BRHI | 1. Vendor contacts AP or buyer with dispute details. 2. AP specialist logs dispute in the dispute tracker. 3. AP specialist and buyer jointly investigate (review PO, GR, invoice, payment records). 4. If BRHI error, corrective payment or credit memo issued. 5. If vendor error, documentation provided to vendor. 6. Resolution documented and dispute closed. | AP Specialist / Buyer | 10 business days |
| **Credit Memo** | Vendor issues a credit memo for returned goods, damaged goods, pricing adjustment, or promotional allowance | 1. Credit memo received (EDI, portal, or mail). 2. AP specialist validates credit memo against supporting documentation (return authorization, damage report, pricing agreement). 3. Credit memo posted to vendor AP subledger. 4. Credit memo applied to next payment or open invoice. 5. If credit memo is not applied within 90 days, escalated to AP Manager. | AP Specialist | Applied within 90 days |

---

## 9. Process Interfaces

The P2P process integrates with the following BRHI business processes and systems:

### Inventory Management

- **Goods Receipt → Inventory Update**: When a goods receipt is posted in Oracle Procurement Cloud (movement type 101), the system automatically updates the inventory quantity and value in the material master. This triggers real-time inventory availability updates for customer order fulfillment, store replenishment, and intercompany transfers.
- **Returns to Vendor → Inventory Decrease**: When goods are returned to vendor (movement type 122), the system reduces inventory and reverses the GR/IR entry.

### Vendor Management

- **Vendor Performance Scorecards**: The P2P process feeds data to the vendor management process for performance measurement. Key data points include: on-time delivery (PO confirmed date vs. actual GR date), quality inspection pass rate, invoice accuracy rate, and responsiveness to issue resolution.
- **Scorecard Data Flow**: Oracle Procurement Cloud and WMS data are extracted weekly and loaded into Oracle EPM Cloud - Analytics, where vendor scorecards are calculated and published. Scorecards are reviewed monthly in the vendor business review meetings led by the Procurement team.

### Accounting (General Ledger)

- **GL Posting — Goods Receipt**: The GR posting creates a journal entry debiting the inventory account (BS) and crediting the GR/IR clearing account (BS).
- **GL Posting — Invoice Receipt**: The invoice posting creates a journal entry debiting the GR/IR clearing account (BS) and crediting the vendor AP subledger (BS), with tax postings to the appropriate tax liability accounts.
- **GL Posting — Payment**: The payment posting creates a journal entry debiting the vendor AP subledger (BS) and crediting the cash/bank account (BS).
- **Accruals**: At month-end, the AP team reviews the GR/IR clearing account for goods received but not yet invoiced (GR/IR imbalance). An accrual is posted for the estimated invoice value of un-invoiced receipts using the GR/IR balance as the basis.
- **Revaluation**: Foreign currency vendor balances are revalued at month-end using the closing exchange rate, with FX gains/losses posted to the appropriate income statement accounts.

### Treasury

- **Payment Execution**: Treasury is responsible for the final transmission of payment files to the bank and ensuring that bank balances are sufficient to cover the daily payment run. Treasury manages the BRHI cash position forecast, which is updated daily based on the scheduled payment run and expected receipts.
- **Bank Reconciliation**: Treasury performs daily bank reconciliation as described in Step 5.5, ensuring all payments are properly cleared and bank balances are accurate.
- **Cash Management**: Treasury provides the daily cash position to the AP team to ensure payment proposals are aligned with available cash. If a cash shortfall is projected, Treasury may request the AP team to defer non-critical payments.

### Receiving and Warehouse Operations

- **Physical Receipt Confirmation**: The DC or store receiving team confirms the physical receipt of goods in the WMS, which feeds the goods receipt into Oracle Procurement Cloud. Accurate and timely receipt entry is critical for the three-way match process and for maintaining inventory accuracy.
- **Putaway and Inventory Availability**: The WMS-directed putaway process ensures that received goods are stored in the correct location and are available for order fulfillment within 24 hours. Putaway confirmation triggers the WMS inventory update and confirms the location of the goods for subsequent picking and shipping.

---

## 6. AI and Automation Enhancements

### 6.1 Oracle AI Agent Integration

#### 6.1.1 Procurement AI Agents

| AI Agent | Current Capability | Oracle AI Enhancement | Business Impact |
|---|---|---|---|
| **Sourcing Agent** | Manual supplier evaluation | AI-powered supplier scoring based on cost, quality, delivery, risk | 30% faster sourcing decisions |
| **Spend Analytics Agent** | Manual spend classification | AI automatic spend classification across 10,000+ suppliers | $50M+ annual savings identification |
| **Contract Agent** | Manual contract review | AI contract risk assessment and term optimization | 40% faster contract cycles |
| **Invoice Agent** | Manual invoice processing | AI invoice data extraction and validation | 95% straight-through processing |

#### 6.1.2 AI-Powered Procurement Process

**Requisition Intelligence:**
- **Smart Recommendations**: AI suggests optimal quantities based on historical usage, seasonality, and promotions
- **Substitution Suggestions**: AI recommends alternative products when preferred items are unavailable
- **Budget Optimization**: AI validates requisitions against available budget and suggests alternatives

**Supplier Intelligence:**
- **Performance Prediction**: AI predicts supplier performance based on historical data and market conditions
- **Risk Monitoring**: Real-time AI monitoring of supplier financial health, news, and geopolitical risks
- **Price Optimization**: AI analyzes market pricing to ensure competitive purchasing

**Invoice Intelligence:**
- **Touchless Processing**: AI extracts data from invoices with 95%+ accuracy
- **Exception Handling**: AI categorizes and routes exceptions for optimal resolution
- **Early Payment Optimization**: AI recommends optimal payment timing for cash flow and discounts

### 6.2 Process Automation Opportunities

#### 6.2.1 Current vs. AI-Enhanced Process

| Process Step | Current State | AI-Enhanced State | Time Savings |
|---|---|---|---|
| **Requisition Creation** | Manual item selection | AI-suggested items and quantities | 60% |
| **Supplier Selection** | Manual evaluation | AI-scored supplier recommendations | 70% |
| **PO Creation** | Manual PO generation | AI-generated POs with optimal terms | 50% |
| **Invoice Processing** | Manual data entry | AI-extracted and validated invoices | 80% |
| **Payment Optimization** | Scheduled payment runs | AI-optimized payment timing | 40% |

#### 6.2.2 Expected Benefits

| Metric | Current | AI-Enhanced | Improvement |
|---|---|---|---|
| **Procurement Cycle Time** | 14 days | 7 days | 50% reduction |
| **Invoice Processing Time** | 5 days | 1 day | 80% reduction |
| **Straight-Through Processing** | 40% | 95% | 138% increase |
| **Savings Identified** | $20M annually | $50M annually | 150% increase |
| **Policy Compliance** | 85% | 99% | 16% increase |

### 6.3 AI Implementation Roadmap

#### Phase 1 (FY2026): Invoice Automation
- Deploy Oracle Payables AI Agent for invoice processing
- Implement touchless invoice processing for high-volume suppliers
- Deploy AI-powered exception handling
- **Target:** 70% straight-through invoice processing

#### Phase 2 (FY2027): Sourcing Optimization
- Deploy Oracle Sourcing AI Agent for supplier evaluation
- Implement AI-powered spend analytics and savings identification
- Deploy contract risk assessment AI
- **Target:** 30% reduction in sourcing cycle time

#### Phase 3 (FY2028): Full Automation
- Deploy AI-powered requisition intelligence
- Implement predictive supplier performance management
- Deploy autonomous procurement for routine purchases
- **Target:** 95% straight-through processing, autonomous procurement

### 6.4 AI Governance for Procurement

#### 6.4.1 AI Decision Authority Matrix

| Decision Type | AI Authority | Human Authority | Escalation |
|---|---|---|---|
| **PO Creation (< $10,000)** | Full AI authority | Review only | Unusual patterns |
| **PO Creation ($10,000-$50,000)** | AI recommendation | Human approval | High-risk suppliers |
| **PO Creation (> $50,000)** | AI analysis only | Full human approval | Always |
| **Supplier Selection** | AI scoring | Human final decision | New suppliers |
| **Contract Terms** | AI suggestions | Human negotiation | Non-standard terms |

#### 6.4.2 AI Monitoring and Oversight

1. **Performance Monitoring**: Daily monitoring of AI accuracy and performance
2. **Bias Testing**: Quarterly testing for supplier selection bias
3. **Audit Trail**: Complete audit trail of AI recommendations and decisions
4. **Human Override Tracking**: Monitor and analyze human overrides of AI recommendations

---

## Appendix A: Approval Authority Matrix Summary

### Requisition Approval

| Threshold | Approver |
|---|---|
| < $5,000 | Requesting Associate + Supervisor |
| $5,000 – $25,000 | Department Manager |
| $25,001 – $100,000 | Vice President |
| > $100,000 | SVP + CFO |

### Purchase Order Approval (Merchandise)

| Threshold | Approver |
|---|---|
| $0 – $5,000 | Buyer |
| $5,001 – $50,000 | Divisional Merchandise Manager |
| $50,001 – $250,000 | VP Merchandising |
| $250,001 – $1,000,000 | SVP Merchandising |
| > $1,000,000 | CMO |

### Purchase Order Approval (Capital)

| Threshold | Approver |
|---|---|
| $0 – $50,000 | Department VP |
| $50,001 – $250,000 | Department VP + CFO |
| $250,001 – $1,000,000 | SVP + CFO |
| > $1,000,000 | CEO + CFO |

### Invoice Exception Approval

| Threshold | Approver |
|---|---|
| $0 – $5,000 | AP Specialist (with documentation) |
| $5,001 – $25,000 | AP Manager |
| $25,001 – $100,000 | Director of Finance or VP |
| > $100,000 | CFO |

---

## Appendix B: EDI Transaction Reference

| Transaction | Description | Direction | Timing |
|---|---|---|---|
| EDI 850 | Purchase Order | BRHI → Vendor | Upon PO release |
| EDI 855 | Purchase Order Acknowledgment | Vendor → BRHI | Within 48 hours of PO receipt |
| EDI 856 | Advance Shipment Notice (ASN) | Vendor → BRHI | 24–48 hours before shipment arrival |
| EDI 810 | Invoice | Vendor → BRHI | Upon shipment or per agreed billing schedule |
| EDI 820 | Remittance Advice | BRHI → Vendor | Upon payment execution |

---

## Appendix C: Glossary

| Term | Definition |
|---|---|
| ACH | Automated Clearing House — electronic funds transfer system for domestic payments |
| AQL | Acceptable Quality Level — statistical sampling method for quality inspection |
| ASN | Advance Shipment Notice — EDI 856 document providing shipment details prior to arrival |
| BOL | Bill of Lading — carrier document detailing shipment contents |
| DPO | Days Payable Outstanding — average days from receipt to payment |
| DDP | Delivered Duty Paid — Incoterm where vendor delivers to buyer's location |
| EDI | Electronic Data Interchange — standardized electronic document exchange |
| FOB | Free on Board — Incoterm defining point of risk transfer |
| FIFO | First In, First Out — inventory rotation method |
| GL | General Ledger — master financial record |
| GR/IR | Goods Receipt / Invoice Receipt — Oracle clearing account for matched receipts and invoices |
| Incoterms | International Commercial Terms — standardized trade terms published by ICC |
| MRO | Maintenance, Repair, and Operations — non-merchandise supplies |
| OS&D | Overage, Shortage, and Damage — report documenting receipt discrepancies |
| OTB | Open-to-Buy — merchandise budget available for purchasing |
| P2P | Procure-to-Pay — end-to-end procurement and payment process |
| PO | Purchase Order — legally binding procurement document |
| SLA | Service Level Agreement — defined performance commitment |
| SoD | Segregation of Duties — internal control requiring task separation |
| SOX | Sarbanes-Oxley Act — federal law requiring financial internal controls |
| WBS | Work Breakdown Structure — project cost element in Oracle Financials Cloud |
| WMS | Warehouse Management System — system directing warehouse operations |
