# Order-to-Cash (O2C) Business Process Documentation

## BuildRight Home Improvement, Inc. (BRHI)

---

## 1. Document Control

| Field | Detail |
|---|---|
| **Document ID** | BRHI-BP-001 |
| **Version** | 1.1 |
| **Classification** | Internal |
| **Effective Date** | April 1, 2026 |
| **Process Owner** | Chief Financial Officer (CFO) |
| **Document Author** | Finance Operations Team |
| **Review Cycle** | Annually or upon significant process change |
| **Last Reviewed** | April 2, 2026 |
| **Next Review Date** | April 1, 2027 |
| **Approved By** | Chief Financial Officer; VP of Operations; VP of Pro Business |

### Revision History

| Version | Date | Author | Description |
|---|---|---|---|
| 1.1 | April 2, 2026 | Enterprise Technology Team | Updated to replace SAP references with Oracle Fusion Cloud ERP |
| 1.0 | April 1, 2026 | Finance Operations Team | Initial release — comprehensive O2C process documentation |

### Distribution

This document is distributed to all individuals and teams involved in the Order-to-Cash cycle, including Store Operations, E-Commerce, Pro Desk, Warehouse/Distribution Center, Accounts Receivable, Finance, and IT. All copies are controlled via the BRHI document management system. Uncontrolled copies should not be used for operational reference.

---

## 2. Process Overview

The Order-to-Cash (O2C) cycle at BuildRight Home Improvement, Inc. encompasses the end-to-end business process from initial customer order through final cash receipt and reconciliation. This process spans all BRHI sales channels and represents the primary revenue-generating workflow of the organization.

The O2C cycle ensures that every customer interaction — from the moment an order is placed to the moment payment is collected and recorded — is executed consistently, accurately, and in compliance with internal controls, accounting standards (ASC 606), and regulatory requirements (PCI DSS, SOX, sales tax).

### Channels Covered

BRHI operates four distinct sales channels, each integrated into the unified O2C process:

- **In-Store Point of Sale (POS)**: Approximately 75% of total revenue. Transactions processed through NCR Emerald terminals across all store locations. Includes retail customers and Pro walk-in business.
- **E-Commerce (buildright.com)**: Approximately 15% of total revenue. Online orders placed through the Salesforce Commerce Cloud platform. Includes BOPIS (Buy Online, Pick Up In Store) and ship-to-home options.
- **Pro Phone/Fax**: Approximately 8% of total revenue. Orders placed by Pro customers via the dedicated Pro Desk phone line (1-800-PRO-BUILD) or fax. These orders typically involve larger volumes, contract pricing, and Net 30 billing terms.
- **Mobile App**: Approximately 2% of total revenue. Orders placed through the BRHI mobile application (iOS and Android), which interfaces with the same Salesforce Commerce Cloud back end as e-commerce.

### Process Objectives

1. Deliver a seamless, consistent customer experience across all sales channels.
2. Ensure accurate order capture, pricing, and invoicing.
3. Optimize fulfillment speed and cost through intelligent order routing.
4. Maintain strong internal controls over revenue recognition, cash handling, and credit management.
5. Minimize days sales outstanding (DSO) and bad debt expense while preserving customer relationships.
6. Comply with all applicable accounting standards, tax regulations, and data security requirements.

---

## 3. SIPOC Analysis

The SIPOC (Suppliers, Inputs, Process, Outputs, Customers) analysis below provides a high-level view of the O2C process boundaries and stakeholder interactions.

### Suppliers

| Supplier | Description |
|---|---|
| **Customers (Retail)** | End consumers who initiate orders in-store, online, or via mobile app. Provide order details, payment information, and delivery preferences. |
| **Customers (Pro)** | Professional contractors, builders, and trade professionals with established BRHI Pro accounts. Provide purchase orders, project references, and billing information. |
| **Sales Associates** | In-store personnel who facilitate POS transactions, provide product expertise, and process customer orders. |
| **BuildRight Website (buildright.com)** | E-commerce platform through which online customers submit orders, select fulfillment options, and complete payment. |
| **Pro Desk Representatives** | Dedicated personnel who manage Pro customer relationships, process phone/fax orders, and coordinate Pro account billing and collections. |
| **Vendors / Suppliers** | Third-party vendors who provide direct-ship fulfillment for special-order and large-item products. Provide inventory availability (vendor ATP) and shipping information. |
| **Carriers** | Shipping partners (UPS, FedEx, USPS, LTL carriers) who provide transit, tracking, and proof-of-delivery data. |
| **Marketing / Pricing Team** | Provides promotional pricing, weekly ad pricing, clearance pricing, and competitive pricing intelligence. |
| **Warehouse / DC Staff** | Distribution center personnel who pick, pack, and ship orders. Provide fulfillment confirmation and shipment details. |

### Inputs

| Input | Description | Source |
|---|---|---|
| **Customer Orders** | Order details including items, quantities, delivery method, and customer information. | All channels |
| **Payment Information** | Credit card data, gift card numbers, cash, Pro account charges. | Customers |
| **Customer Data** | Customer profiles, loyalty information, Pro account details, credit histories. | CRM (Salesforce), POS system |
| **Inventory Data** | Real-time available-to-promise (ATP) inventory across store network, distribution centers, and vendor direct-ship. | WMS (Manhattan), Oracle SCM Cloud - Inventory, vendor feeds |
| **Pricing Data** | Base pricing, Pro contract pricing, promotional pricing, volume discount schedules, price match data. | Oracle Pricing Engine, Pricing team |
| **Credit Limits** | Pro customer credit limits and account standing. | AR/Credit team, Oracle Financials Cloud - AR |
| **Tax Rates / Rules** | Applicable sales tax rates, exemption certificates, and nexus rules. | Vertex tax engine |
| **Delivery Schedules** | Available delivery windows, carrier schedules, and routing information. | OMS (IBM Sterling), carrier APIs |

### Process

The O2C process consists of 5 phases and 29 discrete steps:

| Phase | Steps | Description |
|---|---|---|
| **Phase 1: Order Entry** | Steps 1.1 – 1.7 (7 steps) | Customer order capture, validation, pricing, and confirmation across all channels. |
| **Phase 2: Order Fulfillment** | Steps 2.1 – 2.6 (6 steps) | Order routing, picking, packing, shipping, delivery, and confirmation. |
| **Phase 3: Billing** | Steps 3.1 – 3.5 (5 steps) | Invoice generation, Pro billing, tax calculation, revenue recognition, and exception handling. |
| **Phase 4: Collections and Payment** | Steps 4.1 – 4.6 (6 steps) | Payment processing, Pro account collections, aging management, escalation, dispute resolution, and write-offs. |
| **Phase 5: Returns and Credits** | Steps 5.1 – 5.5 (5 steps) | Return initiation, authorization, refund processing, inventory disposition, and credit memo generation. |

### Outputs

| Output | Description |
|---|---|
| **Fulfilled Orders** | Orders successfully delivered to customers across all channels, with proof of delivery captured. |
| **Invoices** | Transaction invoices (POS receipts, e-commerce invoices) and monthly Pro account statements. |
| **Payments Received** | Credit card settlements, cash deposits, check deposits, ACH/wire transfers, and gift card redemptions. |
| **Financial Records** | Revenue entries (Oracle Financials Cloud), accounts receivable records, credit memos, bad debt provisions, and reconciliation reports. |
| **Customer Notifications** | Order confirmations, shipping notifications, delivery confirmations, billing statements, and return acknowledgments. |
| **Management Reports** | Aging reports, KPI dashboards, return trend analyses, bad debt reports, and collection effectiveness reports. |

### Customers

| Customer | Description |
|---|---|
| **End Customers (Retail)** | Receive fulfilled orders, invoices/receipts, and refund/credit processing. |
| **Pro Customers** | Receive fulfilled orders, monthly billing statements, credit management, and dispute resolution services. |
| **Finance / Accounting** | Receives accurate revenue data, AR records, tax filings, and reconciliation-ready financial entries. |
| **Executive Management** | Receives KPI reporting, trend analysis, and process performance data for strategic decision-making. |
| **Loss Prevention** | Receives return reports, refund anomaly alerts, and cash handling audit data. |
| **External Auditors** | Receives SOX control evidence, revenue recognition documentation, and compliance records. |

---

## 4. Process Scope

### In-Scope

The following processes and functions are included within the boundaries of this O2C documentation:

- **All Sales Channels**: In-store POS (75% of revenue), e-commerce via buildright.com (15%), Pro phone/fax (8%), and mobile app (2%).
- **Order Entry and Capture**: Customer identification, order creation, pricing validation, payment authorization, and order confirmation across all channels.
- **Order Fulfillment**: Order routing, BOPIS processing, DC pick/pack/ship, delivery scheduling, carrier management, and delivery confirmation.
- **Billing and Invoicing**: Invoice generation for all channels, Pro account monthly billing, tax calculation and processing, and revenue recognition under ASC 606.
- **Collections and Payment Processing**: Credit card settlement, cash handling, check processing, Pro account collections, aging management, dispute resolution, and bad debt write-off.
- **Returns and Credits**: Return authorization, refund processing, store credit issuance, inventory disposition, credit memo generation, and vendor chargebacks.
- **Pro Account Management**: Credit limit administration, contract pricing application, Net 30 billing, and Pro account collections lifecycle.
- **Cross-Channel Integration**: Unified order management, shared inventory visibility, and consistent pricing and promotions across all channels.

### Out-of-Scope

The following processes and functions are excluded from this document and are covered by separate documentation:

| Excluded Process | Reference Document |
|---|---|
| Vendor procurement and accounts payable | BRHI-BP-002 Procure-to-Pay |
| Human resources processes (hiring, training, payroll) | BRHI-HR-001 HR Policy Manual |
| Store operations (opening/closing procedures, stocking, merchandising) | SOP 04.01 Store Operations Manual |
| Product master data management | BRHI-IT-003 Master Data Governance |
| IT infrastructure and system administration | BRHI-IT-001 IT Operations Manual |
| Marketing campaign management | BRHI-MKT-001 Marketing Operations |
| Loss Prevention investigations | SOP 06.01 Loss Prevention Procedures |
| Real estate and store expansion | BRHI-RE-001 Real Estate Process |

---

## 5. Process Steps

### Swimlane Assignments

The following roles/swimlanes are used throughout the process steps:

| Swimlane | Abbreviation | Description |
|---|---|---|
| **Customer** | CUST | End customer (retail or Pro) initiating the order or return. |
| **Sales Associate** | SA | In-store associate processing POS transactions or facilitating orders. |
| **POS System** | POS | NCR Emerald point-of-sale system. |
| **E-Commerce Platform** | EC | Salesforce Commerce Cloud (buildright.com and mobile app). |
| **Order Management** | OM | IBM Sterling OMS and Oracle SCM Cloud - Order Management for order routing and management. |
| **Warehouse / DC** | WH | Distribution center and in-store warehouse personnel. |
| **Finance / AR** | FIN | Accounts Receivable team, Credit team, and Finance operations. |

---

### Phase 1: Order Entry

