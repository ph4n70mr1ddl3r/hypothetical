# Store Opening and Closing Business Process

**BuildRight Home Improvement, Inc. (BRHI)**

---

## 1. Document Control

| Field | Detail |
|---|---|
| **Document ID** | BRHI-BP-004 |
| **Version** | 2.5 |
| **Effective Date** | January 1, 2026 |
| **Last Revised** | December 2, 2025 |
| **Process Owner** | Senior Vice President, Store Operations |
| **Approved By** | David Kowalski, EVP Retail Operations |
| **Review Cycle** | Annual (next review: December 2026) |
| **Classification** | Internal — Store Management and Associates |
| **Supersedes** | BRHI-BP-004 v2.4 (June 2025) |

### Revision History

| Version | Date | Author | Description |
|---|---|---|---|
| 1.0 | 2018-09-01 | P. Johannsen | Initial release |
| 1.1 | 2019-03-15 | P. Johannsen | Added shift change procedures |
| 2.0 | 2020-06-01 | L. Franklin | Overhaul: added T-minus timeline structure, emergency variations |
| 2.1 | 2021-11-10 | L. Franklin | Updated cash till amounts; added card payment verification |
| 2.2 | 2023-02-20 | K. Yamamoto | Added holiday and special event procedures |
| 2.3 | 2024-05-15 | K. Yamamoto | Revised morning huddle format; added safety moment requirement |
| 2.4 | 2025-06-01 | K. Yamamoto | Updated emergency power outage procedures; added generator protocol |
| 2.5 | 2025-12-02 | K. Yamamoto | Updated signage procedures; refined T-minus timeline checkpoints |

---

## 2. Process Overview

### 2.1 Purpose

This document establishes the standardized procedures for opening and closing all 187 BRHI retail locations. Consistent opening and closing practices ensure customer readiness, associate safety, cash security, operational efficiency, and accurate daily financial reporting across the BRHI store network.

### 2.2 Scope

This process applies to:

- All BRHI retail store locations (standard, Pro-focused, and compact formats)
- All scheduled operating days including weekends and holidays
- Shift changes involving the Manager on Duty (MOD) transition
- Emergency and weather-related variations to standard procedures

This process does **not** cover:

- Distribution center operations (see BRHI-BP-008)
- Online fulfillment center operations (see BRHI-BP-009)
- Pop-up or temporary event locations (see BRHI-BP-015)

### 2.3 Oracle Fusion Cloud ERP Integration for Store Opening/Closing

**Oracle Modules Used in Opening/Closing Processes:**

| Oracle Module | Opening/Closing Function | System Touchpoint |
|---|---|---|
| **Oracle HCM Cloud** | Time and attendance clock-in/out | Store tablet / Oracle Mobile App |
| **Oracle Financials Cloud** | Daily sales reconciliation, cash drawer counts | POS integration |
| **Oracle SCM Cloud** | Inventory count verification, receiving status | WMS integration |
| **Oracle Analytics Cloud** | Daily performance dashboard review | Store manager portal |

**Opening System Checks:**

1. **Oracle HCM Cloud Time Clock:**
   - All associates clock in via Oracle HCM Cloud self-service
   - Store Manager verifies all scheduled associates have clocked in
   - Overtime alerts triggered automatically for associates approaching 40 hours

2. **Oracle Financials Cloud Daily Report:**
   - Store Manager reviews prior day's sales report from Oracle Analytics Cloud
   - Cash drawer count reconciles with Oracle Financials Cloud expected totals
   - Any variances flagged for investigation

3. **Oracle SCM Cloud Inventory Status:**
   - Overnight inventory adjustments from Oracle SCM Cloud reviewed
   - Receiving schedule from Oracle Procurement Cloud checked
   - Any system alerts or exceptions addressed before opening

**Closing System Procedures:**

1. **Oracle HCM Cloud Time Clock:**
   - All associates clock out via Oracle HCM Cloud self-service
   - Manager verifies all associates have clocked out
   - Daily labor hours recorded in Oracle HCM Cloud for payroll

2. **Oracle Financials Cloud Daily Close:**
   - Daily sales totals submitted from POS to Oracle Financials Cloud
   - Cash drawer reconciliation completed and posted
   - Exception reports generated for any discrepancies

3. **Oracle SCM Cloud Inventory Close:**
   - Daily inventory movements recorded
   - Any inventory adjustments approved and posted
   - Receiving dock status updated for next day

### 2.4 Standard Operating Hours

| Day | Opening Time | Closing Time | Total Hours |
|---|---|---|---|
| Monday – Saturday | 6:00 AM | 9:00 PM | 15 |
| Sunday | 8:00 AM | 8:00 PM | 12 |
| Thanksgiving Day | CLOSED | CLOSED | 0 |
| Christmas Day | CLOSED | CLOSED | 0 |
| New Year's Day | 9:00 AM | 6:00 PM | 9 |
| July 4th | 8:00 AM | 6:00 PM | 10 |
| All other federal holidays | Standard hours apply | Standard hours apply | Standard |

> **Note:** "T-0" (T-minus zero) refers to the scheduled store opening time. "T+0" refers to the scheduled store closing time. All times in this document are expressed relative to T-0 or T+0 unless otherwise stated.

### 2.4 Key Roles

| Abbreviation | Role | Responsibility |
|---|---|---|
| **MOD** | Manager on Duty | Overall store operations during shift; opens or closes store |
| **SM** | Store Manager | Accountable for store performance; serves as MOD or designates ASM |
| **ASM** | Assistant Store Manager | Serves as MOD in SM absence; oversees departments |
| **SS** | Shift Supervisor | Supervises front-end, receiving, or departments during shift |
| **COA** | Cash Office Associate | Manages safe, register tills, and daily cash handling |
| **DA** | Department Associate | Maintains assigned department readiness and recovery |
| **GA** | Greeter Associate | Stationed at entrance during operating hours |
| **RA** | Receiving Associate | Manages inbound freight and backroom organization |
| **LA** | Lot Associate | Manages cart retrieval, lot cleanliness, and exterior areas |

---

## 3. Opening Process

**Standard Timeline (Monday–Saturday):** T-0 = 6:00 AM. All T-minus times are approximate and represent the latest acceptable completion time for the associated tasks. Associates should aim to complete tasks ahead of the stated deadline.

**Sunday Timeline:** T-0 = 8:00 AM. All T-minus times shift accordingly (e.g., T-90 = 6:30 AM).

### Phase 1: Pre-Opening Facility Preparation (T-90 to T-60)

#### T-90 (4:30 AM Mon–Sat / 6:30 AM Sun): MOD Arrival and Facility Unlock

| Step | Action | Role | Details |
|---|---|---|---|
| 3.1.1 | MOD arrives at the store. Uses personal key to unlock the employee entrance door (rear of building, adjacent to Receiving). | MOD | MOD must arrive no later than T-90. If MOD cannot arrive, they must notify the SM by T-120 (90 minutes before opening) so an alternate MOD can be assigned. |
| 3.1.2 | MOD disarms the security alarm system using the MOD-specific code. System requires: store number + MOD employee ID + personal PIN. Alarm panel is located in the Cash Office. | MOD | If the alarm was triggered overnight, MOD must NOT enter the store. MOD calls the Security Monitoring Center (1-800-555-0123) and local police (911 if active intrusion indicated). MOD waits in their vehicle until cleared by police and Security. |
| 3.1.3 | MOD performs a **Facility Safety Walkthrough** of the entire store, following the standard walkthrough route: Receiving → Backroom → Stockroom → Aisles 1–30 (sequentially) → Garden Center → Breakroom → Restrooms → Front End → Parking Lot (exterior check). | MOD | Estimated duration: 20 minutes. |
| 3.1.4 | During walkthrough, MOD checks and documents the following on the Morning Facility Checklist (Form BRHI-FC-001): **Lighting** — all sales floor lights on and functioning; note any burnt-out fixtures on the maintenance ticket log; **HVAC** — system running; verify thermostat set to 68°F (winter) or 72°F (summer); check for unusual odors or noises from HVAC units; **Floor conditions** — no wet spots, spills, tripping hazards, or damaged tiles; if hazards found, place wet floor signs and initiate cleanup; **Overhead doors** — all bay doors in Receiving closed and latched; **Water** — check for leaks in restrooms, breakroom, and Garden Center; **Fire safety** — verify all fire exits unobstructed, fire extinguishers in place (spot-check 3), emergency lighting units illuminated. | MOD | Any safety hazards that cannot be resolved before T-60 must be reported to the SM and documented. Critical hazards (e.g., water leak, electrical issue) require Facilities Maintenance call (ext. 8000 or 1-800-555-0145) before the store can open. |
| 3.1.5 | MOD turns on sales floor lighting zones in the following order: Zone 1 (Front End / Registers), Zone 2 (Main Aisles), Zone 3 (Perimeter Departments: Plumbing, Electrical, Lumber), Zone 4 (Garden Center, if applicable), Zone 5 (Showroom: Appliances, Kitchen/Bath). | MOD | Lighting control panel is in the Electrical Room (off the main hallway near Receiving). |

