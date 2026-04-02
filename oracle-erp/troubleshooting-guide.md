# Oracle Fusion Cloud ERP Troubleshooting Guide

## BuildRight Home Improvement, Inc. (BRHI)

---

## 1. Document Control

| Field | Detail |
|---|---|
| **Document ID** | BRHI-TECH-007 |
| **Version** | 1.0 |
| **Classification** | Internal — All Associates |
| **Effective Date** | April 2, 2026 |
| **Document Owner** | Chief Technology Officer |
| **Approved By** | Executive Leadership Team |
| **Review Cycle** | Quarterly |
| **Next Review Date** | July 2, 2026 |
| **Distribution** | All associates, IT support, Oracle CoE |

### Revision History

| Version | Date | Author | Description |
|---|---|---|---|
| 1.0 | April 2, 2026 | Enterprise Technology Team | Initial release — comprehensive troubleshooting guide |

---

## 2. Purpose and Scope

### 2.1 Purpose

This guide provides step-by-step troubleshooting procedures for common issues encountered when using Oracle Fusion Cloud ERP. It covers:

- **Login and Access Issues**: Problems logging in or accessing the system
- **Performance Issues**: Slow response times, timeouts
- **Transaction Errors**: Common error messages and solutions
- **Data Issues**: Missing or incorrect data
- **Integration Issues**: Problems with connected systems
- **AI and Digital Assistant Issues**: Problems with AI features

### 2.2 Scope

This guide applies to:

- All Oracle Fusion Cloud ERP users across all roles
- All devices (desktop, tablet, mobile)
- All Oracle modules (Phase 1-3)

### 2.3 Troubleshooting Philosophy

1. **Self-Service First**: Try self-help before contacting support
2. **Document Everything**: Record error messages, steps taken, screenshots
3. **Escalate Appropriately**: Use the right channel for your issue type
4. **Learn and Share**: Share solutions with colleagues

---

## 3. Quick Reference: Common Issues and Solutions

### 3.1 Login and Access Issues

| Issue | Possible Causes | Solution |
|---|---|---|
| **"Invalid credentials"** | Wrong username/password | 1. Check Caps Lock<br>2. Reset password via `password.buildright.com`<br>3. Use SSO (same as network login) |
| **MFA not working** | Time mismatch, app issue | 1. Check device time is correct<br>2. Use backup codes<br>3. Re-enroll in MFA |
| **"No access to this page"** | Insufficient permissions | 1. Contact manager to request access<br>2. Check role assignment in HCM |
| **System not loading** | Browser cache, network | 1. Clear browser cache<br>2. Try incognito/private mode<br>3. Check internet connection |
| **Session expired** | Inactivity timeout | 1. Log in again<br>2. Save work frequently |

### 3.2 Performance Issues

| Issue | Possible Causes | Solution |
|---|---|---|
| **Slow page loading** | Network, browser, data volume | 1. Check internet speed (minimum 10 Mbps)<br>2. Close unused browser tabs<br>3. Avoid peak hours (9-11 AM) for heavy reports |
| **Report timing out** | Large data set, complex query | 1. Reduce date range<br>2. Add filters to limit data<br>3. Schedule report for overnight |
| **Mobile app slow** | Network, device memory | 1. Switch to Wi-Fi<br>2. Close other apps<br>3. Restart app |
| **Transaction freezing** | Browser issue, session problem | 1. Refresh page (F5)<br>2. Log out and back in<br>3. Try different browser |

### 3.3 Transaction Errors

| Error Message | Meaning | Solution |
|---|---|---|
| **"Budget check failed"** | Insufficient budget for transaction | 1. Check available budget<br>2. Request budget increase<br>3. Use different budget code |
| **"Approval required"** | Transaction exceeds approval limit | 1. Submit for approval<br>2. Check approval workflow<br>3. Contact approver |
| **"Invalid account combination"** | GL account combination incorrect | 1. Verify chart of accounts<br>2. Use account combination helper<br>3. Contact accounting |
| **"Item not found"** | SKU or item number invalid | 1. Check item number format<br>2. Search item catalog<br>3. Contact merchandising |
| **"Duplicate entry"** | Record already exists | 1. Search existing records<br>2. Use update instead of create<br>3. Contact data governance |

### 3.4 Data Issues

| Issue | Possible Causes | Solution |
|---|---|---|
| **Missing data** | Filter applied, security | 1. Check report filters<br>2. Verify security permissions<br>3. Check data refresh time |
| **Incorrect data** | Timing, source system | 1. Verify data source<br>2. Check data refresh schedule<br>3. Compare with source system |
| **Data not updating** | Cache, refresh needed | 1. Refresh page (F5)<br>2. Clear browser cache<br>3. Wait for next data refresh |
| **Duplicate records** | Data entry error, integration issue | 1. Merge duplicates<br>2. Report to data governance<br>3. Check integration logs |

### 3.5 Integration Issues