**Objective**: Capture customer orders accurately across all channels, validate customer information and credit, verify inventory availability and pricing, authorize payment, and provide order confirmation.

---

#### Step 1.1 — Customer Initiates Order via Channel

| Attribute | Detail |
|---|---|
| **Step ID** | O2C-1.1 |
| **Swimlane** | CUST |
| **Trigger** | Customer decides to purchase product(s) from BRHI. |

The customer initiates the order through one of four channels:

**In-Store POS**: The customer brings product(s) to a checkout lane or Pro Desk register. The sales associate scans or enters each item. The customer may also request items not on the shelf (special orders) which are entered at the Pro Desk or customer service counter.

**E-Commerce (buildright.com)**: The customer browses the online catalog, adds items to the shopping cart, selects a fulfillment method (BOPIS or ship-to-home), and proceeds to checkout. The customer enters or confirms shipping address, billing address, and payment information.

**Pro Phone/Fax**: The Pro customer calls the dedicated Pro Desk line at 1-800-PRO-BUILD and provides their account number, purchase order (PO) number, item numbers or descriptions, quantities, and desired delivery date and location. Alternatively, the Pro customer faxes a purchase order to the Pro Desk fax number. The Pro Desk representative enters the order into Oracle Financials Cloud on the customer's behalf.

**Mobile App**: The customer uses the BRHI mobile application (iOS or Android) to browse, scan barcodes in-store for product information and quick add, select fulfillment method, and complete checkout. The mobile app shares the same back-end infrastructure as buildright.com.

Upon initiation, the order details are captured in the respective channel system and passed to the Order Management layer for validation and processing.

---

#### Step 1.2 — System Validates Customer

| Attribute | Detail |
|---|---|
| **Step ID** | O2C-1.2 |
| **Swimlane** | POS / EC / OM |
| **Trigger** | Order details received from channel. |

**Pro Customers**:

The system identifies the customer as a Pro account holder based on account number, registered email, or Pro card scan. The following validations are performed:

1. **Credit Check**: The Pro customer's outstanding balance and open orders are compared against their approved credit limit. Credit limits by tier are as follows:
   - **Member**: $5,000
   - **VIP**: $50,000
   - **Elite**: $500,000

   If the new order would cause the total exposure (outstanding balance + open orders + new order) to exceed the credit limit, the order is held and the AR/Credit team is notified for review.

2. **Account Standing Verification**: The system checks for any account holds (e.g., past-due balances exceeding terms, disputed items pending resolution, accounts on credit hold). If an account hold exists, the order cannot proceed until the hold is resolved.

3. **Contract Pricing Applied**: The system retrieves the Pro customer's negotiated pricing agreements from Oracle Financials Cloud. Contract pricing is applied automatically based on the customer's tier, vendor agreements, and product categories. Contract prices may be expressed as a fixed price, percentage off list, or percentage off retail, depending on the agreement structure.

**Retail Customers**:

1. **Loyalty Lookup**: If the customer provides a phone number, email, or loyalty card, the system retrieves their existing customer record from Salesforce CRM, including purchase history, loyalty points, and any stored preferences.

2. **Guest Record Creation**: If no existing record is found and the customer does not wish to provide loyalty information, a guest transaction record is created. Minimal information (payment tender, items purchased) is retained for return and reporting purposes.

---

#### Step 1.3 — Real-Time Inventory Availability Check

| Attribute | Detail |
|---|---|
| **Step ID** | O2C-1.3 |
| **Swimlane** | OM |
| **Trigger** | Customer and order items validated. |

The system performs a real-time Available-to-Promise (ATP) query against the perpetual inventory system to confirm product availability:

1. **Store Network Inventory**: The ATP query checks inventory levels across the BRHI store network. For BOPIS orders, the system checks the selected store's inventory. For ship-from-store orders, the system identifies the closest store with available inventory.

2. **Distribution Center (DC) Inventory**: If no store inventory is available, the system checks DC inventory levels across all DCs (regional DCs in the Northeast, Southeast, Midwest, Southwest, and West Coast).

3. **Vendor ATP (Direct-Ship)**: For special-order items, large items (e.g., appliances, building materials), or items not stocked in the BRHI network, the system queries vendor ATP via EDI or API integration. Vendor direct-ship items display estimated lead times at the time of order.

The ATP results determine the fulfillment method and estimated delivery/pickup date presented to the customer. If an item is unavailable across all sources, the customer is notified and offered alternatives (substitution, backorder, or order cancellation).

Inventory is soft-reserved at the time of order confirmation and hard-reserved upon fulfillment assignment.

---

#### Step 1.4 — Pricing Validation

| Attribute | Detail |
|---|---|
| **Step ID** | O2C-1.4 |
| **Swimlane** | POS / EC / OM |
| **Trigger** | Inventory availability confirmed. |

The system applies the appropriate pricing based on customer type, promotions, and business rules:

1. **Pro Contract Price**: For Pro customers, negotiated pricing per vendor agreement is applied. Contract pricing takes precedence over retail pricing for qualifying items. The system compares the contract price against the current list price and applies the lower of the two.

2. **Promotional Pricing**: The system checks for applicable promotional pricing, including:
   - **Weekly Ad Pricing**: Items featured in the current weekly advertisement, valid Sunday through Saturday.
   - **Clearance Pricing**: Discontinued or overstock items marked down for clearance.
   - **Seasonal Promotions**: Time-limited promotions tied to seasonal events (Spring Garden, Black Friday, Holiday, etc.).

3. **Volume Discounts**: Quantity-based discounts are automatically applied:
   - **10+ units**: 5% discount off applicable base price
   - **50+ units**: 10% discount off applicable base price
   - **100+ units**: 15% discount off applicable base price

   Volume discounts apply to individual SKUs. Pro contract pricing and volume discounts are not stackable; the system applies the greater discount.

4. **Price Match**: BRHI honors a price match guarantee for identical items found at a lower price at a local competitor brick-and-mortar store. The policy is:
   - BRHI matches the competitor's price plus an additional 10% of the difference.
   - **Example**: BRHI price $100, competitor price $90. Difference = $10. Price match = $90 - ($10 x 10%) = $89.00.
   - **Exclusions**: Clearance, closeout, installation services, special order items, online-only retailers, and competitor prices that require membership fees.

   The sales associate or customer service representative verifies the competitor price via phone, website (for brick-and-mortar stores), or printed ad. Price match authorization is logged in the POS system for audit purposes.

---

#### Step 1.5 — Sales Order Created in Oracle Financials Cloud

| Attribute | Detail |
|---|---|
| **Step ID** | O2C-1.5 |
| **Swimlane** | OM |
| **Trigger** | Pricing validated and applied. |

Upon successful validation of customer, inventory, and pricing, the system creates a formal sales order in Oracle Financials Cloud (Order Management module):

1. A unique order number is generated in the format: **SO-YYYYMMDD-XXXXXX**
   - YYYYMMDD = date of order creation
   - XXXXXX = sequential six-digit number (system-generated, unique per day)

2. The sales order record includes:
   - Customer number (Pro account number or retail customer ID)
   - Order date and time
   - Sales channel indicator (POS, ECOM, PRO, MOBILE)
   - Line items with SKU, description, quantity, unit price, extended price, and applicable discounts
   - Tax amount (calculated by Vertex)
   - Order total
   - Fulfillment method (BOPIS, ship-from-store, ship-from-DC, vendor direct-ship)
   - Delivery address or pickup store location
   - Payment method and authorization reference
   - Sales associate ID or online session reference
   - Pro customer PO number (if applicable)

3. The customer receives confirmation:
   - **In-Store**: Printed receipt with order number, itemized list, payment summary, and return policy.
   - **E-Commerce / Mobile App**: On-screen confirmation page followed by an email confirmation containing the order number, estimated delivery or pickup date, itemized list, and links to track the order.
   - **Pro Phone/Fax**: Email confirmation (and fax confirmation if requested) with order number, PO reference, itemized list, estimated delivery date, and Pro account terms reminder.

---

#### Step 1.6 — Payment Authorization

| Attribute | Detail |
|---|---|
| **Step ID** | O2C-1.6 |
| **Swimlane** | POS / EC |
| **Trigger** | Sales order created. |

Payment is authorized based on the tender type:

**Credit Card**:

1. The payment gateway (Adyen) processes the authorization request.
2. An authorization hold is placed on the customer's card for the order total.
3. The authorization is valid for **7 calendar days**. If order fulfillment (shipment or pickup) will exceed 7 calendar days, the system automatically initiates a re-authorization. The original authorization is released and a new authorization is obtained.
4. For partial shipments, each shipment is captured separately against the original authorization (if within the 7-day window) or against a re-authorization.
5. The authorization reference is stored in the sales order record for settlement upon fulfillment.

**Gift Card**:

1. The gift card balance is verified in real time.
2. The order amount is deducted from the gift card balance immediately upon order confirmation.
3. If the gift card balance is insufficient, the customer may split payment across multiple tenders (gift card + credit card, gift card + cash, etc.).
4. Gift card maximum balance is $500. No expiration dates. No fees. Redeemable at all BRHI channels.

**Pro Account (Charge)**:

1. For Pro customers purchasing on account, the order total is charged against the Pro account.
2. The system verifies the charge will not exceed the approved credit limit (Step 1.2 pre-check ensures this).
3. A hold is placed on the Pro account for the order amount, reducing available credit.
4. The charge is recorded as an open item on the Pro account in Oracle Financials Cloud - AR.
5. Payment is due per Net 30 terms from the invoice date.

**Cash**:

1. Cash is accepted for in-store transactions only.
2. The sales associate receives payment, opens the cash drawer, and provides change.
3. Cash is deposited in the register and included in the daily deposit (see Phase 4, Step 4.1).
4. For security and control purposes, cash payments above $3,000 require supervisor verification and signature.

---

#### Step 1.7 — Order Confirmation

| Attribute | Detail |
|---|---|
| **Step ID** | O2C-1.7 |
| **Swimlane** | POS / EC / OM |
| **Trigger** | Payment authorized. |

The system finalizes the order confirmation and delivers it to the customer:

**In-Store (POS)**:

- A printed receipt is generated at the register including: store name and address, order number, date and time of transaction, itemized list with SKUs, descriptions, quantities, unit prices, discounts applied, subtotal, tax, total, payment method (last 4 digits for cards), and return policy summary.
- For BOPIS orders placed in-store, the receipt includes the expected pickup date/time and the pickup location within the store.
- For special orders, the receipt includes estimated arrival date and any deposit paid.

**E-Commerce / Mobile App**:

- An on-screen order confirmation page displays immediately after checkout, showing the order number, itemized list, estimated delivery or pickup date, and payment summary.
- An email confirmation is sent to the customer's registered email address within 1 minute of order completion. The email includes:
  - Order number (hyperlinked to order status page on buildright.com)
  - Itemized list with product images, SKUs, descriptions, quantities, unit prices, discounts, subtotal, tax, shipping charges (if applicable), and total
  - Estimated delivery date (for ship-to-home) or estimated pickup-ready time (for BOPIS)
  - Payment summary (card type, last 4 digits)
  - Links to modify or cancel the order (if still within the modification window)
  - Return policy summary