#### T-75 (4:45 AM Mon–Sat / 6:45 AM Sun): Cash Office Activation

| Step | Action | Role | Details |
|---|---|---|---|
| 3.2.1 | COA arrives at the store. MOD admits COA through the employee entrance. | COA / MOD | COA standard arrival: T-75. |
| 3.2.2 | COA unlocks the Cash Office (dual-key system: COA key + MOD key, turned simultaneously). COA and MOD must both be present for Cash Office access during non-operating hours. | COA + MOD | Dual-key requirement is a cash security control. Neither key is functional alone. |
| 3.2.3 | COA performs the **Morning Safe Count**: counts all cash in the safe and verifies it matches the Closing Safe Count from the previous night (recorded on Form BRHI-FC-002, Safe Count Reconciliation). Safe count includes: working cash fund ($5,000), previous night's deposit bag (if not yet picked up by armored car), and any excess cash from prior day. | COA | If safe count does not match, COA immediately notifies the MOD. Discrepancies over $25.00 are reported to the SM and Regional Cash Office Manager. Do NOT proceed with till preparation until the discrepancy is resolved. |
| 3.2.4 | COA prepares **register tills** for the day. Standard till composition per register: | COA | |

**Standard Till Composition ($200.00)**

| Denomination | Quantity | Value |
|---|---|---|
| $20 bills | 5 | $100.00 |
| $10 bills | 4 | $40.00 |
| $5 bills | 10 | $50.00 |
| $1 bills | 5 | $5.00 |
| Quarters | 1 roll ($10) | $10.00 |
| Dimes | 1 roll ($5) | $5.00 |
| Nickels | 0 | $0.00 |
| Pennies | 0 | $0.00 |
| **Total** | | **$210.00** |

> **Note:** Tills are prepared at $210.00. The additional $10.00 provides a small buffer for early-morning cash transactions. Tills over $200.00 at the end of the day are considered overages.

| Step | Action | Role | Details |
|---|---|---|---|
| 3.2.5 | COA prepares the **Coin Order** for the day based on the prior day's coin usage: standard coin allocation is 2 rolls of quarters, 1 roll of dimes, and 1 roll of nickels per register. Additional coin is ordered from the bank on Tuesdays and Fridays. | COA | Coin inventory is maintained in the safe. If coin reserves are below 20 rolls of quarters across all registers, COA requests an emergency coin order from the armored car service. |
| 3.2.6 | COA places prepared tills in the locked till cart. Till cart remains in the Cash Office until register opening at T-30. | COA | Each till is labeled with the register number. Register assignments for the day are posted on the Cash Office whiteboard by the MOD by T-45. |

#### T-60 (5:00 AM Mon–Sat / 7:00 AM Sun): Receiving and Backroom Readiness

| Step | Action | Role | Details |
|---|---|---|---|
| 3.3.1 | RA arrives at the store. MOD admits RA through the Receiving entrance. | RA / MOD | RA standard arrival: T-60. |
| 3.3.2 | RA verifies the Receiving dock is clear and accessible for morning deliveries. Standard morning delivery window: 5:30 AM – 8:00 AM. RA confirms the expected delivery schedule by checking the DC shipment schedule on the handheld RF device (login with employee ID). | RA | If morning deliveries are delayed or canceled, RA reports to the MOD by T-30 so the sales floor can be adjusted accordingly (e.g., fill endcaps with existing stock rather than waiting for new product). |
| 3.3.3 | RA performs a **Backroom Organization Check**: walk all backroom aisles (A through F); verify that merchandise is stored on the correct shelves per the backroom slot map; confirm that no merchandise is blocking egress paths, fire exits, or electrical panels; check that all pallets are wrapped and stacked safely (no leaning or overstacked pallets); verify the Damaged Goods and RTV staging areas are organized and not overflowing. | RA | Any backroom safety issues are resolved immediately. Merchandise blocking egress paths is the #1 priority. |
| 3.3.4 | RA prepares the **Unloading Staging Area**: clear the receiving conveyor, stage pallet jacks and forklift (check charge level — minimum 60% for electric equipment), and position the receiving desk for check-in paperwork. | RA | Forklift operators must have a valid BRHI forklift certification card on file. Forklift is not to be operated without certification. |
| 3.3.5 | RA verifies the **compactor/baler** is empty or has capacity for the day's expected cardboard volume. If the baler is >80% full, RA alerts the MOD to schedule an extra cardboard pickup. | RA | Baler operation requires training. Only trained associates may operate the baler. |

### Phase 2: Sales Floor Readiness (T-45 to T-20)

#### T-45 (5:15 AM Mon–Sat / 7:15 AM Sun): Department Walkthrough

| Step | Action | Role | Details |
|---|---|---|---|
| 3.4.1 | DAs arrive at the store for their scheduled shifts. MOD or SS admits associates through the employee entrance. DAs clock in at the time clock and proceed to their assigned departments. | DA / MOD | DA standard arrival: T-45. |
| 3.4.2 | Each DA performs a **Department Readiness Walk** of their assigned area, completing the Department Readiness Checklist (Form BRHI-FC-003). Checklist items: | DA | |

**Department Readiness Checklist (Form BRHI-FC-003) — Key Items:**

1. Aisles are clear of obstructions (no merchandise, pallets, ladders, or equipment in the customer path)
2. All products are faced (pulled to the front of the shelf, labels facing outward)
3. Shelf labels are present and accurate for all displayed products (spot-check 10 SKUs)
4. Endcap displays match the current promotional planogram (check Endcap Planogram Book at the Service Desk)
5. Feature tables and promotional stacks are stocked per the weekly ad plan
6. Products are in the correct location per the planogram (no mis-slotted items)
7. Peg hooks are full or stocked to the minimum display quantity (per planogram)
8. Price tags and signage are current (compare to the current weekly ad effective date)
9. Clearance items are properly signed with red clearance tags
10. All display models are operational and clean (tools, appliances, electronics)
11. Safety barriers and warning signs are in place where required (e.g., overhead stock areas)
12. Department trash is empty; no trash visible on the floor
13. Sample/displays are clean and presentable

| Step | Action | Role | Details |
|---|---|---|---|
| 3.4.3 | DA addresses all critical issues (empty endcaps, missing price tags, aisle obstructions) before T-30. Non-critical issues (minor facing, display cleaning) are completed before T-15. | DA | If a DA identifies an out-of-stock on a promoted item, they notify the MOD immediately so a substitution or rain check plan can be prepared. |
| 3.4.4 | DAs restock high-velocity items from the backroom using the morning stock pull list generated by the inventory system (printed by the RA at T-60 or accessed on the handheld RF device). Priority items: items featured in the current weekly ad, items below minimum shelf quantity, and endcap items. | DA | Stock pull lists are prioritized by department: Lumber (first), Seasonal, Plumbing/Electrical, Tools, Paint, Decor, Hardware. |

#### T-30 (5:30 AM Mon–Sat / 7:30 AM Sun): Lot Preparation and Exterior Check