| Issue | Possible Causes | Solution |
|---|---|---|
| **POS not syncing** | Network, interface down | 1. Check store network<br>2. Verify POS system status<br>3. Contact IT help desk |
| **Bank feed missing** | Bank connection, file format | 1. Check bank portal<br>2. Verify file format<br>3. Contact treasury |
| **Inventory mismatch** | Timing, cycle count | 1. Perform cycle count<br>2. Check receiving transactions<br>3. Run inventory reconciliation |
| **Customer data missing** | Integration delay, mapping | 1. Wait 15 minutes for sync<br>2. Check integration monitoring<br>3. Contact data governance |

### 3.6 AI and Digital Assistant Issues

| Issue | Possible Causes | Solution |
|---|---|---|
| **AI recommendation wrong** | Data quality, model accuracy | 1. Provide feedback (thumbs down)<br>2. Report to Oracle CoE<br>3. Check AI monitoring dashboard |
| **Digital Assistant not responding** | Network, service issue | 1. Refresh page<br>2. Check system status<br>3. Try again later |
| **AI forecast inaccurate** | Missing data, external factors | 1. Adjust manually<br>2. Provide feedback to AI<br>3. Report to supply chain |
| **AI agent error** | Model issue, data issue | 1. Note error message<br>2. Report to Oracle CoE<br>3. Use manual process as backup |

---

## 4. Step-by-Step Troubleshooting Procedures

### 4.1 Cannot Log In

**Step 1: Verify Credentials**
- Ensure you're using your BuildRight network username (not email)
- Password is same as network password
- Check Caps Lock is off

**Step 2: Password Reset**
1. Go to `https://password.buildright.com`
2. Enter your username
3. Follow password reset process
4. Try logging in again

**Step 3: MFA Issues**
1. Ensure time on your device is correct
2. Try backup codes (saved during enrollment)
3. If still failing, contact IT Help Desk: 1-800-BUILD-IT

**Step 4: Browser Issues**
1. Clear browser cache and cookies
2. Try incognito/private browsing mode
3. Try a different browser (Chrome recommended)

**Step 5: System Status**
1. Check `https://status.buildright.com` for system outages
2. If system is down, wait and try later

### 4.2 Report Not Running

**Step 1: Check Parameters**
1. Verify date range is valid
2. Check filters are correct
3. Ensure you have permission for selected data

**Step 2: Reduce Data Volume**
1. Narrow date range (e.g., 30 days instead of 365)
2. Add filters to limit data
3. Remove unnecessary columns

**Step 3: Schedule Instead**
1. If report is large, schedule it to run overnight
2. Choose "Schedule" instead of "Run"
3. Set time for off-peak hours (2-6 AM)

**Step 4: Contact Support**
1. If still failing, contact Oracle CoE
2. Include: Report name, error message, parameters used
3. Include screenshots if possible

### 4.3 Data Discrepancy

**Step 1: Identify Source of Truth**
1. Determine which system is authoritative
2. Check data refresh schedules
3. Compare timestamps

**Step 2: Check Timing**
1. Is data real-time or batch?
2. How long since last refresh?
3. Are there pending transactions?

**Step 3: Run Reconciliation**
1. Use standard reconciliation reports
2. Identify differences
3. Investigate root cause

**Step 4: Report Issue**
1. If systemic, report to Data Governance
2. Include: Data points, systems, timestamps
3. Request investigation

### 4.4 System Slow or Unresponsive

**Step 1: Check Your Environment**
1. Test internet speed at `speedtest.buildright.com`
2. Close other applications using bandwidth
3. Try wired connection instead of Wi-Fi

**Step 2: Browser Optimization**
1. Clear cache and cookies
2. Disable unnecessary extensions
3. Update browser to latest version

**Step 3: Timing**
1. Avoid peak hours (9-11 AM) for heavy tasks
2. Schedule reports for overnight
3. Use mobile app for quick tasks

**Step 4: Escalate**
1. If persistent, contact IT Help Desk
2. Include: Time of issue, affected screens, your location
3. Note if issue affects multiple users

---

## 5. Error Code Reference

### 5.1 Common Error Codes

| Error Code | Meaning | Action |
|---|---|---|
| **ORA-00001** | Unique constraint violation | Check for duplicate records |
| **ORA-01403** | No data found | Verify search criteria |
| **ORA-01722** | Invalid number | Check numeric fields |
| **ORA-02291** | Integrity constraint violated | Check parent record exists |
| **ORA-04063** | Package has errors | Contact Oracle CoE |
| **ORA-28000** | Account locked | Contact security team |
| **ORA-28001** | Password expired | Reset password |
| **ORA-01034** | Oracle not available | System down, wait and retry |

### 5.2 Application Error Codes

| Error Code | Meaning | Action |
|---|---|---|
| **FND-00001** | General application error | Refresh and retry |
| **FND-00002** | Session expired | Log in again |
| **FND-00003** | Invalid responsibility | Contact manager for access |
| **FND-00004** | Concurrent request failed | Resubmit request |
| **FND-00005** | Validation error | Check entered data |
| **FND-00006** | Workflow error | Contact process owner |
| **FND-00007** | Security violation | Contact security team |