**Pro Phone/Fax**:

- Email confirmation sent to the Pro customer's registered email address.
- Confirmation includes: order number, PO reference, itemized list with contract pricing, estimated delivery date, and Pro account terms (Net 30).
- If the Pro customer has opted in to fax confirmations, a confirmation is faxed to the registered fax number.

At this point, the order is confirmed and transitions to Phase 2 for fulfillment.

---

### Phase 2: Order Fulfillment

**Objective**: Route and fulfill customer orders through the optimal channel, deliver products to the customer, and capture proof of delivery to trigger billing.

---

#### Step 2.1 — Order Routing Engine Determines Optimal Fulfillment

| Attribute | Detail |
|---|---|
| **Step ID** | O2C-2.1 |
| **Swimlane** | OM |
| **Trigger** | Confirmed order enters fulfillment queue. |

The IBM Sterling Order Management System's routing engine evaluates the order and determines the optimal fulfillment method based on the following logic:

1. **BOPIS (In-Store Pickup)**: If the customer selected BOPIS at checkout and the ordered items are available at the selected store, the order is routed to that store for in-store pickup. The store receives a pick notification and the customer is notified when the order is ready.

2. **Ship-from-Store (SFS)**: If the customer selected ship-to-home and inventory is available at a store (but not at the DC or the DC fulfillment window is longer), the order is routed to the closest store with available inventory. Store associates pick and ship the order via the designated carrier.

3. **Ship-from-DC**: If no store inventory is available or the DC can fulfill more efficiently (e.g., proximity to customer, DC has better packaging capabilities for the item type), the order is routed to the appropriate distribution center.

4. **Vendor Direct-Ship**: For special-order items, large items (e.g., appliances, sheds, fencing), or items not stocked in the BRHI network, the order is routed to the vendor for direct shipment to the customer. The vendor is notified via EDI (EDI 850 Purchase Order) and confirms the order with an expected ship date (EDI 855 Purchase Order Acknowledgment).

The routing engine considers the following factors in priority order:
- Customer's selected fulfillment method (BOPIS vs. ship-to-home)
- Inventory availability at each node in the network
- Distance/proximity to customer delivery address
- Fulfillment cost (labor, packaging, shipping)
- Delivery speed (promised delivery date)
- Item characteristics (size, weight, hazmat restrictions)

The routing decision is logged in the OMS and communicated to the assigned fulfillment location.

---

#### Step 2.2 — BOPIS Fulfillment

| Attribute | Detail |
|---|---|
| **Step ID** | O2C-2.2 |
| **Swimlane** | SA / WH |
| **Trigger** | Pick notification received at store. |

For orders routed to a store for BOPIS fulfillment:

1. **Pick Notification**: The assigned sales associate receives a pick notification on their mobile device (BRHI handheld scanner/tablet). The notification includes the order number, customer name, item locations (aisle, bay, shelf), and item descriptions.

2. **Picking**: The associate navigates to each item location, scans the item barcode to verify the correct SKU, and confirms the quantity. All items must be picked within **30 minutes** of the pick notification. If the associate identifies an inventory discrepancy (item not on shelf), they initiate a cycle count and the system checks for alternate locations within the store.

3. **Verification and Staging**: Once all items are picked, the associate scans the completed order for final verification. The items are placed in a designated BOPIS staging area at the front of the store. The order is marked as "Ready for Pickup" in the OMS.

4. **Customer Notification**: The customer is notified via email and SMS that their order is ready for pickup. The notification includes the order number, store location, pickup counter location (e.g., "Order Pickup Counter, near Entrance A"), and the hold limit (48 hours).

5. **Customer Pickup**: The customer arrives at the store, presents a valid photo ID and the order number (or the email confirmation on their phone). The associate verifies the customer's identity, retrieves the order from the staging area, and hands the items to the customer. The associate scans the order as "Picked Up" in the system.

6. **48-Hour Hold Limit**: If the customer does not pick up the order within **48 hours** of the "Ready for Pickup" notification, the order is automatically cancelled. Inventory is restored to available stock. The customer is notified of the cancellation via email. If the customer still wants the items, they must place a new order. Refer to Business Rule BR-O2C-009.

---

#### Step 2.3 — DC / Fulfillment Center Processing

| Attribute | Detail |
|---|---|
| **Step ID** | O2C-2.3 |
| **Swimlane** | WH |
| **Trigger** | Order routed to DC. |

For orders routed to a distribution center:

1. **Wave Release**: Orders are released in waves for efficient processing. Waves are released daily at **6:00 AM** and **2:00 PM** local time. The wave planning engine in Manhattan Associates WMS groups orders by zone, carrier, and priority to optimize pick paths and labor utilization.

2. **RF-Directed Picking**: DC associates use RF (radio frequency) handheld scanners to execute picks. The WMS directs each associate to the optimal pick location, displaying the item SKU, location, and quantity required. The associate scans the location and item barcode to confirm each pick.

3. **Pack Station with Quality Check**: After picking, items move to the pack station. The pack station operator:
   - Scans each item to verify correctness against the order.
   - Performs a visual quality check (no damage, correct packaging, all accessories included).
   - Selects the appropriate box size or packaging material.
   - Packs the order and applies the shipping label.
   - Scans the packed order to confirm completion.

4. **Carrier Selection (Least-Cost Routing)**: The WMS selects the carrier based on least-cost routing rules:
   - **UPS Ground**: Orders under 5 lbs, standard delivery.
   - **FedEx / USPS**: Orders under 1 lb (small parcels, light items).
   - **LTL (Less-Than-Truckload)**: Orders over 150 lbs (building materials, bulk items).
   - Carrier selection also considers delivery speed commitments and customer preferences.

5. **Tracking Number Generation**: Upon carrier handoff, a tracking number is generated and transmitted to the OMS. The customer is notified via email with the tracking number and a link to the carrier's tracking page and the buildright.com order tracking page.

---

#### Step 2.4 — Delivery Scheduling

| Attribute | Detail |
|---|---|
| **Step ID** | O2C-2.4 |
| **Swimlane** | OM / SA |
| **Trigger** | Order contains items requiring scheduled delivery. |

Delivery scheduling applies to the following product categories:
- **Appliances**: All appliance orders over $399 (free delivery).
- **Installation Services**: Any order that includes professional installation (e.g., flooring, countertops, HVAC, water heater).
- **Big-Ticket Lumber and Building Materials**: Large or heavy building materials that cannot be shipped via parcel carrier.

The delivery scheduling process:

1. **Window Selection at Checkout**: The customer selects a preferred **4-hour delivery window** at the time of checkout. Available windows are typically:
   - Morning: 8:00 AM – 12:00 PM
   - Afternoon: 12:00 PM – 4:00 PM
   - Evening: 4:00 PM – 8:00 PM

   Windows are available Tuesday through Saturday (no Sunday or Monday deliveries).

2. **Confirmation Call/Text**: The day before the scheduled delivery, the customer receives a confirmation call (automated or live) and/or text message confirming the delivery date and window. The customer may reschedule at this point if needed.

3. **Two-Person Delivery Team**: All scheduled deliveries are performed by a two-person delivery team (BRHI employees or contracted delivery partners). The team is equipped with the necessary equipment (hand trucks, straps, protective blankets) and customer-facing documentation (delivery receipt, installation checklist if applicable).

4. **Customer Signature Required**: The customer (or an authorized representative age 18+) must be present to sign for the delivery. The delivery team obtains the customer's signature on the electronic delivery receipt. If no one is present, the delivery is re-scheduled and a re-delivery fee may apply.

Delivery charges per Business Rule BR-O2C-008:
- Standard delivery: Free for orders over $49
- Express next-day delivery: $35
- Pro priority delivery: Free for all Pro tiers
- Appliance delivery: Free for orders over $399

---

#### Step 2.5 — Carrier Pickup and Transit

| Attribute | Detail |
|---|---|
| **Step ID** | O2C-2.5 |
| **Swimlane** | WH |
| **Trigger** | Order packed and carrier label applied. |

1. **Carrier Pickup**: The carrier picks up shipments from the DC or store at the scheduled pickup time. The shipper scans each package upon pickup, confirming handoff from BRHI to the carrier.

2. **Transit Tracking**: Tracking updates are captured at each scan point in the carrier's network:
   - Pickup scan
   - Arrival at carrier sorting facility
   - Departure from sorting facility
   - Out for delivery
   - Delivered (or attempted delivery)

3. **Customer-Facing Tracking Page**: The customer can track their order on buildright.com/tracking or via the mobile app. The tracking page displays real-time status, estimated delivery date, and a map of the package's journey. The page also links to the carrier's detailed tracking page.

4. **Exception Alerts for Delays**: If a delay is identified (weather event, carrier mechanical issue, sort facility backlog, missed scan), the OMS triggers an exception alert. The customer is notified within **2 hours** of a known delay via email and/or SMS. The notification includes the reason for the delay, the updated estimated delivery date, and contact information for customer service.

   The DC Customer Service team monitors exception queues and proactively communicates with carriers to resolve delays.

---

#### Step 2.6 — Delivery Confirmation

| Attribute | Detail |
|---|---|
| **Step ID** | O2C-2.6 |
| **Swimlane** | WH / OM |
| **Trigger** | Order delivered to customer. |

1. **Proof of Delivery (POD) Captured**: Upon successful delivery, the following POD data is captured:
   - **Customer Signature**: Electronic signature captured on the delivery driver's handheld device. For scheduled deliveries, the signature is captured on the delivery team's tablet. For parcel carrier deliveries, the carrier captures the signature.
   - **Timestamped Photo**: For scheduled deliveries (appliances, installations, building materials), the delivery team takes a timestamped photo of the delivered items in the customer's designated location. This photo serves as visual proof of delivery condition and placement.
   - **Delivery Timestamp**: The exact date and time of delivery is recorded from the carrier's system.

2. **Status Update in Oracle Financials Cloud**: The POD triggers a status update in Oracle Financials Cloud. The sales order status changes from "In Delivery" to "Completed." This status change is the trigger for the billing process (Phase 3). For Pro accounts, the open item becomes billable.

3. **Delivery Rating Request**: Within 24 hours of delivery confirmation, the customer receives a delivery rating request via email. The customer is asked to rate the delivery experience on a 1-5 star scale and may provide optional comments. Ratings are captured in Salesforce CRM and used for carrier and delivery team performance monitoring.

At this point, the fulfillment phase is complete and the process transitions to Phase 3 (Billing).

---

### Phase 3: Billing

**Objective**: Generate accurate invoices, apply correct taxation, recognize revenue in accordance with ASC 606, and handle billing exceptions.

---

#### Step 3.1 — Invoice Auto-Generated

| Attribute | Detail |
|---|---|
| **Step ID** | O2C-3.1 |
| **Swimlane** | FIN / OM |
| **Trigger** | Delivery confirmed (POD) or POS transaction completed. |

Invoices are auto-generated by Oracle Financials Cloud based on the fulfillment channel:

**In-Store (POS)**: The invoice is generated at the point of sale at the time of transaction completion. The POS receipt serves as the invoice. The transaction is immediately recorded in Oracle Financials Cloud with the full revenue amount. No separate invoice is generated.