| Step | Action | Role | Details |
|---|---|---|---|
| 3.5.1 | LA arrives at the store. MOD or SS admits LA through the employee entrance. LA clocks in and proceeds to the parking lot with the Lot Preparation Kit (vest, radio, cart pusher key, caution signs, trash bags). | LA / MOD | LA standard arrival: T-30. |
| 3.5.2 | LA performs the **Lot Sweep**: collect all shopping carts from the parking lot and cart corrals. Use the motorized cart pusher (if available) or manually push carts. Return all carts to the front entrance cart bay. Standard cart count: minimum 40 carts staged for customer use. | LA | If cart count is below 40, LA reports to MOD. Additional carts may be stored in the side lot storage area. |
| 3.5.3 | LA organizes cart corrals: ensure all corrals are empty and upright, position corrals evenly across the lot (standard positions: every 3 parking rows), and remove any damaged carts from circulation (tag with "OUT OF SERVICE" tag and place behind the building). | LA | |
| 3.5.4 | LA places **exterior signage**: open "A" frame signs at each parking lot entrance (standard messages: "Store Hours: 6 AM – 9 PM", "Pro Parking →", "Curbside Pickup →"), place seasonal promotional banners on the building front (update per the marketing calendar), and verify the roadside marquee sign displays the current weekly ad promotion. | LA | Signage details are provided in the Weekly Signage Plan distributed by email every Friday for the following week. |
| 3.5.5 | LA performs a **quick lot cleanliness check**: remove any visible litter, check for potholes or damage in the driving lanes (report to MOD for facilities ticket), and verify the handicap-accessible spaces are clear and signed. | LA | |
| 3.5.6 | LA verifies the **exterior lighting** is functioning: parking lot lights, building fascia lights, entrance canopy lights, and illuminated signage. Burnt-out lights are reported to the MOD for a facilities maintenance ticket. | LA | Parking lot lighting is a safety priority. If >25% of lot lights are non-functional, the MOD must notify Facilities Maintenance for same-day repair. |

#### T-20 (5:40 AM Mon–Sat / 7:40 AM Sun): Final Systems Check

| Step | Action | Role | Details |
|---|---|---|---|
| 3.6.1 | MOD performs the **Systems Readiness Check**: | MOD | |
| 3.6.2 | **POS System:** COA distributes tills to registers. MOD powers on each register (or verifies auto-power-on schedule executed). MOD logs in to Register 1 as the MOD and runs a test transaction (scan a test item, then void). All registers must display the green "READY" status indicator. | MOD / COA | Standard register count: 8 front-end registers + 2 Pro Desk registers + 1 Garden Center register + 1 Returns/Service Desk register = 12 total. Compact format stores may have fewer registers. |
| 3.6.3 | **Phone System:** MOD verifies the store phone system is operational by placing a test call from a back office phone to the main store number. MOD confirms the auto-attendant greeting is active and the call routes to the correct department extension. Overnight forwarding from the corporate answering service should have been deactivated automatically at T-30. | MOD | If phone forwarding is still active, MOD calls the IT Help Desk (ext. 9000) to manually deactivate. |
| 3.6.4 | **Music and Paging System:** MOD turns on the overhead music system (control panel in the Cash Office, set to the BRHI-approved playlist — channel 3 "Home Improvement Morning" or channel 5 "Weekend Energy" for Saturdays/Sundays). MOD makes a test page: "Attention BRHI associates, this is a test of the paging system. All clear." | MOD | Volume should be set to level 4 (background — audible but not intrusive). Adjust up to level 5 on busy weekends. |
| 3.6.5 | **Self-Checkout Stations:** MOD verifies all self-checkout kiosks are powered on, touchscreens are responsive, barcode scanners are functioning (scan a test item), and the self-checkout attendant station is logged in. | MOD / SS | Self-checkout stations are activated at T-0 (doors open), not before. |
| 3.6.6 | **Security Cameras:** MOD opens the Loss Prevention monitoring application on the back-office PC and verifies all camera feeds are active (standard camera count: 64 per store). MOD spot-checks 5 cameras for clear image quality. | MOD | Any camera outages are reported to IT Help Desk (ext. 9000) and the LP Manager. |
| 3.6.7 | **Wi-Fi and Customer Wi-Fi:** MOD verifies the store's internal Wi-Fi (used by handheld RF devices and POS mobile units) is operational by testing on a handheld device. Customer Wi-Fi access point status is checked in the network dashboard. | MOD | Customer Wi-Fi is a courtesy service. Outages are non-blocking for store opening but should be reported to IT. |
| 3.6.8 | **Curbside Pickup System:** If the store offers curbside pickup, MOD verifies the curbside notification system (iPad at the curbside station) is online and the curbside parking spaces are clear. | MOD | |

### Phase 3: Team Readiness and Store Opening (T-15 to T-0)

#### T-15 (5:45 AM Mon–Sat / 7:45 AM Sun): All Associates on Floor and Daily Huddle

| Step | Action | Role | Details |
|---|---|---|---|
| 3.7.1 | All scheduled associates must be clocked in and on the sales floor by T-15. Late arrivals are recorded per the Attendance Policy (BRHI-HR-006). | All Associates | |
| 3.7.2 | MOD conducts the **Daily Huddle** (also known as "Morning Stand-Up") at the front of the store near the Service Desk. All floor associates, cashiers, and the COA attend. Huddle duration: 5–7 minutes. Associates stand (no seating). | MOD | |
| 3.7.3 | **Huddle Agenda:** (1) **Safety Moment** (1 minute): MOD shares a brief safety reminder. Topics rotate weekly and are provided by the Corporate Safety team (e.g., proper lifting technique, forklift awareness, ladder safety, slip/trip prevention, heat/cold weather precautions). (2) **Sales Goals Update** (1 minute): MOD shares the previous day's sales total, current week-to-date performance vs. plan, and today's sales target. Example: "Yesterday we did $87,400 against a plan of $82,000. We're at 102% for the week. Today's target is $85,000 — let's keep the momentum." (3) **Promotions and Focus Items** (2 minutes): MOD highlights the current weekly ad's top 5 promotional items, any one-day or flash sales, and any items that are new or require associate education. (4) **Operational Updates** (1 minute): MOD shares relevant operational info: expected deliveries, system outages, department transfers, visiting corporate personnel, or scheduled maintenance. (5) **Recognition** (1 minute): MOD recognizes an associate for outstanding performance from the prior day or week (Customer shout-out, sales achievement, safety milestone, or team contribution). | MOD | Huddle talking points are prepared by the MOD using the Daily Huddle Template (distributed by email from the Store Operations team every evening for the following day). |
| 3.7.4 | Following the huddle, associates proceed to their assigned stations. **Station Assignments:** Cashiers to registers (register assignments per the Cash Office whiteboard), DAs to departments, GA to the front entrance, LA to the lot, RA to Receiving, SS to the front-end or assigned zone. | All Associates | |

#### T-5 (5:55 AM Mon–Sat / 7:55 AM Sun): Final Pre-Open Check

| Step | Action | Role | Details |
|---|---|---|---|
| 3.8.1 | MOD performs a **Final Pre-Open Walk**: quick walk through the front of the store to verify that all aisles are clear, associates are at their stations, registers are ready, and the entrance is clean and welcoming. | MOD | |
| 3.8.2 | MOD confirms the GA is positioned at the front entrance with: a vest, a radio, a stack of weekly ad flyers, and a sanitized cart wipe station (sanitizer wipes replenished). | MOD | |
| 3.8.3 | MOD unlocks the front entrance doors using the overhead door control key. Doors remain locked but are "armed" (will unlock automatically at T-0 or can be manually unlocked by the MOD at T-0). | MOD | Automatic door unlock is controlled by the POS system clock. MOD should verify the auto-unlock is set; if the system is down, MOD manually unlocks at T-0. |

#### T-0 (6:00 AM Mon–Sat / 8:00 AM Sun): Doors Open

| Step | Action | Role | Details |
|---|---|---|---|
| 3.9.1 | Front entrance doors unlock automatically. GA greets the first customers: "Good morning, welcome to BuildRight! Here's a copy of today's ad." GA offers a cart wipe and a shopping cart. | GA | The GA is the first BRHI associate every customer sees. First impression is critical. Greeting must be warm and genuine, not robotic. |
| 3.9.2 | MOD monitors the entrance area for the first 15 minutes (T-0 to T+15 relative to opening) to handle any immediate customer needs, answer questions, and ensure a smooth start. | MOD | |
| 3.9.3 | Cashiers are logged in and ready at their assigned registers. Self-checkout stations are activated. | Cashiers / SS | |
| 3.9.4 | MOD logs the store opening time in the Daily Operations Log (Form BRHI-FC-004). If the store opened late (more than 5 minutes after scheduled T-0), MOD records the reason (e.g., system issue, staffing delay, safety hazard) and notifies the SM and Regional Operations Manager by email. | MOD | Stores that open late more than twice in a rolling 30-day period are flagged for Regional review. |

---

## 4. Closing Process

**Standard Timeline (Monday–Saturday):** T+0 = 9:00 PM (closing time). All T-plus times are measured from the scheduled closing time. Sunday T+0 = 8:00 PM.

### Phase 4: Pre-Closing (T-30 to T-0)

#### T-30 (8:30 PM Mon–Sat / 7:30 PM Sun): Last Call and Front-End Recovery

