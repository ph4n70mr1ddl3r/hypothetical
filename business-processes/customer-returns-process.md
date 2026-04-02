# Customer Returns and Exchange Process

**BuildRight Home Improvement, Inc. (BRHI)**

---

## 1. Document Control

| Field | Detail |
|---|---|
| **Document ID** | BRHI-BP-003 |
| **Version** | 3.2 |
| **Effective Date** | January 1, 2026 |
| **Last Revised** | November 14, 2025 |
| **Process Owner** | Vice President, Customer Care |
| **Approved By** | Sarah Mitchell, SVP Store Operations |
| **Review Cycle** | Annual (next review: December 2026) |
| **Classification** | Internal — All Associates |
| **Supersedes** | BRHI-BP-003 v3.1 (March 2025) |

### Revision History

| Version | Date | Author | Description |
|---|---|---|---|
| 1.0 | 2019-06-01 | J. Alvarez | Initial release |
| 2.0 | 2021-01-15 | M. Chen | Added online return procedures; updated authorization tiers |
| 2.1 | 2022-04-10 | M. Chen | Revised fraud detection rules; added serial verification |
| 3.0 | 2024-03-01 | R. Okonkwo | Expanded to include RTV and disposition workflows |
| 3.1 | 2025-03-15 | R. Okonkwo | Updated BuildRight brand return window to 365 days |
| 3.2 | 2025-11-14 | R. Okonkwo | Added hazmat exclusions; updated KPI targets |

---

## 2. Process Overview

### 2.1 Purpose

This document defines the end-to-end process for handling customer-initiated returns, exchanges, and refunds at all BRHI retail locations and through the BRHI e-commerce channel. It ensures consistent, policy-compliant, and customer-friendly resolution of return requests while protecting the company against fraud and minimizing inventory shrinkage.

### 2.2 Scope

This process covers:

- In-store returns and exchanges at all 187 BRHI retail locations
- Online orders returned in-store or via mail
- Returns of BRHI private-label (BuildRight brand) products
- Returns of national-brand merchandise
- Vendor-returnable (RTV) disposition of returned goods
- Special-case returns including contractor/Pro account returns and hazardous materials

This process does **not** cover:

- Vendor-initiated recalls (see BRHI-BP-011, Product Recall Process)
- Warranty claims processed through third-party providers
- Employee merchandise adjustments (see BRHI-BP-012, Internal Inventory Adjustments)

### 2.3 Process Boundaries

- **Start:** Customer presents a return request (in-store at Service Desk or via online portal).
- **End:** Refund is issued to the customer, returned item is dispositioned, and financial reconciliation is recorded.

### 2.4 Oracle Fusion Cloud ERP Integration

**Oracle Modules Involved in Returns Process:**

| Oracle Module | Returns Process Function | Data Flow |
|---|---|---|
| **Oracle Financials Cloud** | Refund processing, credit memos, financial reconciliation | POS → Oracle Financials Cloud |
| **Oracle SCM Cloud** | Inventory updates, RTV processing, vendor chargebacks | WMS → Oracle SCM Cloud |
| **Oracle Customer Experience Cloud** | Customer return history, complaint tracking | BRHI.com → Oracle CX Cloud |
| **Oracle Analytics Cloud** | Returns analytics, trend reporting | All systems → Oracle Analytics Cloud |

**Key Integration Points:**

1. **POS to Oracle Financials Cloud Integration:**
   - All in-store returns generate real-time journal entries in Oracle Financials Cloud
   - Refund transactions update customer accounts receivable and cash accounts
   - Credit memos are automatically created for approved returns

2. **OMS/WMS to Oracle SCM Cloud Integration:**
   - Returned inventory updates are synchronized with Oracle SCM Cloud
   - RTV (Return to Vendor) authorizations flow from Oracle SCM Cloud to vendor systems
   - Inventory disposition decisions are recorded in Oracle SCM Cloud

3. **Oracle AI-Powered Returns Analytics:**
   - Machine learning models identify return fraud patterns
   - Predictive analytics forecast return rates by product category
   - Automated root cause analysis for defective product trends

---

## 3. SIPOC Analysis

| Category | Details |
|---|---|
| **Suppliers** | Customers (returning merchandise), Cashiers, Service Desk Associates, Online Returns Center, Delivery Drivers (pickup returns), Vendors (RTV credits) |
| **Inputs** | Returned merchandise, Sales receipt (paper or digital), Order confirmation number, Customer identification, Original payment instrument, Return reason code, Product serial number (if applicable) |
| **Process** | Return Initiation → Return Validation → Return Authorization → Refund Processing → Item Disposition → Financial Reconciliation |
| **Outputs** | Refund issued (cash, card credit, store credit), Exchange merchandise provided, Return receipt, Updated inventory record, Vendor chargeback request, Damaged goods report, Restocked product |
| **Customers** | Returning customer (refund/exchange), Store operations (inventory accuracy), Finance (reconciliation data), Vendors (RTV notification), Merchandising team (defect trend data) |

---

## 4. Process Steps

### Phase 1: Return Initiation

**Objective:** Capture the return request, identify the customer, and begin the return workflow.

#### 1.1 In-Store Return Initiation