**E-Commerce / Ship-from-DC / Ship-from-Store / Vendor Direct-Ship**: The invoice is generated upon delivery confirmation (Step 2.6). The POD triggers Oracle Financials Cloud to create a billing document (invoice) with the following details:
- Invoice number (system-generated, sequential)
- Order number (SO-YYYYMMDD-XXXXXX)
- Customer name and address
- Invoice date (date of POD)
- Line items: SKU, description, quantity shipped, unit price, extended price
- Discounts applied
- Subtotal
- Tax
- Shipping charges (if applicable)
- Invoice total
- Payment terms (for retail: due immediately via authorized payment method; for Pro: Net 30)

**Pro Account**: Pro account invoices are generated as part of the monthly statement process (see Step 3.2). Individual transaction charges accumulate on the Pro account throughout the month and are consolidated into a single monthly statement.

---

#### Step 3.2 — Pro Billing

| Attribute | Detail |
|---|---|
| **Step ID** | O2C-3.2 |
| **Swimlane** | FIN |
| **Trigger** | First calendar day of each month. |

Pro account billing follows a monthly cycle:

1. **Monthly Statement Generation**: On the **1st day of each month**, Oracle Financials Cloud generates a consolidated statement for each active Pro account. The statement includes all charges (invoices) and credits (returns, credit memos) from the prior calendar month.

2. **Statement Contents**:
   - Pro account number and company name
   - Statement date and statement number
   - Billing period (prior month, e.g., March 1 – March 31)
   - Previous balance
   - Payments received during the period
   - New charges during the period (line-item detail):
     - PO number (as provided by the customer)
     - Item description
     - Quantity
     - Unit price
     - Extended price (quantity x unit price)
     - Tax
   - Credits applied during the period
   - New balance due
   - Payment due date (Day 30 from statement date, i.e., the last day of the current month)
   - Payment remittance instructions (mailing address, ACH routing information, online payment portal)

3. **Statement Delivery**: Statements are delivered via both email and USPS mail. Email statements are sent on the 1st of the month. Mailed statements are printed and sent via first-class mail on the 1st (or next business day) and typically arrive within 3-5 business days.

4. **Payment Terms**: All Pro accounts are on **Net 30** payment terms. Payment is due in full by the 30th day from the statement date (i.e., the last day of the current month). For example, a March statement is due April 30.

---

#### Step 3.3 — Tax Calculation

| Attribute | Detail |
|---|---|
| **Step ID** | O2C-3.3 |
| **Swimlane** | POS / EC / FIN |
| **Trigger** | Order priced and ready for invoicing. |

Tax calculation is managed by the Vertex tax engine integrated with Oracle Financials Cloud and all sales channels:

**In-Store**: Real-time tax calculation is performed at the point of sale. The POS system sends the transaction details (store location, item SKUs, prices, customer information) to Vertex, which returns the applicable tax amount based on the store's jurisdiction. Tax is applied to the transaction and printed on the receipt.

**E-Commerce**: Real-time tax calculation is performed at checkout. The e-commerce platform sends the transaction details (ship-to address, item SKUs, prices, customer information) to Vertex, which returns the applicable tax amount based on the delivery address jurisdiction. Tax is displayed to the customer during checkout and applied to the order total.

**Monthly True-Up**: Vertex maintains current tax rates and rules. BRHI performs a monthly true-up process to reconcile any rate changes that occurred during the prior month. The true-up ensures that all transactions reflect the correct rates for the applicable period.

**Tax-Exempt Processing**: Qualified Pro customers may be exempt from sales tax. The following exemptions are supported:
- **Resale Certificate**: Pro customers who resell BRHI products provide a valid resale certificate (state-specific form). The certificate is scanned and stored in Oracle Financials Cloud and the CRM. Tax is not charged on qualifying items when a valid resale certificate is on file.
- **Government Exemption**: Federal, state, and local government entities are exempt from sales tax. A government exemption certificate or purchase order is required. Tax is not charged when a valid government exemption is on file.

Exemption certificates are reviewed annually for continued validity. Expired certificates trigger a notification to the Pro Desk and AR team.

---

#### Step 3.4 — Revenue Recognition (ASC 606)

| Attribute | Detail |
|---|---|
| **Step ID** | O2C-3.4 |
| **Swimlane** | FIN |
| **Trigger** | Performance obligation satisfied. |

Revenue is recognized in accordance with ASC 606 (Revenue from Contracts with Customers) based on the transfer of control to the customer:

| Revenue Type | Recognition Point | Rationale |
|---|---|---|
| **In-Store Sales** | At register (point of sale) | Customer obtains control of the product at the point of sale. The customer takes physical possession and assumes all risks and rewards of ownership. |
| **Delivery Sales (E-Commerce, Pro Ship-to-Home)** | At proof of delivery (POD) | Customer obtains control upon delivery. POD (signature + timestamp) is the evidence of transfer of control. |
| **Installation Services** | Upon completion of installation | The service performance obligation is satisfied when the installation is complete and the customer accepts the work. Installation revenue is recognized separately from product revenue if the installation is a distinct performance obligation. |
| **Gift Cards** | Upon redemption | The purchase of a gift card creates a contract liability (deferred revenue). Revenue is recognized when the gift card is redeemed for merchandise. Gift cards do not expire. Unredeemed gift card balances are monitored and recognized per state escheatment laws. |
| **Extended Warranties** | Over the warranty period (straight-line) | Extended warranties represent a service performance obligation. Revenue is deferred at the time of sale and recognized on a straight-line basis over the warranty coverage period (e.g., a 3-year extended warranty sold for $300 results in $100 of revenue recognized per year). |

Revenue recognition entries are posted automatically in Oracle Financials Cloud based on the defined rules. Manual override requires Controller approval and is documented with justification.

---

#### Step 3.5 — Exception Handling

| Attribute | Detail |
|---|---|
| **Step ID** | O2C-3.5 |
| **Swimlane** | FIN / SA / OM |
| **Trigger** | Billing exception identified. |

The following billing exceptions are handled per established procedures:

**Pricing Discrepancy**: If the invoiced price does not match the expected price (shelf tag, promotional price, contract price), the exception is routed to the Pricing team for investigation. The Pricing team verifies the correct price within **4 hours** (SLA). If the discrepancy is confirmed, a credit memo is issued for the difference. If the customer was undercharged, the Pricing team determines whether to absorb the difference or issue a supplementary invoice (for Pro accounts only — retail discrepancies in the customer's favor are always resolved in the customer's favor).

**Missing Item**: If an item is confirmed as shipped but the customer reports it as missing from the delivery, the Order Management team investigates. The team verifies packing records, carrier weight data, and delivery photos. If the item is confirmed missing, a replacement is shipped from an alternate location within **24 hours** (SLA). If no replacement inventory is available, a credit/refund is issued.

**Damaged Goods**: If the customer reports damaged goods upon delivery, the DC Customer Service team initiates a return/replace process within **48 hours** (SLA). A carrier claim is filed simultaneously. The customer is offered the choice of replacement or refund. See Phase 5 for the full returns process.

**Incorrect Pro Pricing**: If a Pro customer disputes the pricing on their invoice (does not match contract terms), the exception is routed to the Pro Desk Manager for investigation. The Pro Desk Manager compares the invoiced price to the customer's contract agreement. If an error is confirmed, a credit memo is issued for the difference and the pricing record is corrected. If the contract terms are ambiguous, the dispute is escalated to the VP of Pro Business for resolution.

---

### Phase 4: Collections and Payment

**Objective**: Process and settle all incoming payments, manage Pro account collections, monitor aging, escalate past-due accounts, resolve disputes, and manage bad debt write-offs.

---

#### Step 4.1 — Payment Processing

| Attribute | Detail |
|---|---|
| **Step ID** | O2C-4.1 |
| **Swimlane** | FIN / POS |
| **Trigger** | Payment tender received or settlement due. |

Payments are processed based on the tender type:

**Credit Card Settlement**:

1. Credit card transactions settle on a **T+1 business day** basis.
2. Batch settlement occurs nightly at **11:00 PM ET**. The Adyen payment gateway submits the batch of authorized transactions for settlement.
3. Settlement amounts are captured against the authorization holds placed during Step 1.6.
4. The settlement is recorded in Oracle Financials Cloud as a cash receipt against the corresponding receivable.
5. Settlement reports from Adyen are reconciled daily against Oracle Financials Cloud records. Any discrepancies are investigated and resolved within 2 business days.

**Cash Deposit**:

1. Cash from in-store transactions is deposited the same day it is received.
2. **Dual Custody**: Cash deposits over $500 are counted and verified by two associates (the cashier and a supervisor). Both associates sign the deposit slip.
3. **Armored Car Pickup**: Armored car service picks up cash deposits on a **Monday / Wednesday / Friday** schedule. Deposits are sealed in tamper-evident bags with the deposit slip enclosed.
4. The daily deposit is reconciled against POS transaction records. Variances exceeding $5 trigger an investigation by Loss Prevention (see Controls and Compliance, Section 9).

**Check Deposit**:

1. Checks received from Pro customers (mail or in-store) are deposited the same day using remote deposit capture.
2. Checks are scanned via the desktop check scanner at the AR desk. The scanned image is transmitted to the bank for deposit.
3. The check amount is recorded against the Pro customer's account in Oracle Financials Cloud.
4. Physical checks are stored in a secure location for 90 days and then destroyed per BRHI document retention policy.

**Gift Card Redemption**:

1. Gift cards are redeemed at the POS or online at the time of purchase.
2. The redemption amount is deducted from the gift card balance in real time.
3. Revenue is recognized at the time of redemption (see Step 3.4).
4. Gift card redemptions are reconciled daily against gift card liability accounts in Oracle Financials Cloud.

---

#### Step 4.2 — Pro Account Collections

| Attribute | Detail |
|---|---|
| **Step ID** | O2C-4.2 |
| **Swimlane** | FIN |
| **Trigger** | Monthly statement generated. |

Pro account collections follow a structured monthly cycle:

1. **Statement Generated**: Day 1 of the month — the monthly statement is generated and delivered to the Pro customer (see Step 3.2).

2. **Payment Due**: Day 30 — payment is due in full. Accepted payment methods for Pro accounts:
   - **ACH (Preferred)**: Pro customers are encouraged to pay via ACH electronic funds transfer. ACH payments are processed through the BRHI lockbox bank. ACH details are printed on the monthly statement. ACH payments post to the Pro account within 1 business day of receipt.
   - **Check**: Pro customers may mail a check to the BRHI lockbox address. Checks are processed via remote deposit capture. Check payments post to the Pro account within 1-2 business days of receipt.
   - **Wire Transfer**: Pro customers may initiate a wire transfer for high-value payments. Wire details are provided upon request. Wire payments post to the Pro account on the day of receipt.
   - **Credit Card**: Pro customers may pay by credit card. A **2% surcharge** applies to credit card payments on Pro accounts over $5,000 to offset merchant processing fees. This surcharge is disclosed at the time of payment.