| Step | Action | Role | Details |
|---|---|---|---|
| 4.1.1 | MOD makes the **Last Call Announcement** over the PA system: "Attention BuildRight customers, our store will be closing in 30 minutes. Please bring your final selections to the front registers. Thank you for shopping at BuildRight, and have a great evening." | MOD | Repeat the announcement at T-15. |
| 4.1.2 | DAs begin **front-end recovery** (also called "zoning" or "facing"): starting from the front of the store and working toward the back, DAs face all products to the front of the shelf, pick up misplaced items and return them to their correct locations, remove trash and debris from the aisles, and straighten promotional displays and endcaps. Priority: aisles 1–10 (front of store, highest customer traffic) completed before T-0. | DA | Recovery is an ongoing process throughout the day but intensifies during the last 30 minutes. Associates should NOT abandon recovery when customers are present in their area — customer service always takes priority. |
| 4.1.3 | RA verifies that all inbound freight for the day has been processed and put away. Any remaining freight on the receiving dock is staged for the next morning's stock pull. | RA | |
| 4.1.4 | LA performs a **final lot sweep**: collect all shopping carts from the lot and corrals, returning them to the front entrance cart bay. LA remains on the lot to assist any remaining customers with loading purchases into their vehicles. | LA | |

#### T-15 (8:45 PM Mon–Sat / 7:45 PM Sun): Entrance Closure and Customer Count

| Step | Action | Role | Details |
|---|---|---|---|
| 4.2.1 | MOD makes the **Second Closing Announcement**: "Attention BuildRight customers, our store will be closing in 15 minutes. Please proceed to the front registers with your selections. Thank you for shopping at BuildRight." | MOD | |
| 4.2.2 | GA closes and locks the **secondary entrance door** (if the store has dual entrances; the main entrance remains open but one-way traffic is enforced — customers exit only through the secondary door, customers may still enter through the main entrance). | GA / MOD | |
| 4.2.3 | GA performs a **Customer Count**: GA (or designated associate) walks the entire store and counts the number of customers still shopping. GA reports the count to the MOD via radio. Standard expectation: fewer than 15 customers at T-15. If more than 25 customers remain, MOD may consider a 15-minute extension (requires SM approval if SM is not on-site). | GA | |
| 4.2.4 | DAs continue recovery in their departments. DAs stationed near the back of the store gently inform customers in their area: "Just to let you know, we'll be closing in about 15 minutes. Can I help you find anything?" | DA | |
| 4.2.5 | SS begins **front-end wind-down**: reduces open registers to 2 (Register 1 and Register 2) plus the Self-Checkout stations. Remaining cashiers are reassigned to recovery or released for the evening if their shift has ended. | SS | |

#### T-0 (9:00 PM Mon–Sat / 8:00 PM Sun): Doors Locked and Final Customer Processing

| Step | Action | Role | Details |
|---|---|---|---|
| 4.3.1 | MOD makes the **Final Closing Announcement**: "Attention BuildRight customers, BuildRight is now closed. Please bring your items to the front registers for checkout. Thank you for shopping with us today." | MOD | |
| 4.3.2 | GA locks the **main entrance doors** (using the overhead door control key). Entrance doors are locked in the "exit only" position — customers inside can exit, but no new customers can enter. | GA / MOD | |
| 4.3.3 | MOD performs a **Final Store Walk**: MOD walks the entire sales floor, starting from the back of the store (Aisle 30) and moving toward the front. MOD's objectives: ensure no customers remain in the store (all aisles, restrooms, Garden Center, breakroom, and fitting rooms checked); identify any safety issues that need immediate attention; verify that all department associates have begun recovery. MOD carries a radio and communicates customer count to the front end as they walk. | MOD | Under NO circumstances should the MOD assume the store is empty without physically walking it. This is a safety and security requirement. |
| 4.3.4 | MOD checks the **Restrooms**: knock on each restroom door, announce "BuildRight closing," open and verify no one is inside. Lock restroom doors from the outside. | MOD | |
| 4.3.5 | Remaining customers are directed to the open registers. MOD ensures all customers are checked out promptly and courteously. No customer should feel rushed at the register — the urgency was in the announcements, not the checkout experience. | MOD / Cashier | |

### Phase 5: Post-Closing Operations (T+15 to T+60)

#### T+15 (9:15 PM Mon–Sat / 8:15 PM Sun): Register Close and Cash Handling