| Step | Action | Role | System |
|---|---|---|---|
| 1.1.1 | Customer approaches Service Desk or any open register with item(s) to return. Greeter may direct customer to Service Desk for non-standard returns. | Customer / Greeter | — |
| 1.1.2 | Associate greets customer and asks for receipt. If customer has receipt, proceed to Phase 2. | Service Desk Associate / Cashier | — |
| 1.1.3 | If no receipt, associate explains that a receipt lookup can be performed (see Step 2.2) and that a valid government-issued photo ID is required for all no-receipt returns. | Service Desk Associate | — |
| 1.1.4 | Associate selects "New Return" in POS and scans item barcode(s). POS displays item description, current retail price, and original sale price (if receipt is provided). | Service Desk Associate / Cashier | POS |

#### 1.2 Online Return Initiation

| Step | Action | Role | System |
|---|---|---|---|
| 1.2.1 | Customer logs into BRHI.com account, navigates to Order History, and selects "Return Item(s)" on the relevant order. | Customer | BRHI.com |
| 1.2.2 | Customer selects return reason from dropdown (defective, wrong item, changed mind, found better price, damaged in shipping, other) and adds optional comments. | Customer | BRHI.com |
| 1.2.3 | System displays return eligibility status and estimated refund amount. Customer selects return method: **In-Store Drop-off** or **Prepaid Mail Return** (FedEx label generated). | Customer | BRHI.com |
| 1.2.4 | If In-Store Drop-off: customer receives QR code and confirmation email. If Mail Return: customer receives prepaid shipping label via email and is instructed to package item securely. | System (automated) | BRHI.com / OMS |
| 1.2.5 | For mail returns, the Online Returns Center receives the package, scans the RMA barcode, and proceeds to Phase 2 validation. | Returns Center Associate | OMS / WMS |

---

### Phase 2: Return Validation

**Objective:** Verify the purchase, confirm return eligibility, and assess item condition.

#### 2.1 Receipt-Based Purchase Verification

| Step | Action | Role | System |
|---|---|---|---|
| 2.1.1 | Associate scans the barcode on the printed receipt. POS retrieves the original transaction, displaying: items purchased, date, payment method, transaction number, and store location. | Cashier / Service Desk Associate | POS |
| 2.1.2 | Associate confirms the returned item SKU matches a SKU on the original receipt. If multiple quantities of the same SKU were purchased, associate confirms the quantity being returned does not exceed the quantity on the receipt. | Cashier / Service Desk Associate | POS |
| 2.1.3 | POS automatically checks the return eligibility time window based on product category (see Section 5, Return Policy Details) and displays PASS or FAIL. | System (automated) | POS |

#### 2.2 No-Receipt Purchase Verification

| Step | Action | Role | System |
|---|---|---|---|
| 2.2.1 | Associate requests customer's government-issued photo ID (driver's license, state ID, passport, or military ID). Associate enters or scans the ID into POS. | Service Desk Associate | POS |
| 2.2.2 | Associate performs **Receipt Lookup** using one of the following methods: credit/debit card swipe, Pro account number, phone number on file, or transaction date + store location range. | Service Desk Associate | POS |
| 2.2.3 | If the original transaction is located, proceed as receipt-based (Step 2.1). If the transaction cannot be located, the return proceeds as a **No-Receipt Return** subject to Section 6 Business Rules. | Service Desk Associate | POS |
| 2.2.4 | POS checks the customer's no-receipt return history using the ID number. The system enforces the following limits: no more than 3 no-receipt returns in a rolling 90-day period and no more than $150 aggregate value in no-receipt returns in a rolling 12-month period. | System (automated) | POS / CRM |

#### 2.3 Pro Account Verification

| Step | Action | Role | System |
|---|---|---|---|
| 2.3.1 | If customer presents a BRHI Pro Account card or provides Pro account number, associate enters it in POS. Pro account returns receive an extended 120-day standard return window and dedicated account history for lookups. | Service Desk Associate | POS / Pro CRM |
| 2.3.2 | Associate verifies the Pro account is in good standing (not suspended or in collections). Returns on delinquent accounts require Manager approval. | Service Desk Associate | POS / Pro CRM |

#### 2.4 Item Condition Assessment

| Step | Action | Role | System |
|---|---|---|---|
| 2.4.1 | Associate visually inspects the returned item for completeness: all original parts, accessories, manuals, and packaging must be present unless the return reason is "defective." | Cashier / Service Desk Associate | — |
| 2.4.2 | Associate categorizes item condition using one of the following codes: **A — Like New / Resalable** (unopened or opened but complete and undamaged), **B — Open Box / Acceptable** (opened, possibly missing minor packaging, but fully functional), **C — Damaged / Defective** (broken, missing parts, or non-functional), **D — Used / Worn** (evidence of extended use beyond testing). | Cashier / Service Desk Associate | POS |
| 2.4.3 | For electronics and power tools ($50+), associate verifies the serial number on the item matches the serial number recorded at the time of original sale. If no serial was recorded at sale, associate records the serial number now. See Step 4.3 for fraud detection. | Service Desk Associate | POS / Inventory |
| 2.4.4 | For items containing hazardous materials (paint, chemicals, propane tanks, pesticides, adhesives), associate follows Hazmat Return Protocol: item is not returned to sales floor and is routed directly to the Hazmat Holding Area in Receiving. See Section 6.5. | Service Desk Associate | — |

#### 2.5 Return Eligibility Determination