3. **Payment Application**: All payments are applied to the Pro customer's account in Oracle Financials Cloud. Payments are matched to open invoices using the invoice number or PO number provided by the customer. Unmatched payments are researched and applied within 2 business days.

---

#### Step 4.3 — Aging Management

| Attribute | Detail |
|---|---|
| **Step ID** | O2C-4.3 |
| **Swimlane** | FIN |
| **Trigger** | Weekly aging review. |

The AR Manager reviews the Pro account aging report weekly:

1. **Aging Buckets**: The aging report categorizes all open Pro account receivables into the following buckets:

   | Aging Bucket | Description |
   |---|---|
   | **Current** | Invoices not yet due (0-30 days from statement date) |
   | **31-60 Days** | Invoices 1-30 days past due |
   | **61-90 Days** | Invoices 31-60 days past due |
   | **91-120 Days** | Invoices 61-90 days past due |
   | **120+ Days** | Invoices more than 90 days past due |

2. **Flagging Past-Due Accounts**: Accounts that fall into the 31-60 day bucket or higher are flagged for action. The AR Manager assigns these accounts to AR Specialists for follow-up based on the escalation schedule (Step 4.4).

3. **Weekly Review Meeting**: The AR Manager, AR Specialists, and Controller meet weekly to review the aging report, discuss problematic accounts, and assign actions. Meeting minutes are documented and action items are tracked to completion.

4. **Management Reporting**: The aging report is included in the monthly Finance management reporting package distributed to the CFO and VP of Pro Business. Key metrics include total Pro receivables, aging distribution, DSO, and CEI (see KPIs, Section 8).

---

#### Step 4.4 — Late Payment Escalation

| Attribute | Detail |
|---|---|
| **Step ID** | O2C-4.4 |
| **Swimlane** | FIN |
| **Trigger** | Pro account payment past due. |

The following escalation schedule applies to past-due Pro accounts:

| Day Past Due | Action | Responsible Party |
|---|---|---|
| **Day 31** | **Automated Reminder Email**: System sends an automated email to the Pro customer's registered email address reminding them of the past-due balance. The email includes the amount due, a summary of outstanding invoices, and payment instructions. | System (automated) |
| **Day 45** | **Phone Call**: The AR Specialist assigned to the account places a phone call to the Pro customer's accounts payable contact. The AR Specialist makes a minimum of **2 attempts** on different days and at different times of day. Each attempt and the outcome are logged in Salesforce CRM. | AR Specialist |
| **Day 60** | **Formal Demand Letter**: A formal demand letter is sent via certified mail (USPS) to the Pro customer's business address. The letter specifies the amount due, the invoices outstanding, the payment deadline (15 days from letter date), and the consequences of continued non-payment (account hold, collection referral). | AR Specialist (drafted), AR Manager (approved) |
| **Day 90** | **Account Placed on Hold**: The Pro account is placed on credit hold. No new orders or shipments are processed for the account until the past-due balance is resolved or a payment plan is agreed upon. The Pro Desk is notified of the hold. The customer is notified via email and phone. | AR Manager |
| **Day 120** | **Third-Party Collection Agency**: The account is referred to BRHI's contracted third-party collection agency. The agency works the account on a contingency fee basis (25-33% of recovered amount, depending on account age and complexity). All collection activity is logged and reported monthly by the agency. | AR Manager (referral), Collection Agency (execution) |
| **Day 180** | **Legal Review**: Accounts that remain unresolved after 180 days are referred to BRHI's legal counsel for litigation consideration. Legal counsel evaluates the likelihood of recovery, the cost of litigation, and the strategic implications. Litigation is pursued only when approved by the CFO. | AR Manager (referral), Legal Counsel (evaluation), CFO (approval) |

---

#### Step 4.5 — Dispute Resolution

| Attribute | Detail |
|---|---|
| **Step ID** | O2C-4.5 |
| **Swimlane** | FIN / SA |
| **Trigger** | Customer contacts AR or Pro Desk regarding a billing dispute. |

The dispute resolution process ensures that customer billing disputes are investigated and resolved promptly:

1. **Dispute Initiation**: The customer contacts the AR team (via phone at 1-800-BRHI-BILL, email at ar@buildright.com, or the online portal) or the Pro Desk (in-store or via the Pro phone line) to report a billing dispute. The dispute may involve a pricing error, incorrect quantity, missing item, damaged goods, duplicate charge, or contract terms disagreement.

2. **Research Initiated**: The AR Specialist opens a dispute case in Salesforce CRM and begins research within **48 hours** of receipt. The Specialist gathers the following documentation:
   - Purchase order (PO) from the customer
   - Delivery receipt / proof of delivery (POD)
   - Invoice or statement in question
   - Pro contract / pricing agreement (if applicable)
   - Correspondence history with the customer

3. **Resolution and Approval Authority**: The AR Specialist investigates the dispute and determines the appropriate resolution (credit memo, invoice correction, payment plan, etc.). The resolution requires approval based on the following authority matrix:

   | Dispute Amount | Approval Authority |
   |---|---|
   | $0 – $500 | AR Specialist |
   | $500 – $5,000 | AR Manager |
   | $5,000 – $50,000 | Controller |
   | >$50,000 | CFO |

4. **Credit Memo Issued**: Upon approval, a credit memo is generated in Oracle Financials Cloud and applied to the customer's account. The credit memo references the original invoice, the dispute case number, and the reason for the credit.

5. **Customer Notification**: The customer is notified of the resolution within **5 business days** of the dispute case being opened. The notification includes the resolution details, the credit memo number and amount (if applicable), and any corrective actions taken to prevent recurrence.

6. **Dispute Tracking**: All disputes are tracked in Salesforce CRM with full case history, documentation, resolution, and aging. Dispute metrics (volume, aging, root cause) are included in the monthly AR management report.

---

#### Step 4.6 — Write-Off

| Attribute | Detail |
|---|---|
| **Step ID** | O2C-4.6 |
| **Swimlane** | FIN |
| **Trigger** | Account delinquent 180+ days. |

Bad debt write-offs are managed through a controlled approval process:

1. **Quarterly Review**: Accounts that are **180+ days delinquent** are reviewed quarterly (January, April, July, October) by the AR Manager and Controller. The review considers the account's collection history, the collection agency's recovery assessment, the customer's financial condition, and the cost of continued collection effort.

2. **Write-Off Approval Authority**:

   | Write-Off Amount | Approval Required |
   |---|---|
   | Less than $10,000 | AR Manager + Controller (dual approval) |
   | $10,000 – $50,000 | CFO approval |
   | Greater than $50,000 | CFO + CEO (dual approval) |

3. **Write-Off Execution**: Upon approval, the AR Specialist processes the write-off in Oracle Financials Cloud. The bad debt expense is recorded in the appropriate GL account. The customer's account balance is reduced by the written-off amount. A write-off memo is created documenting the approval, the reason, and the amount.

4. **Continued Collection Effort**: A write-off does not extinguish the debt. The account remains with the collection agency for continued recovery efforts. Any amounts recovered after write-off are recorded as **bad debt recovery** in the period received.

5. **Reporting**: Write-off activity is reported in the quarterly financial reporting package. Total bad debt expense as a percentage of revenue is tracked as a KPI (target: <0.1% of revenue).

---

### Phase 5: Returns and Credits

**Objective**: Process customer returns efficiently and accurately, issue refunds or store credits, disposition returned inventory, and maintain financial controls over return transactions.

---

#### Step 5.1 — Customer Initiates Return

| Attribute | Detail |
|---|---|
| **Step ID** | O2C-5.1 |
| **Swimlane** | CUST |
| **Trigger** | Customer decides to return merchandise. |

The customer initiates the return through the appropriate channel:

**In-Store at Service Desk**: Retail customers bring the merchandise and proof of purchase (receipt, credit card used, or loyalty account lookup) to the Service Desk located at the front of each store. The Service Desk is staffed during all store operating hours.

**Online at buildright.com/returns**: E-commerce customers can initiate a return online. The customer logs in to their account, selects the order, and chooses the item(s) to return along with the reason. The system generates a prepaid return shipping label (for ship-to-home orders) or directs the customer to the nearest store for in-person return (for BOPIS orders). Online-initiated returns can also be dropped off at any BRHI store.

**Pro Desk**: Pro customers initiate returns through the Pro Desk (in-store or by calling the Pro phone line at 1-800-PRO-BUILD). The Pro Desk representative assists with the return, verifies the Pro account, and processes the credit to the account.

---

#### Step 5.2 — Return Authorization

| Attribute | Detail |
|---|---|
| **Step ID** | O2C-5.2 |
| **Swimlane** | SA / POS |
| **Trigger** | Return request received. |

The associate verifies the return eligibility:

1. **Verify Purchase**: The associate confirms the purchase using one of the following methods:
   - **Receipt Scan**: The barcode on the original receipt is scanned to pull up the transaction.
   - **Credit Card Lookup**: The last 4 digits of the credit card used for the original purchase are entered to locate the transaction. The system displays all transactions matching the card within the return eligibility period.
   - **Pro Account Lookup**: For Pro customers, the associate looks up the transaction on the Pro account using the order number or invoice number.
   - **Transaction ID**: The transaction ID from the receipt or email confirmation is entered.

2. **Check Eligibility per Return Policy**:

   | Return Type | Eligibility Period | Conditions |
   |---|---|---|
   | **Standard Return** | 90 days from purchase | Item must be unused, in original packaging, with all parts and accessories. |
   | **BuildRight Brand Products** | 365 days from purchase | BuildRight private-label products carry an extended return window. Item must be in returnable condition. |
   | **No-Receipt Return** | Within return policy period | Limited to **3 returns per 12-month rolling period** per customer. Valid government-issued photo ID required. See Business Rule BR-O2C-010. |

3. **Inspect Condition**: The associate inspects the returned item:
   - Is the item unused?
   - Is the original packaging intact?
   - Are all parts, accessories, and manuals included?
   - Are there any signs of damage that were not present at the time of purchase?

   If the item does not meet the return condition requirements, the associate may decline the return or offer a reduced refund (e.g., open-box value). Declined returns are logged in the POS system.

---

#### Step 5.3 — Refund Processing

| Attribute | Detail |
|---|---|
| **Step ID** | O2C-5.3 |
| **Swimlane** | SA / POS |
| **Trigger** | Return authorized. |

The refund is processed based on the refund method:

**Original Tender Refund**: The refund is issued to the original payment method used for the purchase.

| Original Payment Method | Refund Method | Processing Time |
|---|---|---|
| Credit Card | Credit card refund to original card | 3-5 business days |
| Debit Card | Debit card refund to original card | 5-10 business days |
| Cash | Cash refund at Service Desk | Immediate |
| Pro Account | Credit memo to Pro account | Immediate (applied to account balance) |
| Gift Card | Refund to original gift card (if available) or new gift card | Immediate |

**Store Credit (BuildRight Gift Card)**: If the customer prefers store credit or does not have the original payment method, the refund is issued as a BuildRight Gift Card. The gift card is issued immediately with no expiration date and no fees. Store credit is redeemable at all BRHI channels.