| Step | Action | Role | Details |
|---|---|---|---|
| 4.4.1 | MOD confirms all customers have exited the building. MOD authorizes register close procedure. | MOD | |
| 4.4.2 | Cashiers perform the **Register Close** on each open register: select "Close Register" in POS, POS displays the electronic till count, cashier counts the physical cash in the till and enters the count, POS compares physical count to the electronic count and displays any variance, cashier prints the register close report. | Cashier | Variances over $5.00 require MOD sign-off on the variance report. Variances over $25.00 require a written explanation and are reported to the SM. |
| 4.4.3 | Cashier places the till contents in a tamper-evident deposit bag (pre-printed with register number, date, and associate ID). Cashier seals the bag, signs the seal, and writes the total on the outside. | Cashier | |
| 4.4.4 | COA (or designated SS if COA has left for the day) collects all deposit bags from the registers and the cash from the self-checkout stations. COA and MOD both sign the Till Pick-Up Log (Form BRHI-FC-005). | COA / MOD | |
| 4.4.5 | COA transports deposit bags to the Cash Office. COA counts each till in the Cash Office and reconciles against the register close report. Total store cash is reconciled. COA prepares the **Daily Deposit**: total cash sales less the $5,000 working cash fund less the next day's till requirements. The deposit is placed in a secure deposit bag, sealed, and placed in the safe for armored car pickup. | COA | Armored car pickup schedule: Monday through Saturday at approximately 10:00 PM (varies by location). Sunday deposits are held in the safe for Monday pickup. |
| 4.4.6 | COA prepares tills for the next morning (if the next day's till preparation was not already done during the morning shift). Tills are placed in the locked till cart in the Cash Office. | COA | |
| 4.4.7 | COA performs the **Closing Safe Count**: counts all cash remaining in the safe and records it on the Safe Count Reconciliation form (Form BRHI-FC-002). The closing safe count must equal the $5,000 working cash fund plus any held deposits. | COA | Closing safe count is the opening safe count for the next morning. Any discrepancy must be resolved before the COA leaves. |
| 4.4.8 | COA locks the Cash Office. MOD verifies the Cash Office door is locked and the deadbolt is engaged. | COA / MOD | |

#### T+30 (9:30 PM Mon–Sat / 8:30 PM Sun): Department Recovery Completion

| Step | Action | Role | Details |
|---|---|---|---|
| 4.5.1 | DAs complete **department recovery**: all products faced, overstock removed from the top of shelves (either placed in the backroom or consolidated), misplaced items returned to their home locations, peg hooks straightened and restocked to minimum display quantity, trash emptied, and department floors swept (or spot-swept as needed). | DA | Recovery standard: a customer walking the department tomorrow morning should see a clean, fully stocked, and organized department indistinguishable from a "grand opening" presentation. |
| 4.5.2 | DAs report recovery completion to the SS or MOD via radio. MOD or SS spot-checks 3 departments for recovery quality. | DA / SS / MOD | Spot-check items: facing accuracy (product pulled to the front), shelf label accuracy (3 random SKUs checked), and no misplaced items. Departments that fail the spot-check are re-covered by the DA before clock-out. |
| 4.5.3 | RA completes the **Receiving Close**: all inbound freight for the day is processed and put away; receiving dock door is closed and locked; backroom is organized; Damaged Goods and RTV areas are tidy; compactor/baler is loaded and cycled (if >60% full); forklift and powered equipment are plugged in for charging. | RA | Forklift charging stations are in the backroom. Equipment must be charging by T+30 to ensure full charge for the next morning. |
| 4.5.4 | LA completes the **Lot Close**: all shopping carts collected from the lot and stored in the cart bay or side storage area; cart corrals inspected for damage; lot checked for litter (quick sweep); exterior signage collected and stored inside the entrance vestibule. | LA | |
| 4.5.5 | DAs, RA, and LA clock out. SS verifies all hourly associates have clocked out by T+40. Any associate still on the floor after T+40 must be authorized by the MOD for overtime. | DA / RA / LA / SS | |

#### T+45 (9:45 PM Mon–Sat / 8:45 PM Sun): Final Walkthrough

| Step | Action | Role | Details |
|---|---|---|---|
| 4.6.1 | MOD performs the **Final Closing Walkthrough** of the entire store, following the same route as the morning walkthrough (Receiving → Backroom → Stockroom → Aisles 1–30 → Garden Center → Breakroom → Restrooms → Front End → Parking Lot). | MOD | Estimated duration: 15 minutes. |
| 4.6.2 | MOD checks and documents the following on the Closing Facility Checklist (Form BRHI-FC-006): | MOD | |

**Closing Facility Checklist (Form BRHI-FC-006) — Key Items:**

1. All customers and non-management associates have exited the building
2. All department lights are off (except security lighting — Zone 6, always on)
3. All equipment is powered off or charging: forklifts (charging), pallet jacks (charging), floor scrubber (charging), pipe-cutting machine (off), key-cutting machine (off), screen-printing machine (off), paint shaker (off), radial arm saw (off, blade guard in place)
4. All bay doors in Receiving are closed and locked
5. Restrooms are empty and locked; faucets are off; no running water
6. Breakroom is clean: tables wiped, trash emptied, refrigerator checked for expired items (dispose), coffee maker off
7. All propane cage and lumber rack locks are engaged
8. Garden Center gate is closed and locked (if applicable)
9. HVAC set to unoccupied mode (thermostat setback: 60°F winter / 80°F summer)
10. All fire exits are unobstructed
11. Cash Office is locked (double-verified)
12. All registers are powered off (except Register 1, left on for nightly POS update batch)
13. Self-checkout stations are powered off
14. Back office computers are logged off (not powered down — they receive nightly updates)
15. Phone system is set to overnight forwarding (automatic at T+30; verify manually if auto-forward failed)
16. Music / paging system is off
17. Safe is locked and the MOD has verified the deposit bag is inside
18. All exterior doors are locked: employee entrance, Receiving entrance, Fire exits (remain latched but not locked from inside — fire code), and front entrance doors (both)
19. No unauthorized persons remain in the building
20. Parking lot is empty of customers (or any remaining vehicles are noted and reported to Security Monitoring)

| Step | Action | Role | Details |
|---|---|---|---|
| 4.6.3 | MOD checks the **Daily Operations Log** (Form BRHI-FC-004) for completeness. Log must include: store opening time, MOD name(s) for the day, sales totals (from POS end-of-day report), customer count, any incidents (safety, customer complaints, security), any maintenance issues reported, any staffing shortages or call-outs for the next day, and the closing safe count. | MOD | |
| 4.6.4 | MOD completes any pending paperwork: filing of the day's return receipts, signing off on the daily return report, and reviewing/approving any timeclock adjustments. | MOD | |

#### T+60 (10:00 PM Mon–Sat / 9:00 PM Sun): Alarm Set and Building Exit

| Step | Action | Role | Details |
|---|---|---|---|
| 4.7.1 | MOD proceeds to the Alarm Panel in the Cash Office. MOD arms the security alarm system: store number + MOD employee ID + personal PIN + "AWAY" mode (all motion sensors and door contacts active). | MOD | The alarm allows a 60-second exit delay. MOD must exit the building within 60 seconds of arming. |
| 4.7.2 | MOD exits through the Employee Entrance. MOD pulls the door shut and verifies it is locked by pushing the door handle (door should not open from the outside). | MOD | |
| 4.7.3 | MOD performs a **final exterior check**: walk the perimeter of the building, verify all exterior doors are closed and locked, check that no vehicles remain in the employee parking area (other than the MOD's own vehicle), and verify the parking lot lights are on (timer-controlled, should activate at dusk). | MOD | |
| 4.7.4 | MOD drives past the front entrance to verify the front doors are locked and the entrance area is clear. MOD departs. | MOD | |
| 4.7.5 | MOD emails the **Daily Close Confirmation** to the SM and Regional Operations Manager: "Store [###] closed on schedule at [time]. Safe count reconciled. No issues / [note any issues]. MOD: [name]." | MOD | Email must be sent within 30 minutes of leaving the store (by T+90 at the latest). |

---

## 5. Shift Change Process

### 5.1 MOD Handoff Overview

Shift changes involving the MOD occur at standard times: **2:00 PM** (Morning MOD to Afternoon MOD) and **10:00 PM** (Afternoon MOD to Closing MOD, if applicable; in most stores, the Afternoon MOD also serves as the Closing MOD).

### 5.2 MOD Handoff Checklist

The outgoing MOD and incoming MOD conduct a **face-to-face handoff** at the Service Desk or MOD station. Handoff duration: 10–15 minutes. Both MODs walk the front of the store together during the handoff.

**MOD Handoff Checklist (Form BRHI-FC-007):**

| # | Item | Details |
|---|---|---|
| 1 | Sales Performance | Current day's sales vs. plan (POS dashboard). Any departments significantly over or under plan. |
| 2 | Customer Count | Current day's customer count vs. plan. Foot traffic trends. |
| 3 | Staffing Status | Current associate headcount vs. schedule. Any call-outs or early releases. Upcoming shift changes. Any associates needing coaching or recognition. |
| 4 | Open Incidents | Any active customer complaints, safety incidents, or security concerns. Status of any open incidents from the morning shift. |
| 5 | Deliveries and Freight | Status of today's inbound deliveries. Any remaining freight to be processed. Expected afternoon/evening deliveries (e.g., vendor direct deliveries). |
| 6 | Operational Issues | Any equipment out of service (forklift, POS registers, self-checkout, phones, HVAC). Status of any open facilities maintenance tickets. |
| 7 | Promotions and Pricing | Any pricing errors identified. Promotional items that are out of stock. Rain checks issued. |
| 8 | Returns and LP | Notable returns processed (high-value, fraud-flagged, manager overrides). Any active LP concerns. |
| 9 | Cash Office Status | Safe count status. Any cash variances. Next armored car pickup time. |
| 10 | Communications | Messages from Regional or Corporate. Any tasks or directives from the SM. |
| 11 | Weather / External Factors | Weather forecast affecting operations. Local events impacting traffic. |
| 12 | Keys and Alarm Codes | Transfer of MOD keys (Cash Office key, door control key, forklift key, propane cage key). Incoming MOD confirms their alarm code is active. |

### 5.3 Communication Log

The **MOD Communication Log** is a physical logbook (or digital log on the store tablet) maintained at the MOD station. It is a running record of key events and decisions throughout the day. Entries include:

- Timestamp
- MOD name
- Event description (e.g., "Customer slip-and-fall in Aisle 14 — incident report filed," "Register 5 printer jammed — IT ticket #4567," "High-value return $875 — approved by MOD, fraud check clear")
- Resolution or status
- Follow-up required (yes/no, with details)

The outgoing MOD reviews all open items in the log with the incoming MOD. The incoming MOD signs the log to acknowledge receipt of the handoff.

### 5.4 Open Issues Transfer

Any issue that was not resolved during the outgoing MOD's shift is formally transferred to the incoming MOD. Open issues are documented on the MOD Communication Log with:

- Issue description
- Current status
- Required next steps
- Deadline for resolution (if applicable)
- Person responsible

---

## 6. Checklists

### 6.1 Opening Checklist (Form BRHI-FC-001)

**Store #:** ________  **Date:** ________  **MOD:** ____________________  **Signature:** ____________________

| # | Task | Time (Target) | Responsible | Completed (✓) | Initials |
|---|---|---|---|---|---|
| 1 | MOD arrives at store | T-90 (4:30 AM) | MOD | ___ | ___ |
| 2 | Disarm security alarm | T-90 | MOD | ___ | ___ |
| 3 | Facility safety walkthrough (lights, HVAC, floors, hazards, fire safety) | T-90 to T-75 | MOD | ___ | ___ |
| 4 | Sales floor lighting turned on (Zones 1–5) | T-90 | MOD | ___ | ___ |
| 5 | Cash Office unlocked (dual key) | T-75 (4:45 AM) | MOD + COA | ___ | ___ |
| 6 | Morning safe count performed and reconciled | T-75 | COA | ___ | ___ |
| 7 | Register tills prepared ($210.00 per till) | T-75 to T-60 | COA | ___ | ___ |
| 8 | Coin order prepared for registers | T-75 to T-60 | COA | ___ | ___ |
| 9 | Receiving area cleared and ready for deliveries | T-60 (5:00 AM) | RA | ___ | ___ |
| 10 | Backroom organization check completed | T-60 | RA | ___ | ___ |
| 11 | Unloading staging area prepared (pallet jacks, forklift charged) | T-60 | RA | ___ | ___ |
| 12 | Compactor/baler capacity checked | T-60 | RA | ___ | ___ |
| 13 | Department readiness walkthroughs completed (all departments) | T-45 (5:15 AM) | DA | ___ | ___ |
| 14 | Products faced, endcaps verified, shelf labels checked | T-45 to T-30 | DA | ___ | ___ |
| 15 | Stock pull list executed — high-velocity and ad items restocked | T-45 to T-20 | DA | ___ | ___ |
| 16 | Lot sweep — carts collected (min. 40 at entrance) | T-30 (5:30 AM) | LA | ___ | ___ |
| 17 | Cart corrals organized and positioned | T-30 | LA | ___ | ___ |
| 18 | Exterior signage placed (A-frames, banners, marquee) | T-30 | LA | ___ | ___ |
| 19 | Lot cleanliness and lighting check | T-30 | LA | ___ | ___ |
| 20 | POS system online — test transaction on Register 1 | T-20 (5:40 AM) | MOD | ___ | ___ |
| 21 | Phone system verified — test call completed | T-20 | MOD | ___ | ___ |
| 22 | Music/paging system on — test page completed | T-20 | MOD | ___ | ___ |
| 23 | Self-checkout kiosks powered on and tested | T-20 | MOD / SS | ___ | ___ |
| 24 | Security cameras verified — all feeds active | T-20 | MOD | ___ | ___ |
| 25 | Wi-Fi (internal and customer) verified | T-20 | MOD | ___ | ___ |
| 26 | Curbside pickup system verified (if applicable) | T-20 | MOD | ___ | ___ |
| 27 | Register till distribution to all registers | T-20 | COA | ___ | ___ |
| 28 | All associates clocked in and on sales floor | T-15 (5:45 AM) | All | ___ | ___ |
| 29 | Daily huddle conducted (safety, goals, promos, ops, recognition) | T-15 | MOD | ___ | ___ |
| 30 | Associates at assigned stations | T-10 | All | ___ | ___ |
| 31 | Final pre-open walk completed | T-5 (5:55 AM) | MOD | ___ | ___ |
| 32 | Greeter positioned at entrance with flyers, wipes, carts | T-5 | GA | ___ | ___ |
| 33 | Front entrance doors armed for auto-unlock | T-5 | MOD | ___ | ___ |
| 34 | **DOORS OPEN — store opens on time** | **T-0 (6:00 AM)** | **MOD** | ___ | ___ |
| 35 | Opening time logged in Daily Operations Log | T-0 | MOD | ___ | ___ |

**SM Review Signature:** ____________________  **Date:** ____________

---

### 6.2 Closing Checklist (Form BRHI-FC-006)

**Store #:** ________  **Date:** ________  **MOD:** ____________________  **Signature:** ____________________

| # | Task | Time (Target) | Responsible | Completed (✓) | Initials |
|---|---|---|---|---|---|
| 1 | Last call announcement (30-minute warning) | T-30 (8:30 PM) | MOD | ___ | ___ |
| 2 | Front-end recovery initiated (aisles 1–10 priority) | T-30 | DA | ___ | ___ |
| 3 | Receiving area — all freight processed or staged | T-30 | RA | ___ | ___ |
| 4 | Lot sweep — all carts collected | T-30 | LA | ___ | ___ |
| 5 | Second closing announcement (15-minute warning) | T-15 (8:45 PM) | MOD | ___ | ___ |
| 6 | Secondary entrance door closed and locked | T-15 | GA / MOD | ___ | ___ |
| 7 | Customer count performed — count reported to MOD | T-15 | GA | ___ | ___ |
| 8 | DAs inform remaining customers of closing in their areas | T-15 | DA | ___ | ___ |
| 9 | Front-end reduced to 2 registers + self-checkout | T-15 | SS | ___ | ___ |
| 10 | Final closing announcement | T-0 (9:00 PM) | MOD | ___ | ___ |
| 11 | Main entrance doors locked (exit only) | T-0 | GA / MOD | ___ | ___ |
| 12 | Final store walk — all areas checked, no customers remain | T-0 | MOD | ___ | ___ |
| 13 | Restrooms checked, cleared, and locked | T-0 | MOD | ___ | ___ |
| 14 | All remaining customers checked out | T-0 to T+10 | Cashier / MOD | ___ | ___ |
| 15 | All registers closed — till counts reconciled | T+15 (9:15 PM) | Cashier | ___ | ___ |
| 16 | Tills placed in deposit bags and sealed | T+15 | Cashier | ___ | ___ |
| 17 | Cash pick-up from all registers and self-checkout | T+15 | COA / MOD | ___ | ___ |
| 18 | Daily deposit prepared and placed in safe | T+15 to T+30 | COA | ___ | ___ |
| 19 | Next-day tills prepared (if not done in morning) | T+15 to T+30 | COA | ___ | ___ |
| 20 | Closing safe count performed and recorded | T+30 (9:30 PM) | COA | ___ | ___ |
| 21 | Cash Office locked and verified | T+30 | COA / MOD | ___ | ___ |
| 22 | Department recovery completed — all areas faced and clean | T+30 | DA | ___ | ___ |
| 23 | Department recovery spot-check (3 departments) | T+30 | MOD / SS | ___ | ___ |
| 24 | Receiving close — dock locked, backroom organized, equipment charging | T+30 | RA | ___ | ___ |
| 25 | Lot close — carts stored, signage collected, lot clear | T+30 | LA | ___ | ___ |
| 26 | All hourly associates clocked out (by T+40) | T+30 to T+40 | SS | ___ | ___ |
| 27 | Final closing walkthrough (full store — see Section 4.6.2 for 20 items) | T+45 (9:45 PM) | MOD | ___ | ___ |
| 28 | Sales floor lights off (except Zone 6 security lighting) | T+45 | MOD | ___ | ___ |
| 29 | All equipment off or charging | T+45 | MOD | ___ | ___ |
| 30 | HVAC set to unoccupied mode | T+45 | MOD | ___ | ___ |
| 31 | Phone system verified on overnight forwarding | T+45 | MOD | ___ | ___ |
| 32 | Music/paging system off | T+45 | MOD | ___ | ___ |
| 33 | Daily Operations Log completed and reviewed | T+45 | MOD | ___ | ___ |
| 34 | All paperwork filed (returns, timeclock adjustments, incident reports) | T+45 | MOD | ___ | ___ |
| 35 | **Alarm set — AWAY mode** | **T+60 (10:00 PM)** | **MOD** | ___ | ___ |
| 36 | Building exited — employee entrance locked and verified | T+60 | MOD | ___ | ___ |
| 37 | Exterior perimeter check — all doors locked, lot clear | T+60 | MOD | ___ | ___ |
| 38 | Daily Close Confirmation email sent to SM and Regional Ops | T+60 to T+90 | MOD | ___ | ___ |

**SM Review Signature:** ____________________  **Date:** ____________

---

## 7. Holiday and Special Event Procedures

### 7.1 Extended Hours

| Event | Standard Hours | Modified Hours | Schedule Adjustment |
|---|---|---|---|
| Black Friday (Day after Thanksgiving) | 6 AM – 9 PM | 5 AM – 11 PM | Open: T-90 becomes 3:30 AM. All opening tasks shift 90 minutes earlier. Additional MOD scheduled for the extended shift. |
| Christmas Eve (December 24) | 6 AM – 9 PM | 6 AM – 6 PM | Close: T+0 = 6 PM. Closing tasks begin at 5:30 PM. All closing tasks shift 3 hours earlier. |
| New Year's Eve (December 31) | 6 AM – 9 PM | 6 AM – 6 PM | Close: T+0 = 6 PM. Same as Christmas Eve. |
| Memorial Day / Labor Day Weekends (Saturday–Sunday) | Sat 6–9, Sun 8–8 | Sat 6–10, Sun 7–9 | Open: Sunday T-90 = 5:30 AM. Close: Saturday T+0 = 10 PM. Additional associate scheduled. |
| Spring Sale Event (1st weekend in April) | Standard | Sat 5 AM – 10 PM, Sun 7 AM – 9 PM | Open: Saturday T-90 = 3:30 AM. Additional morning stock team scheduled. |
| Pro Week Event (3rd week in September) | Standard | Mon–Sat 5 AM – 9 PM, Sun 7 AM – 8 PM | Open: Mon–Sat T-90 = 3:30 AM. Pro Desk staffed with 2 additional associates. Early breakfast provided for associates. |

**Extended Hours Protocol:**

- SM must submit the Extended Hours Staffing Plan to the Regional Operations Manager at least 14 days before the event.
- Associate voluntary overtime sign-up sheets are posted 21 days in advance. Mandatory overtime is a last resort and requires SM approval.
- The MOD must provide meal breaks for all associates working extended shifts per the BRHI Meal and Rest Break Policy (BRHI-HR-010).
- Security is enhanced during extended hours: an additional LP associate is scheduled during Black Friday and Spring Sale events.

### 7.2 Early Closures

Early closures may be authorized by the SM or, if the SM is unavailable, by the Regional VP. Triggers for early closure include:

- Severe weather (see Section 8.1)
- Power outage exceeding 2 hours (see Section 8.2)
- Civil emergency or government order
- Building safety issue (e.g., water main break, gas leak)
- Associate safety concern (e.g., parking lot icing, civil unrest in the area)

**Early Closure Procedure:**

1. SM (or MOD) makes the decision and notifies the Regional VP by phone.
2. MOD makes the announcement: "Attention BuildRight customers and associates, due to [reason], our store will be closing at [time]. We apologize for the inconvenience. Please bring your items to the front registers. Associates, please begin closing procedures immediately."
3. Closing procedures (Section 4) are executed on an accelerated timeline. The MOD prioritizes: customer notification and checkout → register close and cash handling → building secure and alarm set.
4. The MOD sends the Early Closure Report to the SM, Regional VP, and VP Customer Care within 2 hours of closure.

### 7.3 Seasonal Setup Timeline

| Season | Setup Start | Setup Complete | Key Changes |
|---|---|---|---|
| Spring / Garden (March) | February 15 | March 1 | Garden Center display installation; outdoor furniture staging; lawn care product expansion; nursery live goods area prepared |
| Summer (May) | May 1 | May 15 | Grilling center setup; pool and patio merchandise; cooling products display; outdoor lighting expansion |
| Back-to-School / Fall (August) | August 1 | August 15 | Organization and storage displays; dorm/apartment essentials; fall seasonal décor; weatherization products |
| Holiday (November) | October 15 | November 1 | Holiday décor; lighting; gift center; tool gift sets; small appliances for gifting; propane and heating expansion |
| Winter (December) | December 1 | December 15 | Snow removal equipment; ice melt display; insulation and weatherstripping; space heaters; generator promotion |

Seasonal setup is a **store-wide effort** involving all DAs, the RA, and the Visual Merchandising team (which provides the seasonal planograms and display instructions). The SM assigns a seasonal setup captain (typically an ASM) who coordinates the transition.

Setup activities are scheduled during the **T-90 to T-0 pre-opening window** and during low-traffic afternoon hours (2:00 PM – 4:00 PM) to minimize disruption to customers. Heavy merchandising (pallet displays, forklift work) is restricted to pre-opening hours only for safety.

---

## 8. Emergency Variations

### 8.1 Weather Events

#### Severe Winter Weather (Snow, Ice, Blizzard)

| Condition | Action | Decision Maker |
|---|---|---|
| Winter Storm Warning issued by NWS for store's county | SM evaluates opening status by 4:00 AM (or 3 hours before opening). Options: open on time, delay opening, or close for the day. | SM (with Regional VP concurrence) |
| Delayed Opening (2-hour delay) | All T-minus times shift by 2 hours. Example: T-90 becomes 8:30 AM instead of 4:30 AM. Store opens at 8:00 AM. Essential tasks only: facility safety check, register prep, and department walkthrough. Non-essential tasks (lot signage, display cleaning) are deferred. | MOD executes |
| Full-Day Closure | SM notifies all associates via the BRHI Associate Hotline (1-800-555-0177) and the scheduling app by 5:00 AM. MOD does NOT report to the store. Regional VP is notified by email. Store is marked "CLOSED" on the BRHI.com store locator and Google Business listing. | SM |
| Early Closure due to deteriorating weather | Follow Early Closure Procedure (Section 7.2). Priority: get associates and customers home safely. MOD authorizes associates to leave as soon as closing tasks are complete — no recovery required. | SM or MOD |

**Snow Removal Protocol:**

- The snow removal contractor (under contract with BRHI Facilities) is responsible for plowing the parking lot and salting walkways. Contractor is auto-dispatched when accumulations reach 2 inches.
- The LA is responsible for shoveling and salting the entrance vestibule, cart bay area, and employee entrance walkway. Salt and shovels are stored in the Receiving janitorial closet.
- If the snow removal contractor has not arrived by T-30, the MOD calls Facilities Maintenance (1-800-555-0145) for a status update.

#### Severe Thunderstorm / Tornado Warning

| Condition | Action | Decision Maker |
|---|---|---|
| Severe Thunderstorm Warning | MOD monitors the weather via the NOAA Weather Radio (located in the Cash Office). MOD makes a PA announcement: "Attention customers and associates, a severe thunderstorm warning is in effect for our area. Please be aware of your surroundings and move away from exterior doors and windows if conditions worsen." | MOD |
| Tornado Warning (store's county) | MOD activates the **Tornado Safety Protocol**: PA announcement: "Attention, a tornado warning has been issued for our area. All customers and associates, please move immediately to the interior of the building, away from windows and exterior walls. Proceed to Aisles 15–20 in the center of the store, or the Receiving area. Do not use the front entrance." MOD directs the GA to lock the entrance doors (to prevent customers from going to their cars). DAs sweep their departments to direct customers to the safe zones. LA comes inside immediately. | MOD |
| Tornado Warning All-Clear | MOD monitors for the official all-clear from NOAA. MOD makes the all-clear PA announcement. MOD performs a facility damage assessment. If damage is found, MOD contacts Facilities Maintenance and the Regional VP. If no damage, resume normal operations. | MOD |

#### Hurricane (Coastal Stores Only)

- Stores in the projected path of a Category 2+ hurricane are preemptively closed 12 hours before expected tropical storm-force winds. The Regional VP issues the closure directive.
- Pre-closure tasks (24 hours before expected closure): secure all outdoor merchandise (Garden Center, lumber, patio furniture) indoors or under cover; sandbag entrances if flooding is a risk; back up all POS and inventory data to the cloud; safe contents are picked up by armored car early.
- Post-storm reopening requires a full facility inspection by Facilities Maintenance before associates re-enter the building.

### 8.2 Power Outage

| Step | Action | Role | Details |
|---|---|---|---|
| 8.2.1 | When power fails, the **emergency generator** auto-starts within 10 seconds. Generator provides power to: security system and cameras, emergency lighting (aisle exit signs and perimeter lighting at 30% illumination), Cash Office (safe lock and alarm), and fire suppression system. Generator does NOT power: POS registers, self-checkout, overhead lighting, HVAC, or the phone system. | System (automated) | Generator fuel capacity: 8 hours at standard load. If outage exceeds 6 hours, MOD calls Facilities to arrange fuel delivery. |
| 8.2.2 | MOD makes a PA announcement (battery-powered backup PA is available): "Attention customers and associates, we are experiencing a power outage. Emergency lighting is on. Please remain calm and stay where you are. We are assessing the situation and will provide an update shortly." | MOD | |
| 8.2.3 | MOD contacts the **power utility** (number posted on the Electrical Room door) to report the outage and get an estimated restoration time. MOD also contacts Facilities Maintenance (1-800-555-0145). | MOD | |
| 8.2.4 | If estimated restoration time is **under 30 minutes**: MOD keeps the store open. Cashiers process transactions using **manual backup procedures**: write paper receipts (pre-printed receipt pads in each register drawer), calculate totals manually, and accept cash only (no credit/debit cards during outage). When power is restored, cashiers enter the manual transactions as "Offline Transactions" in POS. | Cashier / MOD | |
| 8.2.5 | If estimated restoration time is **30 minutes to 2 hours**: MOD may keep the store open at their discretion, based on remaining daylight (if daytime) and customer traffic. If the outage occurs at night, close the store per the Early Closure Procedure. | MOD | |
| 8.2.6 | If estimated restoration time is **over 2 hours** (or unknown): MOD initiates the Early Closure Procedure (Section 7.2). MOD prioritizes: customer notification, manual checkout for remaining customers, register close (manual count of tills), safe deposit, building secure, alarm set. | MOD | |
| 8.2.7 | After power is restored, MOD performs a **systems restart**: POS registers reboot (auto-restart when power returns; verify all are online), phone system reset (may require manual reboot — IT Help Desk ext. 9000), HVAC restart (set to occupied mode), lighting (all zones on), music/paging system on, self-checkout reactivated, and verify all security cameras are back online. | MOD | |
| 8.2.8 | MOD documents the power outage in the Daily Operations Log, including: time of outage, duration, estimated lost sales (compare to a typical day's hourly sales for the same time period), any manual transactions processed, and any equipment damage caused by the outage. | MOD | |

### 8.3 Fire or Smoke Event

| Condition | Action |
|---|---|
| Fire alarm activation | MOD calls 911 immediately, even if a false alarm is suspected. MOD then makes a PA announcement: "Attention, the fire alarm has been activated. All customers and associates, please exit the building immediately through the nearest exit. Do not use elevators. Proceed to the designated assembly point in the parking lot, at least 100 feet from the building." MOD directs the GA to hold exit doors open. DAs sweep their departments for customers and direct them to exits. MOD is the LAST person to exit after verifying all areas are clear (if safe to do so). |
| Visible smoke (no alarm) | MOD calls 911 and activates the fire alarm manually (pull station located at each exit). Follow the same evacuation procedure. |
| Small, contained fire (e.g., trash can) | Only if the fire is small and the associate has been trained, use the nearest fire extinguisher (PASS method: Pull, Aim, Squeeze, Sweep). If the fire is not extinguished within 30 seconds, evacuate. |
| Re-entry after fire event | The fire department must provide an all-clear before anyone re-enters the building. The SM and Facilities Maintenance must assess building safety before the store can reopen. |

### 8.4 Active Threat / Robbery

- BRHI follows the **"Run, Hide, Fight"** protocol for active threat situations, as trained in the annual BRHI Safety and Security module.
- In the event of a robbery: associates are trained to **comply** with all demands. Do not resist. The safety of associates and customers is the absolute priority. Do NOT activate any alarms or attempt to confront the individual(s).
- After the threat has left, MOD calls 911, then calls the BRHI Security Monitoring Center (1-800-555-0123), then notifies the SM and Regional LP Manager.
- The store remains closed until cleared by law enforcement. All associates are offered access to the BRHI Employee Assistance Program (EAP) for counseling.

### 8.5 Gas Leak or Chemical Spill

| Condition | Action |
|---|---|
| Suspected gas leak (natural gas odor) | MOD calls 911 and the gas utility company (number posted on the Electrical Room door). MOD does NOT use light switches, radios, or anything that could create a spark. Evacuate the building immediately using the fire evacuation route. Do not re-enter until the fire department provides an all-clear. |
| Chemical spill (in-store) | If the spill is a known, non-hazardous product: DA cleans per the Safety Data Sheet (SDS) instructions (SDS binder located at the Service Desk and in each department). If the spill is unknown, large, or involves a hazmat product: DA notifies the MOD immediately. MOD evacuates the immediate area, calls 911 if necessary, and contacts Facilities Maintenance. Associates do NOT attempt to clean hazmat spills unless they hold a current HAZWOPER certification. |
| Chemical spill (customer vehicle in lot) | LA notifies the MOD. MOD contacts the local fire department's non-emergency line for guidance. MOD places caution barriers around the vehicle and directs customers away from the area. |

### 8.6 Medical Emergency

- Any associate who witnesses a medical emergency calls 911 immediately and then notifies the MOD via radio.
- MOD or a trained associate retrieves the **AED** (Automated External Defibrillator) located at the Service Desk and the Receiving desk. AED units are tested monthly (first of each month) by the MOD and documented on the Monthly AED Check Form (BRHI-FC-010).
- MOD assigns an associate to meet the ambulance at the front entrance and guide EMS to the patient.
- MOD completes an Incident Report (BRHI-SF-001) within 24 hours of the event.

---

## Appendices

### Appendix A: Store Format Variations

| Element | Standard Format (147 stores) | Compact Format (28 stores) | Pro-Focused Format (12 stores) |
|---|---|---|---|
| Register count | 12 (8 FE + 2 Pro + 1 GC + 1 SD) | 6 (4 FE + 1 Pro + 1 SD) | 14 (6 FE + 4 Pro + 2 GC + 2 SD) |
| Standard till amount | $210 | $160 | $210 |
| DA count (morning) | 8–10 | 4–5 | 8–10 |
| MOD count (per day) | 2 (morning, afternoon/evening) | 1 (all day) | 2 (morning, afternoon/evening) |
| Forklifts | 2 | 1 | 3 |
| Garden Center | Yes | Limited (seasonal outdoor area only) | Yes (expanded) |
| Pro Desk | Yes | Shared with Service Desk | Yes (dedicated, 2 desks) |

### Appendix B: Key Contacts

| Role / Service | Contact | Available |
|---|---|---|
| Security Monitoring Center | 1-800-555-0123 | 24/7 |
| Facilities Maintenance | 1-800-555-0145 (dispatch) / ext. 8000 (internal) | 24/7 (emergency) / Business hours (routine) |
| IT Help Desk | ext. 9000 (internal) / 1-800-555-0188 (external) | 24/7 |
| Regional Operations Manager | See store-specific contact list | Business hours / cell after hours |
| Regional VP Store Operations | See store-specific contact list | Cell: see contact list |
| Armored Car Service (Loomis) | 1-800-555-0199 | Pickup per schedule |
| Gas Utility (varies by region) | Posted on Electrical Room door | 24/7 |
| Electric Utility (varies by region) | Posted on Electrical Room door | 24/7 |
| Snow Removal Contractor | See store-specific vendor list | Per contract activation |
| BRHI Associate Hotline (closures) | 1-800-555-0177 | 24/7 (recording updated by SM) |
| Employee Assistance Program (EAP) | 1-800-555-0166 | 24/7 (counseling) |
| EnviroSafe (Hazmat disposal) | 1-800-555-0199 | Per contract schedule |

### Appendix C: Form Index

| Form # | Form Name | Location | Used By |
|---|---|---|---|
| BRHI-FC-001 | Morning Facility Checklist (Opening) | Cash Office | MOD |
| BRHI-FC-002 | Safe Count Reconciliation | Cash Office | COA |
| BRHI-FC-003 | Department Readiness Checklist | Service Desk / DA stations | DA |
| BRHI-FC-004 | Daily Operations Log | MOD station | MOD |
| BRHI-FC-005 | Till Pick-Up Log | Cash Office | COA / MOD |
| BRHI-FC-006 | Closing Facility Checklist | Cash Office | MOD |
| BRHI-FC-007 | MOD Handoff Checklist | MOD station | MOD (outgoing/incoming) |
| BRHI-FC-008 | Weekly Signage Plan (distributed by email) | Service Desk | LA / MOD |
| BRHI-FC-009 | Monthly AED Check Form | Service Desk | MOD |
| BRHI-FC-010 | Incident Report (BRHI-SF-001) | Service Desk / MOD station | MOD |
| BRHI-FC-011 | Early Closure Report | MOD station (digital) | MOD |
| BRHI-FC-012 | Register Close Variance Report | Cash Office | Cashier / MOD |

### Appendix D: Glossary

| Term | Definition |
|---|---|
| **T-0** | Scheduled store opening time (e.g., 6:00 AM Monday–Saturday) |
| **T+0** | Scheduled store closing time (e.g., 9:00 PM Monday–Saturday) |
| **T-minus** | Time before opening (e.g., T-90 = 90 minutes before opening) |
| **T-plus** | Time after closing (e.g., T+30 = 30 minutes after closing) |
| **MOD** | Manager on Duty — the management-level associate responsible for store operations during their shift |
| **COA** | Cash Office Associate — the associate responsible for safe, tills, and daily cash handling |
| **DA** | Department Associate — the associate assigned to maintain a specific department |
| **RA** | Receiving Associate — the associate responsible for inbound freight and backroom operations |
| **LA** | Lot Associate — the associate responsible for parking lot, carts, and exterior areas |
| **GA** | Greeter Associate — the associate stationed at the front entrance to welcome customers |
| **SS** | Shift Supervisor — the supervisor overseeing front-end or zone operations |
| **Zoning** | The process of straightening merchandise on shelves, facing products forward, and ensuring the sales floor is presentation-ready (also called "recovery" or "facing") |
| **RTV** | Return to Vendor — merchandise returned to the vendor for credit |
| **SDS** | Safety Data Sheet — document providing safety information about chemical products |
| **AED** | Automated External Defibrillator — device used to treat sudden cardiac arrest |
| **NOAA** | National Oceanic and Atmospheric Administration — US government agency that provides weather forecasts and warnings |
| **NWS** | National Weather Service — a division of NOAA |

---

*End of Document BRHI-BP-004 v2.5*