| Step | Action | Role | System |
|---|---|---|---|
| 2.5.1 | POS evaluates the return against all policy rules: time window, category restrictions, condition requirements, and receipt status. System returns one of the following statuses: **ELIGIBLE**, **ELIGIBLE WITH RESTOCKING FEE**, **ELIGIBLE WITH MANAGER APPROVAL**, or **NOT ELIGIBLE**. | System (automated) | POS |
| 2.5.2 | If **NOT ELIGIBLE**, associate explains the reason to the customer and offers alternatives where possible (e.g., manufacturer warranty contact, exchange only). Associate may escalate to the MOD for a policy exception. | Service Desk Associate | — |
| 2.5.3 | If **ELIGIBLE WITH RESTOCKING FEE**, associate informs customer of the fee amount (see Section 5.4) and proceeds to Phase 3. | Service Desk Associate | POS |

---

### Phase 3: Return Authorization

**Objective:** Obtain the correct level of approval, perform fraud screening, and authorize the return.

#### 3.1 Authorization Level Matrix

| Return Value (Pre-Tax) | Required Authorizer | Authorization Method |
|---|---|---|
| $0.01 – $50.00 | Cashier (self-authorized) | Cashier enters own ID; POS logs auto-approval |
| $50.01 – $200.00 | Shift Supervisor | Supervisor swipes ID badge or enters credentials at POS |
| $200.01 – $1,000.00 | Department Manager or Assistant Store Manager | Manager swipes ID badge at POS; receives POS alert for approval |
| $1,000.01+ | Store Manager (or ASM if SM is off-site) | Store Manager reviews transaction details on POS or mobile device; approves via dual-key entry |
| Any value, no receipt, over policy limit | Store Manager only | Manual override with documented reason code; see Section 6.1 |

| Step | Action | Role | System |
|---|---|---|---|
| 3.1.1 | After validation is complete, POS calculates the refund subtotal (original purchase price, less any restocking fee) and displays the required authorization level. | System (automated) | POS |
| 3.1.2 | If the return exceeds the current associate's authorization level, POS prompts for the appropriate authorizer. Associate pages or calls the authorizer to the register. | Cashier / Service Desk Associate | POS |
| 3.1.3 | Authorizer reviews the return details on screen (item, condition code, reason, receipt status, refund amount) and approves or denies. If denied, authorizer provides reason and associate communicates to customer. | Supervisor / Manager | POS |
| 3.1.4 | Approved authorizations are logged in the POS audit trail with authorizer ID, timestamp, and return transaction number. | System (automated) | POS |

#### 3.2 Fraud Detection Check

| Step | Action | Role | System |
|---|---|---|---|
| 3.2.1 | POS automatically performs the following fraud checks before authorization: **Return Frequency** — more than 5 returns in the past 30 days or 12 returns in the past 90 days by the same customer (matched by ID, Pro account, or credit card); **Pattern Analysis** — repeated returns of the same high-value SKU; **Price Discrepancy** — current retail price significantly higher than original purchase price, suggesting receipt fraud; **Serial Number Mismatch** — serial number on returned item does not match serial number recorded at sale. | System (automated) | POS / Fraud Engine |
| 3.2.2 | If any fraud indicator triggers, POS flags the return with a **FRAUD ALERT** and requires Store Manager authorization regardless of dollar value. The return is NOT blocked outright; the Store Manager reviews the full context. | System (automated) | POS / Fraud Engine |
| 3.2.3 | Store Manager reviews the customer's return history, the specific fraud trigger, and the current return details. Manager may: approve the return (with documentation of reason), deny the return (explain to customer), or escalate to the Loss Prevention team. | Store Manager | POS / LP Portal |
| 3.2.4 | If escalated, Loss Prevention reviews the case within 24 hours. Customer is given a return claim ticket and contacted by LP within 2 business days. | Loss Prevention Analyst | LP Portal |
| 3.2.5 | All fraud-flagged returns are included in the weekly Loss Prevention Exception Report sent to the Regional LP Manager. | System (automated) | LP Portal / Reporting |

---

### Phase 4: Refund Processing

**Objective:** Issue the refund to the customer using the appropriate method and complete the return transaction.

#### 4.1 Refund Method Selection

| Refund Method | When Used | Processing Details |
|---|---|---|
| **Original Tender** (preferred) | Receipt-based returns within policy window | Refund to the same credit/debit card, cash, or check used for the original purchase. If original card is unavailable, store credit is offered. |
| **Store Credit** (BRHI Merchandise Credit Card) | No-receipt returns, returns after policy window with manager approval, or customer preference | Issued as a physical BRHI Merchandise Credit Card loaded with the refund amount. No expiration date. Usable at any BRHI location or on BRHI.com. |
| **Exchange** (even or uneven trade) | Customer selects replacement merchandise | Customer selects new item(s). If even exchange (same price), no payment required. If uneven, customer pays difference or receives merchandise credit for the balance. |
| **Corporate / Pro Account Credit** | Pro account returns where the original charge was to a Pro account invoice | Credit applied to the Pro account open balance. Reflected on the next monthly Pro statement. |