**Exchange**: The customer may exchange the returned item for a different item. If the new item is the same price, it is an even trade. If the new item costs more, the customer pays the difference. If the new item costs less, the difference is refunded via the original tender method or as store credit.

**Authorization Matrix**: Refund authorization is enforced in the POS system. Associates cannot process refunds above their authorization level without the required manager login:

| Refund Amount | Authorization Required |
|---|---|
| $0 – $50 | Cashier |
| $50 – $200 | Supervisor |
| $200 – $1,000 | Manager (Assistant Store Manager or higher) |
| $1,000+ | Store Manager only |

The POS system enforces this hierarchy — an associate cannot bypass the authorization requirement. Each authorized refund is logged with the authorizer's employee ID, timestamp, and reason code.

---

#### Step 5.4 — Inventory Disposition

| Attribute | Detail |
|---|---|
| **Step ID** | O2C-5.4 |
| **Swimlane** | WH / SA |
| **Trigger** | Return processed and item received. |

Returned inventory is dispositioned based on the condition and type:

1. **Return to Shelf**: If the item is sellable and in its original packaging with all parts and accessories, the associate scans the item back into inventory using the POS system. The item is returned to the sales floor shelf and is immediately available for sale.

2. **RTV (Return to Vendor)**: If the item is defective or the vendor accepts returns for credit, the associate initiates a vendor Return Merchandise Authorization (RMA). The RMA request is submitted to the vendor via EDI or the vendor portal. Upon vendor approval, the item is packaged and shipped back to the vendor within **14 days**. Vendor credit is recorded upon receipt of the credit memo from the vendor.

3. **Markdown**: If the item is shopworn, has damaged packaging, or is otherwise not suitable for sale at full price but is still functional, a markdown is applied. The markdown follows the established markdown schedule (e.g., 25% off for open box, 50% off for damaged packaging). The item is placed on the clearance rack or designated markdown area.

4. **Donate**: If the item is sellable but not economical to restock (e.g., low-value items, discontinued products with no RTV option), the item may be donated to an approved charity. Donations must be approved by the Store Manager and are logged in the donation tracking system. BRHI maintains relationships with approved charities including Habitat for Humanity ReStore and local community organizations.

5. **Dispose**: If the item is unsellable and cannot be returned to vendor or donated (e.g., hazardous materials, broken items, recalled products), the item is disposed of per the Environmental SOP. Hazardous materials are handled per OSHA and EPA guidelines. Disposal is documented and logged for environmental compliance records.

---

#### Step 5.5 — Credit Memo and Reporting

| Attribute | Detail |
|---|---|
| **Step ID** | O2C-5.5 |
| **Swimlane** | FIN / POS |
| **Trigger** | Return completed and refund issued. |

1. **Credit Memo Generated in Oracle Financials Cloud**: A credit memo is automatically generated in Oracle Financials Cloud for every return transaction. The credit memo includes:
   - Credit memo number (system-generated)
   - Original order/invoice number
   - Customer number
   - Returned item(s): SKU, description, quantity, unit price, extended price
   - Refund amount and method
   - Reason code (customer reason for return)
   - Associate and authorizer IDs

   The credit memo offsets the original revenue entry and reduces the customer's account balance (Pro accounts) or records the refund liability (retail credit card refunds).

2. **Vendor Chargeback**: For defective merchandise returned under warranty or vendor quality issues, a vendor chargeback is processed. The Purchasing team submits the chargeback to the vendor for the cost of the returned item plus any associated handling costs. The chargeback is tracked to resolution.

3. **Daily Return Report**: A daily return report is generated from the POS system and reviewed by Loss Prevention. The report includes all returns processed during the previous day, sorted by store and associate. Loss Prevention reviews the report for anomalies including:
   - High volume of returns by a single customer
   - High-dollar returns
   - Returns processed by the same associate repeatedly
   - Returns without receipts exceeding policy limits
   - Returns of high-theft items (power tools, electronics)

4. **Weekly Return Trend Analysis**: The Finance team produces a weekly return trend analysis report. The report tracks:
   - Return rate by category and SKU
   - Return reason distribution
   - Return rate by store
   - Return rate by channel (in-store vs. online)
   - Trend comparison to prior periods (week-over-week, year-over-year)

   Significant variances from historical trends are investigated and root causes are addressed. The weekly report is distributed to Store Operations, Merchandising, and Finance leadership.

---

## 6. System Landscape

The O2C process is supported by the following integrated systems:

### POS — NCR Emerald

- **Function**: In-store point-of-sale transaction processing.
- **Capabilities**: Real-time inventory decrement upon sale, customer lookup (loyalty, Pro account), payment processing integration (Adyen), receipt printing, return processing, price override with authorization, end-of-day register reconciliation.
- **Integration**: Oracle Financials Cloud (order and financial posting), Salesforce CRM (customer data), Adyen (payment processing), Vertex (tax calculation), Manhattan WMS (inventory updates).

### E-Commerce — Salesforce Commerce Cloud

- **Function**: Online and mobile storefront for buildright.com and the BRHI mobile app.
- **Capabilities**: Product catalog and search, shopping cart and checkout, customer account management, BOPIS and ship-to-home selection, promotional pricing and coupon management, order history and tracking, return initiation.
- **Integration**: IBM Sterling OMS (order routing), Oracle Financials Cloud (order creation), Adyen (payment processing), Salesforce CRM (customer data), Vertex (tax calculation).

### ERP — Oracle Fusion Cloud ERP

- **Function**: Central enterprise resource planning system.
- **Modules Used in O2C**:
  - **SD (Sales and Distribution)**: Sales order management, pricing, delivery, billing.
  - **FI-AR (Financial Accounting — Accounts Receivable)**: Invoice management, payment processing, aging, credit memos, dunning.
  - **MM (Materials Management)**: Inventory management, goods receipt/issue, ATP.
  - **CO (Controlling)**: Revenue and cost tracking, profitability analysis.
- **Integration**: NCR Emerald POS, Salesforce Commerce Cloud, IBM Sterling OMS, Manhattan WMS, Vertex, Salesforce CRM, Adyen.

### WMS — Manhattan Associates

- **Function**: Distribution center warehouse management.
- **Capabilities**: Wave planning and release, RF-directed picking, pack station management, quality checks, carrier label generation, inventory management, cycle counting, replenishment.
- **Integration**: Oracle Financials Cloud (inventory and order data), IBM Sterling OMS (fulfillment status), carrier systems (tracking number generation).

### CRM — Salesforce

- **Function**: Customer relationship management.
- **Capabilities**: Customer record management (retail and Pro), Pro account profiles, interaction history (calls, emails, in-store visits), loyalty program management, dispute case management, marketing segmentation.
- **Integration**: Oracle Financials Cloud (Pro account and billing data), NCR Emerald POS (customer lookup), Salesforce Commerce Cloud (online customer data), IBM Sterling OMS (order history).

### Payment Gateway — Adyen

- **Function**: Multi-channel payment processing.
- **Capabilities**: Credit and debit card processing (Visa, Mastercard, Amex, Discover), tokenization for stored card data, multi-channel support (POS, e-commerce, mobile), PCI Level 1 compliance, chargeback management, settlement reporting.
- **Integration**: NCR Emerald POS (card-present), Salesforce Commerce Cloud (card-not-present), Oracle Financials Cloud (settlement and reconciliation).

### Tax Engine — Vertex

- **Function**: Real-time sales tax calculation and compliance.
- **Capabilities**: Real-time tax calculation based on jurisdiction (store location or ship-to address), exemption certificate management, tax filing support (monthly/quarterly), rate change updates, nexus monitoring.
- **Integration**: NCR Emerald POS, Salesforce Commerce Cloud, Oracle Financials Cloud (tax posting).

### OMS — IBM Sterling

- **Function**: Order management and fulfillment optimization.
- **Capabilities**: Order routing (BOPIS, ship-from-store, ship-from-DC, vendor direct-ship), inventory visibility across the entire network (stores, DCs, vendor ATP), fulfillment optimization, promise date calculation, exception management.
- **Integration**: Oracle Financials Cloud (order data), Salesforce Commerce Cloud (online orders), Manhattan WMS (DC fulfillment), NCR Emerald POS (store inventory and BOPIS), carrier APIs (tracking).

### System Integration Architecture

All systems are integrated via a combination of real-time APIs (REST/SOAP) for synchronous transactions (e.g., payment authorization, tax calculation, inventory lookup) and batch EDI/file feeds for asynchronous processes (e.g., settlement reconciliation, vendor order transmission, reporting). The integration layer is managed by BRHI's IT team with monitoring for latency, error rates, and data quality.

---

## 7. Business Rules

The following business rules govern the O2C process:

### BR-O2C-001: Minimum Pro Delivery Order

The minimum order value for a Pro delivery (ship-to-job-site) is **$250**. Orders below $250 are available for BOPIS or Pro customer pickup at the store. This minimum does not apply to Pro orders picked up in-store.

### BR-O2C-002: Maximum Store Credit Without Receipt

The maximum store credit (BuildRight Gift Card) issued for a return without a receipt is **$250 per return**. Each customer is limited to **3 no-receipt returns per 12-month rolling period**. Returns exceeding these limits are declined. The customer's return history is tracked in the CRM by government-issued photo ID number.

### BR-O2C-003: Price Match Policy

BRHI will match the price of an identical item (same brand, model, size, and specifications) found at a local competitor brick-and-mortar store, plus an additional **10% of the difference** between BRHI's price and the competitor's price.