### 5.3 Integration Error Codes

| Error Code | Meaning | Action |
|---|---|---|
| **INT-00001** | Connection failed | Check network, try again |
| **INT-00002** | Authentication failed | Check credentials |
| **INT-00003** | Data format invalid | Verify data mapping |
| **INT-00004** | Timeout exceeded | Increase timeout or simplify |
| **INT-00005** | Business rule violation | Check data validity |
| **INT-00006** | Duplicate record | Check for existing record |
| **INT-00007** | Missing required field | Add required data |

---

## 6. Escalation Procedures

### 6.1 Self-Service First

**Before contacting support:**
1. Check this troubleshooting guide
2. Search Oracle Help Center
3. Ask the Digital Assistant
4. Check system status page
5. Try basic troubleshooting steps

### 6.2 Contacting Support

**Information to provide:**
1. Your name, role, store/department
2. Error message (exact text)
3. Screenshot of error (if possible)
4. Steps to reproduce the issue
5. Business impact (how urgent?)
6. Time the issue occurred
7. What you've already tried

### 6.3 Support Channels

| Issue Type | Channel | Contact | Response Time |
|---|---|---|---|
| **Login/Access** | IT Help Desk | 1-800-BUILD-IT | 15 minutes |
| **System Down** | IT Help Desk | 1-800-BUILD-IT | Immediate |
| **Transaction Errors** | Oracle CoE | oracle-support@buildright.com | 1 hour |
| **Data Issues** | Data Governance | oracle-data-gov@buildright.com | 2 hours |
| **Security Issues** | Security Team | oracle-security@buildright.com | Immediate |
| **Training** | Oracle Training | oracle-training@buildright.com | 1 business day |

### 6.4 Emergency Contacts

**System Outage:**
- IT Operations: 1-800-BUILD-IT (option 9)
- Oracle CoE On-Call: [List in emergency contacts]

**Security Incident:**
- Security Operations Center: 1-888-BUILD-SEC
- CISO: Maria Torres (404-555-0302)

**Data Breach:**
- Legal Department: 1-800-BUILD-LEGAL
- General Counsel: [List in emergency contacts]

---

## 7. Preventive Measures

### 7.1 Regular Maintenance

**User Responsibilities:**
- Keep browser updated
- Clear cache weekly
- Report issues early
- Complete required training

**System Responsibilities:**
- Regular backups
- Performance monitoring
- Security updates
- Data quality checks

### 7.2 Best Practices

1. **Save Frequently**: Use Ctrl+S every 5-10 minutes
2. **Log Out Properly**: Use logout button, don't just close browser
3. **One Session**: Don't open multiple tabs with same transaction
4. **Use Recommended Browser**: Chrome is optimized for Oracle
5. **Avoid Peak Times**: Heavy processing during off-hours

### 7.3 Proactive Monitoring

**System Health Dashboard:**
- Access: `https://status.buildright.com`
- Shows: System status, performance metrics, scheduled maintenance

**Personal Dashboard:**
- Check your approval queue daily
- Review error notifications
- Monitor AI recommendations

---

## 8. Appendices

### Appendix A: Browser Requirements

| Browser | Version | Support Level |
|---|---|---|
| **Google Chrome** | Latest | Fully supported |
| **Microsoft Edge** | Latest | Fully supported |
| **Apple Safari** | Latest | Supported |
| **Mozilla Firefox** | Latest | Supported |
| **Internet Explorer** | Any | Not supported |

### Appendix B: Mobile App Requirements

| Device | OS Version | Support Level |
|---|---|---|
| **iPhone** | iOS 14+ | Fully supported |
| **iPad** | iPadOS 14+ | Fully supported |
| **Android Phone** | Android 10+ | Fully supported |
| **Android Tablet** | Android 10+ | Supported |

### Appendix C: System Status Page

**URL**: `https://status.buildright.com`

**Information Available:**
- Current system status (green/yellow/red)
- Scheduled maintenance windows
- Historical uptime statistics
- Incident reports
- Performance metrics

### Appendix D: Document References

| Document | ID | Location |
|---|---|---|
| Oracle User Guide | BRHI-TECH-005 | oracle-erp/user-guide.md |
| Oracle Reporting Guide | BRHI-TECH-006 | oracle-erp/reporting-guide.md |
| Oracle Security Policy | BRHI-SEC-001 | oracle-erp/security-administration-policy.md |
| Oracle Training Guide | BRHI-TRN-001 | oracle-erp/training-change-management.md |

---

*This document is the property of BuildRight Home Improvement, Inc. and is intended for internal use by authorized associates. Unauthorized distribution, reproduction, or disclosure is prohibited. For questions regarding this document, contact the Enterprise Technology Team at oracle-support@buildright.com or extension 4-0002.*