| Step | Action | Role | System |
|---|---|---|---|
| 4.1.1 | Associate asks customer: "How would you like to receive your refund today?" and presents the eligible options based on policy rules. | Cashier / Service Desk Associate | — |
| 4.1.2 | For credit/debit card refunds, associate selects "Refund to Card" in POS. Customer swipes or taps the original card. POS sends the refund authorization to the payment processor. Refund posts to customer's account within 3–5 business days (credit) or 5–7 business days (debit). | Cashier / Service Desk Associate | POS / Payment Gateway |
| 4.1.3 | For cash refunds over $100, associate calls for a supervisor to verify the cash count before dispensing. Cash refunds are dispensed from the register drawer in bills no larger than $20. | Cashier / Supervisor | POS |
| 4.1.4 | For store credit, associate selects "Issue Merchandise Credit" in POS. POS generates a unique merchandise credit number. Associate loads the amount onto a physical BRHI Merchandise Credit Card, hands it to the customer, and reads the balance aloud. | Cashier / Service Desk Associate | POS |
| 4.1.5 | For exchanges, associate selects "Process Exchange" in POS, scans the returned item(s), then scans the new item(s). POS calculates any difference. Customer pays the balance due or receives a merchandise credit for the overage. | Cashier / Service Desk Associate | POS |

#### 4.2 Customer Receipt and Signatures

| Step | Action | Role | System |
|---|---|---|---|
| 4.2.1 | POS prints the Return Receipt detailing: returned item(s), SKU(s), original price, restocking fee (if any), refund amount, refund method, and return transaction number. | System (automated) | POS |
| 4.2.2 | For refunds over $50, cash refunds, or store credit: associate asks customer to sign the Return Receipt (physical or electronic signature pad). Associate verifies the signature matches the ID on file for no-receipt returns. | Cashier / Service Desk Associate | POS |
| 4.2.3 | Associate hands the customer copy of the Return Receipt to the customer. Store copy is retained in the register till for end-of-day reconciliation. | Cashier / Service Desk Associate | — |
| 4.2.4 | Associate thanks the customer and asks if there is anything else they need assistance with. | Cashier / Service Desk Associate | — |

#### 4.3 Serial Number Verification (Electronics / Power Tools)

| Step | Action | Role | System |
|---|---|---|---|
| 4.3.1 | For items in the Electronics, Power Tools, and Outdoor Power Equipment categories with a retail value of $50 or more, associate locates and records the serial number. | Service Desk Associate | POS |
| 4.3.2 | Associate enters the serial number in the POS serial number field. POS compares it against the serial number recorded at the time of original sale. | Service Desk Associate | POS |
| 4.3.3 | If serial numbers match: proceed normally. If serial numbers do not match: POS triggers a FRAUD ALERT (see Step 3.2.2). Associate does not confront the customer; instead, associate politely states that "the system requires a manager's review" and pages the MOD. | Service Desk Associate | POS |
| 4.3.4 | If no serial number was recorded at the time of sale (system displays "Serial Not Captured"), associate records the serial number now for future reference and proceeds with the return. | Service Desk Associate | POS |

---

### Phase 5: Item Disposition

**Objective:** Route the returned item to the correct destination based on its condition and resalability.

#### 5.1 Disposition Decision Matrix

| Condition Code | Description | Disposition | Target Timeline |
|---|---|---|---|
| **A — Like New** | Unopened packaging, or opened but complete and undamaged | Restock to shelf | Within 2 hours of return |
| **B — Open Box** | Opened, possibly missing minor packaging, fully functional | Route to Open Box / Clearance area | Within 4 hours of return |
| **C — Damaged / Defective** | Broken, missing parts, or non-functional | Route to Damaged Goods staging area | Within 1 hour of return |
| **D — Used / Worn** | Evidence of extended use | Route to Damaged Goods staging area | Within 1 hour of return |
| **Hazmat** | Paint, chemicals, propane, pesticides, adhesives | Route to Hazmat Holding Area | Immediately |

#### 5.2 Restock to Shelf (Condition A)

| Step | Action | Role | System |
|---|---|---|---|
| 5.2.1 | Associate places a green "RETURN — INSPECTED" sticker on the item (sticker includes date, associate initials, and condition code). | Service Desk Associate / Cashier | — |
| 5.2.2 | Associate places item in the Returns-to-Shelf cart located at the Service Desk. | Service Desk Associate / Cashier | — |
| 5.2.3 | Department Associate picks up Returns-to-Shelf cart every 2 hours (on the even hours: 10:00 AM, 12:00 PM, 2:00 PM, 4:00 PM, 6:00 PM, 8:00 PM) and returns items to their designated shelf locations. | Department Associate | — |
| 5.2.4 | POS automatically adjusts the on-hand inventory count when the return is completed. No manual inventory adjustment is needed for restocked items. | System (automated) | POS / Inventory |

#### 5.3 Open Box / Clearance (Condition B)

| Step | Action | Role | System |
|---|---|---|---|
| 5.3.1 | Associate places a yellow "OPEN BOX" sticker on the item, annotating the date and condition assessment. | Service Desk Associate | — |
| 5.3.2 | Item is placed in the Open Box staging area behind the Service Desk. | Service Desk Associate | — |
| 5.3.3 | Pricing Associate reviews open box items daily at 9:00 AM and sets a clearance price using the following schedule: markdown 15% if returned within 14 days of original sale, markdown 25% if returned after 14 days, markdown 40% if returned after 30 days. Markdown prices are entered into POS as a clearance SKU. | Pricing Associate | POS / PIM |
| 5.3.4 | Item is placed on the Open Box / Clearance fixture at the front of the corresponding department. Items unsold after 14 days on clearance are moved to the Bi-Weekly Clearance Event area near the store entrance. | Department Associate | — |