**Exclusions**: The price match policy does not apply to:
- Clearance or closeout items
- Installation services
- Special order items
- Prices from online-only retailers (e.g., Amazon, Wayfair)
- Competitor prices that require a paid membership (e.g., Costco, Sam's Club)
- Competitor prices resulting from typographical errors
- Bundled or package deals

The competitor price must be verified by the associate (printed ad, phone verification, or competitor website for brick-and-mortar stores). Price match transactions are logged for audit and trend analysis.

### BR-O2C-004: Restocking Fee for Special Orders

A restocking fee of **15%** is applied to special order items that are returned. Special orders are defined as items that BRHI does not stock in regular store or DC inventory and were ordered specifically for the customer from the vendor.

**Waiver**: The restocking fee is waived for **Pro Elite** tier customers. Pro Member and VIP customers are subject to the restocking fee.

The restocking fee is disclosed to the customer at the time the special order is placed and is printed on the order confirmation.

### BR-O2C-005: Credit Card Authorization Validity

Credit card authorizations are valid for **7 calendar days** from the date of authorization. If order fulfillment (shipment or BOPIS pickup) will not occur within 7 calendar days, the system automatically initiates a re-authorization:

1. The original authorization is released.
2. A new authorization for the current order total is obtained from the card issuer.
3. If the re-authorization fails (e.g., card expired, insufficient funds, account closed), the customer is notified and given 3 business days to provide updated payment information.
4. If the customer does not respond within 3 business days, the order is cancelled.

### BR-O2C-006: Gift Card Terms

- Maximum gift card balance: **$500** per card.
- No expiration date on any BuildRight Gift Card.
- No fees (no dormancy fees, no maintenance fees).
- Redeemable at all BRHI channels: in-store POS, buildright.com, mobile app.
- Gift cards cannot be used to purchase other gift cards.
- Lost or stolen gift cards are not replaceable unless the customer has the gift card number and proof of purchase.

### BR-O2C-007: Pro Credit Limits

Pro account credit limits by tier:

| Pro Tier | Credit Limit | Requirements |
|---|---|---|
| **Member** | $5,000 | Business license, basic credit application |
| **VIP** | $50,000 | Member requirements + 12+ months payment history, trade references |
| **Elite** | $500,000 | VIP requirements + audited financial statements, 24+ months payment history, Dunn & Bradstreet report |

Credit limit increases require a formal credit review conducted by the AR/Credit team. The review evaluates the customer's financial statements, trade references, payment history with BRHI, and external credit reports (D&B, Experian Business). Increases are approved per the authority matrix:

- Increase to $50,000 or below: AR Manager approval
- Increase to $500,000 or below: Controller approval
- Increase above $500,000: CFO approval

### BR-O2C-008: Delivery Charges

| Delivery Type | Charge | Conditions |
|---|---|---|
| **Standard Delivery** | Free | Orders over $49 |
| **Standard Delivery** | $5.99 | Orders under $49 |
| **Express Next-Day Delivery** | $35 | Available in select metro areas; order must be placed by 2:00 PM local time |
| **Pro Priority Delivery** | Free | All Pro tiers, all order sizes (subject to BR-O2C-001 minimum) |
| **Appliance Delivery** | Free | Appliance orders over $399 |
| **Appliance Delivery** | $59.99 | Appliance orders under $399 |

### BR-O2C-009: BOPIS Hold Limit

BOPIS orders are held at the store for **48 hours** from the time the "Ready for Pickup" notification is sent to the customer. If the customer does not pick up the order within 48 hours:

1. The order is automatically cancelled.
2. Inventory is restored to available stock in the perpetual inventory system.
3. The customer is notified of the cancellation via email.
4. If the customer still wants the items, they must place a new order.
5. Payment authorization is released (credit card) or reversed (gift card balance restored).

### BR-O2C-010: Returns Without Receipt

Returns without a receipt are processed under the following conditions:

- The customer receives store credit (BuildRight Gift Card) at the **lowest sale price in the prior 365 days** for the returned item.
- A valid **government-issued photo ID** is required (driver's license, state ID, passport, military ID). The ID number is recorded in the CRM.
- Each customer is limited to **3 no-receipt returns per 12-month rolling period**, tracked by government-issued photo ID number across all BRHI channels.
- No-receipt returns exceeding $250 are declined and escalated to the Store Manager for exception review.
- Exceptions to the 3-return limit require District Manager approval.

---

## 8. Key Performance Indicators (KPIs)

The following KPIs are monitored to measure O2C process performance:

### Operational KPIs

| KPI | Definition | Target | Measurement Frequency |
|---|---|---|---|
| **Order Accuracy** | Percentage of orders fulfilled with correct items, quantities, and pricing on the first attempt. | 99.5% | Weekly |
| **On-Time Delivery** | Percentage of delivered orders arriving within the promised delivery window. | 98% | Weekly |
| **Average Order-to-Delivery Time (E-Commerce)** | Average elapsed time from online order placement to delivery confirmation. | 2.5 days | Weekly |
| **BOPIS Ready Time** | Average elapsed time from order confirmation to customer notification that the order is ready for pickup. | Less than 2 hours | Daily |
| **BOPIS Pickup Rate** | Percentage of BOPIS orders picked up within 24 hours of the "Ready for Pickup" notification. | 85% | Weekly |
| **Return Rate** | Total returns as a percentage of total sales (by dollar value). | Less than 8% | Monthly |

### Financial KPIs

| KPI | Definition | Target | Measurement Frequency |
|---|---|---|---|
| **Days Sales Outstanding (DSO) — Pro Accounts** | Average number of days from invoice date to payment receipt for Pro account receivables. Calculated as: (Average Pro AR Balance / Pro Credit Sales) x Number of Days in Period. | 35 days | Monthly |
| **Collection Effectiveness Index (CEI)** | Measures the effectiveness of the collections function. Calculated as: (Beginning AR + Credit Sales – Ending AR) / (Beginning AR + Credit Sales – Ending Current AR) x 100. | 95% | Monthly |
| **First-Pass Invoice Yield** | Percentage of invoices that match and post without manual intervention or correction. | 97% | Monthly |
| **Bad Debt Expense** | Total bad debt write-offs as a percentage of total revenue. | Less than 0.1% | Quarterly |
| **Pro Account Aging >90 Days** | Total Pro account receivables aged over 90 days as a percentage of total Pro account receivables. | Less than 5% | Monthly |

### KPI Reporting and Governance

- **Daily Dashboard**: BOPIS Ready Time is reported on a daily dashboard accessible to Store Operations and Fulfillment leadership.
- **Weekly Scorecard**: Order Accuracy, On-Time Delivery, Average Order-to-Delivery Time, and BOPIS Pickup Rate are reported on a weekly scorecard distributed to Operations, E-Commerce, and Finance leadership.
- **Monthly Financial Report**: DSO, CEI, First-Pass Invoice Yield, Return Rate, and Pro Account Aging are reported in the monthly Finance management reporting package.
- **Quarterly Business Review**: Bad Debt Expense and trend analysis for all KPIs are presented in the quarterly business review to the CFO and executive team.
- **Escalation Thresholds**: If any KPI falls below target for two consecutive reporting periods, the process owner (CFO) initiates a root cause analysis and corrective action plan.

---

## 9. Controls and Compliance

### SOX Controls

The following SOX (Sarbanes-Oxley) controls are in place for the O2C process:

**Revenue Recognition (ASC 606)**:
- The revenue recognition control framework is documented and tested quarterly by internal audit.
- Oracle Financials Cloud is configured to automatically apply the correct revenue recognition treatment based on transaction type (see Step 3.4).
- Manual overrides to automatic revenue recognition require Controller approval and documented justification.
- Revenue cutoff testing is performed at each quarter-end to ensure revenue is recorded in the correct period.

**Credit Approval Segregation**:
- Sales team members (sales associates, Pro Desk representatives) **cannot** approve credit limits for Pro customers.
- Credit limit establishment and increases are the exclusive responsibility of the AR/Credit team.
- This segregation of duties prevents sales personnel from extending credit to unqualified customers to meet sales targets.
- The control is enforced in Oracle Financials Cloud — credit limit fields require AR/Credit team authorization credentials.

**Refund Authorization Matrix**:
- The refund authorization matrix (see Step 5.3) is enforced in the POS system.
- Associates **cannot** process refunds above their authorization level without the required manager login.
- The POS system cannot be overridden — there is no "force" or "supervisor bypass" for refund authorization.
- All refund transactions are logged with the authorizer's employee ID, timestamp, and reason code.

**Manual Journal Entries**:
- Manual journal entries to revenue or AR accounts exceeding **$50,000** require dual approval (preparer + reviewer).
- The reviewer must be at the Manager level or above.
- Manual journal entries are reviewed by the Controller monthly.

**Monthly Reconciliation**:
- Revenue recorded in Oracle Financials Cloud is reconciled to cash receipts and bank deposits on a monthly basis.
- Reconciliation is performed by a Senior Accountant and reviewed by the Controller.
- Unreconciled items exceeding $1,000 are investigated and resolved within 5 business days.

### PCI DSS Compliance

BRHI is PCI DSS (Payment Card Industry Data Security Standard) compliant at the **SAQ-D** level:

**Point-to-Point Encryption (P2PE)**:
- All card-present transactions use P2PE encryption from the point of interaction (card reader) through to the payment gateway (Adyen).
- Cardholder data is encrypted at the moment of card swipe, dip, or tap and is never transmitted or stored in clear text within the BRHI environment.

**Network Segmentation**:
- The POS network operates on an **isolated VLAN** separate from the general corporate and guest networks.
- Firewall rules restrict traffic between the POS VLAN and other network segments to only the required communication paths (payment gateway, tax engine, Oracle Financials Cloud).

**Vulnerability Management**:
- **Quarterly ASV (Approved Scanning Vendor) Scans**: External vulnerability scans are performed quarterly by a PCI-approved scanning vendor.
- **Annual Penetration Test**: A comprehensive penetration test is performed annually by a qualified third-party firm.
- **SAQ-D Compliance Validation**: The Self-Assessment Questionnaire D is completed annually and attested by the CIO and CFO.

**Tokenization**:
- Stored card data (e.g., saved cards in customer profiles, recurring Pro payments) is tokenized by Adyen. BRHI stores only the token — not the actual card number.
- Tokenization ensures that even in the event of a data breach, cardholder data is not exposed.

**PCI Training**:
- All POS associates complete annual PCI awareness training covering: secure handling of cardholder data, recognition of skimming devices, phishing awareness, and incident reporting procedures.
- Training completion is tracked in the HR learning management system and reported to the PCI compliance officer.

### Sales Tax Compliance

**Automated Calculation**:
- All sales tax calculations are performed in real time by the Vertex tax engine, ensuring accuracy across all jurisdictions where BRHI has nexus.

**Exemption Certificate Management**:
- Tax exemption certificates (W-9 forms, resale certificates) are scanned and stored electronically in the Vertex exemption certificate management module.
- Exemption certificates are linked to the corresponding customer account in Oracle Financials Cloud and the CRM.
- Expiration dates are monitored, and customers are notified 60 days before expiration to provide renewed certificates.

**Monthly Reconciliation**:
- Sales tax collected in Oracle Financials Cloud is reconciled monthly to the tax returns filed in each jurisdiction.
- Variances exceeding $100 per jurisdiction are investigated and corrected.

**Annual True-Up**:
- An annual true-up process reconciles all tax collected to tax filed across all jurisdictions.
- Adjustments are recorded in the period identified.

**Nexus Monitoring**:
- Vertex monitors changes in tax law and nexus thresholds across all states and localities where BRHI operates.
- New nexus obligations are identified and communicated to the Tax team for registration and compliance.
- Economic nexus thresholds (post-Wayfair) are monitored for all states where BRHI exceeds the threshold based on sales volume and transaction count.

### Refund Controls

**Authorization Matrix Enforcement**:
- The POS system enforces the refund authorization matrix (see Step 5.3). Associates cannot process refunds without the required level of authorization.
- There is no system-level override. All refund transactions are captured with full audit trail.

**Pattern Detection (Loss Prevention)**:
- Loss Prevention reviews the **daily refund report** for anomalies:
  - High volume of returns by a single customer (more than 3 returns in a single day)
  - High-dollar returns (over $500)
  - Returns processed by the same associate repeatedly (more than 5 returns per associate per shift)
  - Returns of high-theft categories (power tools, electronics, small appliances)
  - No-receipt returns near the $250 limit (potential policy exploitation)
- Anomalies are flagged for investigation. Confirmed fraud is referred to Loss Prevention for formal investigation.

**Serial Number Verification**:
- For electronics and power tools, the serial number of the returned item is scanned and compared to the serial number on the original transaction.
- If the serial numbers do not match, the return is declined and flagged for Loss Prevention review.

**Gift Card Refund Monitoring (Anti-Money Laundering)**:
- Refunds issued as gift cards are monitored for patterns that may indicate money laundering or return fraud.
- Multiple refunds to gift cards by the same customer within a short period are flagged.
- Aggregate gift card refund balances exceeding $1,000 per customer per month are flagged for review.

### Cash Handling Controls

**Dual Custody**:
- Cash deposits exceeding **$500** require dual custody — two associates must count and verify the deposit together. Both associates sign the deposit slip.
- The dual custody requirement is enforced by store policy and verified via the POS end-of-day reconciliation process.

**Safe Counts**:
- The store safe is counted at **opening** and **closing** each day.
- The safe count is compared to the expected amount (prior close + deposits – withdrawals).
- Any variance exceeding **$5** triggers an immediate investigation by the Store Manager and a report to Loss Prevention.

**Armored Car Pickup**:
- Armored car pickup occurs on a **Monday / Wednesday / Friday** schedule at all store locations.
- Deposits are sealed in tamper-evident bags with the deposit slip enclosed. The armored car guard signs for each bag.
- The armored car receipt is reconciled to the POS deposit record the following business day.

**Surprise Cash Audits**:
- Loss Prevention conducts **quarterly surprise cash audits** at randomly selected store locations.
- The audit includes a count of all registers, safes, and petty cash funds.
- Audit findings are documented and reported to the Store Manager, District Manager, and Controller.
- Variances are investigated and resolved within 5 business days.

---

## 10. Exception Handling Matrix

The following table provides a comprehensive reference for handling O2C exceptions:

| Exception | Resolution Steps | Responsible Party | SLA | Escalation Path |
|---|---|---|---|---|
| **Price discrepancy (POS vs. shelf tag)** | 1. Verify shelf tag is current and correctly placed. 2. Check promotional pricing schedule in Oracle Financials Cloud. 3. Honor the lower of the displayed price (shelf tag) or system price per BRHI customer-first policy. 4. Correct the pricing in the system if shelf tag is accurate and system is wrong. 5. Notify Pricing team if the discrepancy is systemic (multiple items, multiple stores). | Department Supervisor | Immediate (at register) | Pricing Manager if systemic issue identified |
| **Online order out-of-stock (after order placed)** | 1. Check inventory at alternate store and DC locations. 2. If inventory available at alternate location, re-route order. 3. If no inventory available, contact customer to offer substitution (comparable item at same price). 4. If customer declines substitution, issue full refund. 5. Notify Buyer if out-of-stock is widespread across multiple locations. | Order Management Specialist | 4 hours from identification | Buyer if widespread stockout; Merchandising VP if chronic |
| **Delivery damage reported by customer** | 1. Document damage details (photos requested from customer, carrier claim form). 2. File carrier damage claim with supporting documentation. 3. Re-ship replacement item from nearest available location. 4. Issue credit for returned damaged item (customer may keep or return damaged item per carrier instructions). 5. Track carrier claim to resolution. | DC Customer Service Representative | 24 hours from customer report | Transportation Manager if recurring with same carrier; VP Operations if systemic |
| **Pro pricing dispute** | 1. Pull customer's contract pricing agreement from Oracle Financials Cloud. 2. Compare disputed invoice line items to contract terms. 3. If pricing error confirmed, issue credit memo for difference. 4. Correct pricing record in Oracle Financials Cloud to prevent recurrence. 5. If customer's interpretation differs, escalate for negotiation. | Pro Desk Manager | 48 hours from dispute receipt | VP Pro Business if disagreement on contract terms; Legal if contractual dispute |
| **Duplicate charge** | 1. Verify both transactions in POS/Oracle Financials Cloud (timestamps, amounts, authorization codes). 2. If duplicate confirmed, process immediate refund for the duplicate charge. 3. Document the duplicate with both transaction IDs. 4. Investigate root cause (system error, associate error). | Service Desk Supervisor | Immediate (at time of identification) | Store Manager if amount exceeds $500; IT if system-caused |
| **Return without receipt over limit** | 1. Decline the return per policy (3 per 12 months, $250 max per return). 2. Offer exchange as alternative (no cash/gift card refund). 3. If customer requests exception, escalate to Store Manager. 4. Store Manager evaluates on case-by-case basis (customer history, item value, circumstances). | Store Manager only (for exception review) | N/A (real-time decision) | District Manager if Store Manager approves exception; LP if pattern suspected |
| **Pro account over credit limit** | 1. System automatically places a hold on the order. 2. AR Specialist notified of the hold. 3. AR Specialist contacts Pro customer to inform them of the credit limit situation. 4. Options presented: (a) Make a payment to reduce balance, (b) Request a credit limit increase (requires credit review), (c) Split payment (partial on account, partial via credit card). 5. Once exposure is within limit, order is released. | AR Specialist | Same day as hold | AR Manager if customer is unresponsive within 2 business days; Controller for limit increase requests; CFO for limit increases above $50,000 |
| **Incorrect item shipped** | 1. Verify customer's claim (request photo of received item). 2. Check packing records and pick verification scans in WMS. 3. Ship correct item from nearest available location via expedited shipping at no charge. 4. Provide prepaid return label for incorrect item. 5. Record carrier claim if shipping error. | Order Management Specialist | 24 hours from customer report | DC Manager if picking error; Transportation Manager if carrier misroute |
| **Customer does not receive order (tracking shows delivered)** | 1. Verify delivery address on order. 2. Contact carrier for delivery details (GPS coordinates, delivery photo, signature). 3. If carrier confirms mis-delivery, file claim and re-ship. 4. If carrier confirms correct delivery, assist customer with checking with household members, neighbors, or building management. 5. If unresolved after 3 business days, issue refund or re-ship. | DC Customer Service Representative | 24 hours from customer report | Transportation Manager for carrier escalation; LP if fraud suspected |
| **System outage (POS or e-commerce)** | 1. IT notified immediately via monitoring alert or store call. 2. IT assesses scope and estimated recovery time. 3. If POS down: stores switch to offline mode (limited transaction processing, batch sync upon recovery). 4. If e-commerce down: display maintenance page with estimated recovery time. 5. Post-recovery: reconcile all transactions processed during outage. | IT Operations | POS: 1 hour; E-Commerce: 2 hours | IT Director if SLA breached; CIO if extended outage (>4 hours) |

---

## 11. Process Improvement Opportunities

The following initiatives have been identified to improve O2C process efficiency, accuracy, and customer experience:

### AI-Powered Demand Forecasting

**Current State**: Inventory replenishment is driven by historical sales data and manual buyer adjustments. In-stock rate averages 97%.

**Proposed Improvement**: Implement an AI-powered demand forecasting engine that incorporates historical sales patterns, weather data, local construction permits, seasonal trends, promotional calendars, and macroeconomic indicators to predict demand at the SKU-store level.

**Projected Impact**: Increase in-stock rate from **97% to 99%**, reduce lost sales due to stockouts, and decrease excess inventory carrying costs. Estimated annual benefit: $2.5M in incremental revenue and $1.2M in reduced markdowns.

**Status**: Pilot planned for Q3 2026 in the Southeast region.

### Dynamic Pricing Engine

**Current State**: Price matching is a manual process requiring associate verification and supervisor authorization. Competitive pricing intelligence is gathered weekly via manual checks.

**Proposed Improvement**: Implement a dynamic pricing engine that monitors competitor pricing in real time via web scraping and third-party data feeds, automatically adjusts BRHI online prices within defined guardrails, and generates price match alerts for in-store associates.

**Projected Impact**: Reduce price match processing time by 75%, increase competitive positioning, and improve price perception among customers. Estimated annual benefit: $800K in retained sales.

**Status**: Vendor evaluation in progress. Target implementation: Q4 2026.

### Mobile POS for Line-Busting

**Current State**: During peak periods (weekends, seasonal events, promotional launches), checkout lines exceed 10 minutes, resulting in cart abandonment and customer dissatisfaction.

**Proposed Improvement**: Deploy mobile POS devices (tablets with card readers) that allow associates to process transactions anywhere in the store. During peak periods, designated "line-busting" associates approach customers in line and process their transactions on the spot.

**Projected Impact**: Reduce average checkout wait time by **40%** (from 8 minutes to 4.8 minutes during peak). Increase customer satisfaction scores. Estimated annual benefit: $1.5M in reduced cart abandonment.

**Status**: Pilot completed in 5 stores (Q1 2026). Results positive. Rollout to all stores planned for Q3 2026.

### Automated Pro Account Collections with Predictive Payment Analytics

**Current State**: Pro account collections follow a manual escalation schedule (Step 4.4). AR Specialists review aging reports weekly and make phone calls based on aging buckets.

**Proposed Improvement**: Implement predictive payment analytics that analyze Pro customer payment behavior, financial indicators, and external credit data to predict which accounts are most likely to become delinquent. Automated communication workflows (email, SMS) are triggered based on risk scores. AR Specialists focus their time on high-risk accounts identified by the model.

**Projected Impact**: Reduce DSO from 35 days to **30 days**, reduce Pro account aging >90 days from 5% to **3%**, and improve CEI from 95% to **97%**. Estimated annual benefit: $1.8M in improved cash flow and $200K in reduced bad debt.

**Status**: RFP issued. Vendor selection planned for Q2 2026.

### Unified Commerce Platform

**Current State**: POS (NCR Emerald), e-commerce (Salesforce Commerce Cloud), and mobile app operate as separate front-end systems integrated via middleware. Customer experience is not fully seamless (e.g., online cart not available in-store, loyalty points visible in different formats).

**Proposed Improvement**: Migrate to a unified commerce platform that provides a single, consistent customer experience across all channels. Features include: real-time cart sync across devices, unified loyalty program, consistent pricing and promotions, and single customer view across channels.

**Projected Impact**: Improve customer satisfaction, increase cross-channel sales, reduce IT integration complexity and maintenance costs. Estimated annual benefit: $3M in incremental cross-channel revenue and $500K in IT cost savings.

**Status**: Long-term initiative. Business case under development. Target implementation: 2027-2028.

### Real-Time Fraud Detection for Online Orders

**Current State**: Online order fraud detection relies on basic rules (order value thresholds, shipping/billing address mismatch, velocity checks). Manual review team processes flagged orders with a 4-hour SLA, delaying legitimate orders.

**Proposed Improvement**: Implement a machine learning-based fraud detection system that evaluates each transaction in real time across multiple signals (device fingerprint, IP geolocation, behavioral biometrics, purchase history, third-party fraud data). Legitimate orders are approved instantly; suspicious orders are flagged for manual review with enriched data.

**Projected Impact**: Reduce fraud losses by **60%** (from $1.2M to $480K annually), reduce manual review volume by **70%**, and improve order approval speed for legitimate customers.

**Status**: Vendor shortlist finalized. Pilot planned for Q2 2026 on e-commerce channel.

---

*End of Document BRHI-BP-001 v1.0 — Order-to-Cash Business Process Documentation*
*BuildRight Home Improvement, Inc. — Effective April 1, 2026*
*Classification: Internal — Do Not Distribute Externally*