#### 5.4 Damaged Goods (Condition C and D)

| Step | Action | Role | System |
|---|---|---|---|
| 5.4.1 | Associate places a red "DAMAGED — DO NOT SELL" sticker on the item and records the return transaction number on the sticker. | Service Desk Associate | — |
| 5.4.2 | Item is placed in the Damaged Goods bin at the Service Desk. Bin is emptied to the Receiving Damaged Goods staging area every 4 hours (10:00 AM, 2:00 PM, 6:00 PM, 10:00 PM). | Service Desk Associate | — |
| 5.4.3 | Receiving Associate checks each damaged item against the RTV Eligibility List (updated monthly by Merchandising). Items eligible for vendor return are moved to the RTV staging area (Step 5.5). | Receiving Associate | RTV Eligibility List |
| 5.4.4 | Items not eligible for RTV are assessed for donation eligibility (see Step 5.6) or scheduled for disposal (see Step 5.7). | Receiving Associate | — |

#### 5.5 Return-to-Vendor (RTV) Initiation

| Step | Action | Role | System |
|---|---|---|---|
| 5.5.1 | Receiving Associate creates an RTV case in the RTV module of the inventory system, entering: vendor name, vendor part number, BRHI SKU, quantity, defect description, original PO number, and return transaction number. | Receiving Associate | RTV Module |
| 5.5.2 | System generates an RMA (Return Merchandise Authorization) request and transmits it to the vendor via EDI or vendor portal. | System (automated) | RTV Module / EDI |
| 5.5.3 | Items are held in the RTV staging area until the vendor approves the RMA and provides shipping instructions. RTV items older than 30 days without vendor response are escalated to the Merchandising team. | Receiving Associate | RTV Module |
| 5.5.4 | Once RMA is approved, Receiving Associate packs and ships the item per vendor instructions. Shipping cost is charged to the vendor per the vendor agreement. | Receiving Associate | RTV Module / WMS |
| 5.5.5 | Vendor credit is tracked in the RTV Module. If credit is not received within 60 days of shipment, AP Associate escalates to the Vendor Relations team. | AP Associate | RTV Module / AP |

#### 5.6 Donation

| Step | Action | Role | System |
|---|---|---|---|
| 5.6.1 | Items that are functional but not sellable (e.g., minor cosmetic damage, discontinued packaging) may be eligible for donation to BRHI's charitable partners (Habitat for Humanity ReStore, local community organizations). | Receiving Associate | — |
| 5.6.2 | Receiving Associate places item in the Donation staging area. Donation Coordinator reviews items weekly (every Tuesday) and arranges pickup or delivery. | Donation Coordinator | — |
| 5.6.3 | Donation Coordinator records the donation in the inventory system with the charitable organization name, item description, estimated value, and date. A donation receipt is generated and provided to the organization. | Donation Coordinator | Inventory / Tax Module |

#### 5.7 Disposal

| Step | Action | Role | System |
|---|---|---|---|
| 5.7.1 | Items that are unsellable, not RTV-eligible, and not donatable are scheduled for disposal. This includes items that pose a safety risk if resold (e.g., recalled items, structurally compromised ladders, broken electrical components). | Receiving Associate | — |
| 5.7.2 | Hazmat items for disposal are processed through the licensed hazmat disposal contractor (EnviroSafe Inc., contract #ENV-2024-0187) per the schedule of twice-monthly pickups (1st and 3rd Wednesday). | Receiving Associate / Facilities | — |
| 5.7.3 | Non-hazmat disposal items are compacted and placed in the locked disposal dumpster. Disposal dumpster is emptied by the waste management contractor every Tuesday and Friday. | Receiving Associate | — |
| 5.7.4 | Receiving Associate updates the inventory system to write off the disposed items, recording the disposal reason, date, and associate ID. | Receiving Associate | Inventory |

#### 5.8 System Inventory Update Summary

| Disposition | Inventory Impact |
|---|---|
| Restock to shelf | On-hand quantity increases by 1; item is available for sale |
| Open Box / Clearance | Original SKU on-hand unchanged (it was already decremented at return); new clearance SKU created with quantity 1 |
| Damaged Goods | On-hand quantity unchanged (already decremented); item tracked in Damaged Goods inventory |
| RTV | Inventory decremented from Damaged Goods; tracked in RTV Module until vendor credit received |
| Donation | Inventory decremented from Damaged Goods; donation recorded for tax purposes |
| Disposal | Inventory decremented from Damaged Goods; write-off recorded in shrinkage account |

---

### Phase 6: Financial Reconciliation

**Objective:** Ensure all returns are accurately reflected in the store's daily financial reporting and vendor chargebacks are processed.

#### 6.1 Daily Return Report

| Step | Action | Role | System |
|---|---|---|---|
| 6.1.1 | At store close, the POS system automatically generates the Daily Return Report, which includes: total number of returns, total refund value by refund method (cash, card, store credit, exchange), returns by department, returns by condition code, returns requiring manager override, fraud-alerted returns, and no-receipt returns. | System (automated) | POS / Reporting |
| 6.1.2 | Report is emailed to the Store Manager, ASM, and Loss Prevention Manager by 11:00 PM local time. | System (automated) | Reporting / Email |
| 6.1.3 | Store Manager reviews the Daily Return Report by 9:00 AM the following business day and signs off. Any anomalies (e.g., high-return associate, unusual pattern) are flagged for LP follow-up. | Store Manager | POS / Reporting |

#### 6.2 Refund Reconciliation

| Step | Action | Role | System |
|---|---|---|---|
| 6.2.1 | Cash Office Associate reconciles the physical cash in each register till against the POS cash refund total for the day. Variances over $5.00 are documented and reported to the ASM. | Cash Office Associate | POS / Cash Office |
| 6.2.2 | Credit/debit card refund totals are reconciled against the payment gateway settlement report. Any unmatched transactions are researched and resolved within 2 business days. | Cash Office Associate | POS / Payment Gateway |
| 6.2.3 | Merchandise Credit issued totals are reconciled against the Merchandise Credit log. Physical cards issued must match the number of credit transactions in POS. | Cash Office Associate | POS / Gift Card System |

#### 6.3 Vendor Chargeback

| Step | Action | Role | System |
|---|---|---|---|
| 6.3.1 | For RTV-eligible items, the RTV Module generates a Vendor Chargeback Request once the vendor approves the RMA. The chargeback includes: vendor name, PO number, SKU, quantity, unit cost, and defect reason code. | System (automated) | RTV Module / AP |
| 6.3.2 | Chargeback is submitted to the vendor's AP department via EDI (812 Credit/Debit Adjustment transaction). | System (automated) | EDI |
| 6.3.3 | If vendor disputes the chargeback, the Merchandising team reviews the case and provides documentation (photos, defect descriptions, PO records). Resolution target is 30 days. | Merchandise Analyst | AP / Vendor Portal |
| 6.3.4 | Unresolved chargebacks exceeding $500 are escalated to the Director of Vendor Relations. Chargebacks exceeding $5,000 are escalated to the VP of Merchandising. | AP Manager | AP |

---

## 5. Return Policy Details

### 5.1 Standard Return Time Windows

| Product Category | Return Window (With Receipt) | Return Window (BuildRight Brand) | Return Window (No Receipt) |
|---|---|---|---|
| General Merchandise (hardware, tools, home decor, storage) | 90 days | 365 days | 30 days (store credit only) |
| Lumber and Building Materials | 90 days | 365 days | 30 days (store credit only) |
| Plumbing, Electrical, HVAC | 90 days | 365 days | 30 days (store credit only) |
| Paint and Sundries (unopened, unmixed) | 90 days | 365 days | 30 days (store credit only) |
| Custom / Tinted Paint | No return (exchange only for color correction within 30 days) | Color correction within 365 days | Not eligible |
| Flooring and Tile (unopened full cases) | 90 days | 365 days | 30 days (store credit only) |
| Appliances (major: refrigerators, washers, dryers, ranges) | 30 days (uninstalled, in original packaging) | 90 days | Not eligible |
| Outdoor Power Equipment (mowers, chainsaws, blowers, tillers) | 30 days (if unfueled and unused, or defective) | 90 days | Not eligible |
| Power Tools | 90 days | 365 days | 30 days (store credit only) |
| Hand Tools | Lifetime (BuildRight brand), 90 days (other brands) | Lifetime | 30 days (store credit only) |
| Electronics (security cameras, smart home, audio) | 30 days | 90 days | Not eligible |
| Seasonal Items (patio furniture, holiday decor, grills) | 90 days (within season), 30 days (off-season) | 365 days | Not eligible off-season |
| Live Goods (plants, trees, shrubs) | 365 days (BuildRight brand, with receipt and plant) | 365 days | Not eligible |
| Gift Cards | Not returnable | Not returnable | Not returnable |
| Custom Orders (specialty windows, custom countertops) | Not returnable (unless defective) | Not returnable (unless defective) | Not returnable |
| Clearance / Final Sale Items | Not returnable (marked "Final Sale") | Not returnable | Not returnable |

### 5.2 Pro Account Exceptions

- Pro account holders receive a 120-day standard return window on all eligible categories (except Appliances and Outdoor Power Equipment, which remain at 30 days).
- Bulk return requests (10+ units or $500+) may be scheduled with the Pro Desk for dedicated processing to avoid regular checkout delays.
- Pro account returns may be applied as account credit rather than refunds, at the customer's request.

### 5.3 Online Return Time Windows

- Online orders follow the same category-based time windows as in-store purchases.
- The return window begins on the **delivery date** (not the order date).
- Online customers receive an email reminder about return eligibility 7 days before the window expires.

### 5.4 Restocking Fees

| Situation | Restocking Fee |
|---|---|
| Special-order items returned without defect | 25% of purchase price |
| Appliances returned opened but not defective | 15% of purchase price |
| Outdoor power equipment returned opened and unfueled | 15% of purchase price |
| Electronics returned opened and not defective | 15% of purchase price |
| Flooring/tile returned with opened cases (partial case) | 20% of purchase price (open cases only) |
| Items returned after the standard window but within the extended window (with manager approval) | 10% of purchase price |
| BuildRight brand items — no restocking fee ever | 0% |
| Defective items (any brand) — no restocking fee | 0% |

Restocking fees are calculated on the pre-tax purchase price. The fee is deducted from the refund amount before tax recalculation.

---

## 6. Business Rules

### 6.1 No-Receipt Return Limits

- Customers may make a maximum of **3 no-receipt returns** within a rolling 90-day period.
- The aggregate value of no-receipt returns may not exceed **$150** within a rolling 12-month period.
- No-receipt returns always receive **store credit** (BRHI Merchandise Credit Card), never cash or card refunds.
- A valid government-issued photo ID is required for every no-receipt return. Acceptable forms: state driver's license, state ID card, US passport, US military ID, permanent resident card.
- No-receipt returns for items over $50 require Supervisor authorization. No-receipt returns for items over $100 require Store Manager authorization.

### 6.2 ID Requirements

| Scenario | ID Required | ID Type |
|---|---|---|
| Receipt-based return, refund to original card | No | — |
| Receipt-based return, cash refund under $50 | No | — |
| Receipt-based return, cash refund $50+ | Yes | Any photo ID |
| No-receipt return (any value) | Yes | Government-issued photo ID |
| Store credit issuance (any value) | Yes | Any photo ID |
| Exchange, even trade | No | — |
| Pro account return | Yes | Pro account card or government-issued photo ID |

### 6.3 Serial Number Verification

- Serial number recording is **mandatory** at the time of sale for all Electronics and Power Tools with a retail value of $50 or more.
- Serial number verification is **mandatory** at the time of return for the same categories.
- If the serial number on the returned item does not match the serial number recorded at sale, the return is flagged as a Fraud Alert (see Step 3.2).
- If the item was purchased at a different BRHI location, the associate can access the original transaction's serial number via the cross-store transaction lookup in POS.

### 6.4 Return Window Enforcement

- POS enforces return windows automatically based on the original transaction date (receipt) or the estimated purchase date (no-receipt, based on the item's first receiving date in inventory).
- Returns outside the standard window are blocked by POS. Only the Store Manager can override a window block.
- Manager overrides for return window exceptions are logged in the POS audit trail and included in the Daily Return Report. More than 3 overrides by the same Store Manager in a rolling 30-day period triggers a Regional LP review.

### 6.5 Hazmat Exclusions

The following items **cannot** be returned once opened or mixed, regardless of brand or reason:

- Mixed or custom-tinted paint (exchange only for color correction)
- Opened containers of pesticides, herbicides, or fungicides
- Opened propane tanks or propane canisters
- Opened containers of solvents, adhesives, or chemical strippers
- Asbestos-containing products
- Lead-based products

Unopened hazmat items in original, sealed packaging may be returned within the standard 90-day window. Associates must inspect the seal integrity before accepting the return.

### 6.6 Fraud Prevention Rules

- The POS Fraud Engine evaluates every return against a ruleset maintained by the Corporate Loss Prevention team. Rules are updated quarterly.
- Customers with a documented history of return fraud (confirmed by LP investigation) are flagged in the system. Flagged customers may only process returns with a Store Manager present and LP notification.
- Associates are trained to recognize common return fraud schemes: wardrobing (buying, using, returning), receipt switching, shop-and-return (stealing an item then "returning" it), and price tag switching.
- The Fraud Engine uses the customer's ID number (from no-receipt returns), credit card token, or Pro account number to track return behavior across all BRHI locations.

---

## 7. Key Performance Indicators (KPIs)

| KPI | Target | Measurement Frequency | Data Source |
|---|---|---|---|
| **Return Rate** (total returns as a percentage of gross sales) | < 8% | Weekly, reported monthly | POS / Finance |
| **Return Processing Time** (average time from return initiation to refund receipt) | < 5 minutes | Daily, reported weekly | POS timestamp data |
| **Customer Satisfaction with Return Experience** | ≥ 90% positive (4+ out of 5 on post-return survey) | Continuous, reported monthly | Customer Survey (post-return email) |
| **No-Receipt Return Rate** | < 15% of total returns | Weekly, reported monthly | POS |
| **Fraud Detection Rate** | > 95% of confirmed fraudulent return attempts flagged by system | Monthly | LP Case Tracking / POS Fraud Engine |
| **Restock-to-Shelf Timeliness** | 100% of Condition A items restocked within 2 hours | Daily audit, reported weekly | Inventory timestamps |
| **RTV Processing Time** (from return to RTV shipment) | < 10 business days | Monthly | RTV Module |
| **Vendor Chargeback Recovery Rate** | > 85% of eligible RTV charges recovered | Monthly | AP / RTV Module |
| **Financial Reconciliation Accuracy** | Daily refund totals balanced within $5.00 variance | Daily | Cash Office / POS |
| **Manager Override Frequency** | < 2% of total returns require manager override | Weekly, reported monthly | POS Audit Trail |

### 7.1 KPI Escalation Thresholds

| KPI | Yellow Flag | Red Flag | Escalation |
|---|---|---|---|
| Return Rate | 8% – 10% | > 10% | Regional VP review at Red |
| Processing Time | 5 – 7 minutes | > 7 minutes | Store Manager action plan at Red |
| Customer Satisfaction | 85% – 90% | < 85% | VP Customer Care review at Red |
| Fraud Detection Rate | 90% – 95% | < 90% | Director of LP review at Red |
| Manager Override Rate | 2% – 4% | > 4% | Regional LP review at Red |

---

## 8. Controls

### 8.1 Fraud Detection Controls

| Control | Description | Owner |
|---|---|---|
| Automated Return Frequency Monitoring | POS tracks return frequency per customer (ID, card, or account) and flags anomalies | POS / Fraud Engine |
| Pattern Analysis Engine | Machine learning model identifies unusual return patterns across SKU, time, and geography | Corporate LP / Data Science |
| Serial Number Matching | POS compares return serial number to sale serial number for applicable categories | POS |
| Cross-Store Return Visibility | Returns initiated at one store are visible to all BRHI locations, preventing repeat fraud across stores | POS / Central DB |
| No-Receipt Return Limiting | Hard limits on frequency (3 per 90 days) and value ($150 per year) per customer ID | POS |
| High-Value Return Notification | All returns over $500 trigger an automatic notification to the Regional LP Manager | POS / Email |

### 8.2 Serial Number Tracking

- All electronics and power tools ($50+ retail) have serial numbers recorded at both sale and return.
- Serial numbers are stored in the centralized inventory database and are accessible across all locations.
- Discrepancies between sale and return serial numbers trigger a FRAUD ALERT (see Step 3.2).
- Serial number data is shared with law enforcement upon request during theft investigations (with Legal approval).

### 8.3 Manager Override Controls

| Override Type | Approval Level | Documentation Required |
|---|---|---|
| Return window extension (up to 30 additional days) | Store Manager | Override reason code + customer ID |
| Return window extension (more than 30 additional days) | Regional VP Customer Care (via email or phone) | Written justification + customer ID + original receipt |
| No-receipt return exceeding $150 annual limit | Store Manager + Regional LP Manager | Override reason code + LP acknowledgment |
| Restocking fee waiver | ASM or above | Reason code (e.g., customer loyalty, product defect) |
| Refund to alternate tender (not original payment method, over $200) | Store Manager | Override reason code |
| Return of Final Sale item | Store Manager + Regional VP approval | Written justification; case-by-case only |

All overrides are logged in the POS audit trail with:

- Authorizer name and ID
- Date and time of override
- Original transaction number
- Override reason code
- Customer ID (if applicable)

The Loss Prevention team reviews the Override Report weekly and investigates any override that appears to be outside normal business parameters.

### 8.4 Physical Controls

- Returned items are never left unattended at the Service Desk. Items awaiting disposition are stored in the locked Returns staging area.
- Damaged Goods and RTV items are stored in the locked Receiving area, accessible only to authorized Receiving and Management personnel.
- Hazmat returns are stored in the ventilated, locked Hazmat Holding Area in Receiving, separate from all other inventory.
- The Damaged Goods and RTV staging areas are inventoried weekly by the Receiving Supervisor and reconciled against the POS return records.
- Store credit cards are treated as negotiable instruments. Blank cards are kept in the Cash Office safe and counted daily.

### 8.5 Audit and Compliance

- Internal Audit conducts a Returns Process audit at each store at least once per year, with high-shrink stores audited semi-annually.
- Audit scope includes: POS return transaction accuracy, physical inventory reconciliation of returned items, cash handling procedures, override documentation completeness, and fraud alert response timeliness.
- Findings are reported to the VP Customer Care, SVP Store Operations, and the Regional VP.
- Critical findings (e.g., systematic override abuse, missing inventory) require a corrective action plan within 14 business days.

---

## Appendices

### Appendix A: Return Reason Codes

| Code | Description | Typical Disposition |
|---|---|---|
| RR-01 | Defective / Does not work | Damaged / RTV |
| RR-02 | Wrong item received / purchased | Restock (if sealed) |
| RR-03 | Changed mind / No longer needed | Restock (if Condition A) |
| RR-04 | Found a better price | Restock (if Condition A) |
| RR-05 | Damaged in shipping / transit | Damaged / RTV |
| RR-06 | Missing parts | Damaged / RTV / Vendor claim |
| RR-07 | Not as described / depicted | Restock or Open Box |
| RR-08 | Duplicate purchase | Restock (if Condition A) |
| RR-09 | Warranty exchange (BRHI brand) | Damaged / Write-off |
| RR-10 | Recall return | Per Recall instructions (see BRHI-BP-011) |
| RR-11 | Store error (wrong item given to customer) | Restock (if Condition A) |
| RR-12 | Other (associate must provide notes) | Varies |

### Appendix B: RMA Request Template Fields

- Vendor Name
- Vendor Number
- BRHI SKU
- Vendor Part Number
- Original PO Number
- Quantity
- Unit Cost
- Defect Description (free text, 500 char max)
- Defect Code (from vendor-provided list)
- Return Transaction Number
- Store Number
- Photographs (required for items over $100)

### Appendix C: Contacts

| Role | Name | Phone | Email |
|---|---|---|---|
| VP Customer Care | Angela Morales | ext. 4401 | a.morales@brhi.com |
| Director of Loss Prevention | Marcus Webb | ext. 5500 | m.webb@brhi.com |
| RTV Coordinator | Central RTV Team | ext. 6200 | rtv@brhi.com |
| Merchandise Credit Support | IT Help Desk | ext. 9000 | it.helpdesk@brhi.com |
| Hazmat Disposal (EnviroSafe) | Dispatch | (800) 555-0199 | dispatch@envirosafe.com |

---

*End of Document BRHI-BP-003 v3.2*
