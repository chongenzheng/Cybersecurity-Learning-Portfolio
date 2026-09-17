# Botium Toys Security Audit

## Project Overview

This project is a simulated internal security audit for **Botium Toys**, a fictional business used as part of the Google Cybersecurity Professional Certificate.

The objective of this project was to review the organization's existing security posture, assess security controls and compliance practices, identify security gaps, and recommend improvements.

The audit included:

- Reviewing the audit scope and organizational assets
- Analyzing the existing risk assessment
- Assessing security controls
- Reviewing compliance practices
- Identifying security gaps
- Developing remediation recommendations

---

## Audit Scope

The scope of the audit covered the entire security program at Botium Toys, including organizational assets, internal processes, security controls, and compliance practices.

Assets included:

- On-premises equipment
- Employee devices and remote workstations
- Internal networks
- Internet access
- Databases and data storage
- Accounting systems
- E-commerce systems
- Inventory management systems
- Surveillance equipment
- Legacy systems

The goal was to determine which controls and compliance practices needed improvement in order to strengthen the organization's overall security posture.

---

## Initial Risk Assessment

The provided risk assessment assigned Botium Toys a:

> **Risk Score: 8/10**

The relatively high risk score resulted from missing or insufficient security controls and gaps in compliance practices.

Several major risks were identified:

- Employees had excessive access to internally stored data.
- Least privilege was not implemented.
- Separation of duties was not implemented.
- Sensitive customer and payment data was not encrypted.
- No Intrusion Detection System (IDS) was deployed.
- No disaster recovery plan existed.
- Critical data was not backed up.
- Password requirements were insufficient.
- No centralized password management system was implemented.
- Legacy system monitoring lacked a regular schedule and clearly defined intervention procedures.

---

## Security Controls Assessment

I evaluated the organization's existing controls across administrative, technical, and physical control areas.

### Administrative / Managerial Controls

| Control | Assessment |
|---|---|
| Least Privilege | ❌ Needs Improvement |
| Disaster Recovery Plan | ❌ Needs Improvement |
| Password Policies | ❌ Needs Improvement |
| Separation of Duties | ❌ Needs Improvement |

### Technical Controls

| Control | Assessment |
|---|---|
| Firewall | ✅ Implemented |
| Intrusion Detection System (IDS) | ❌ Needs Improvement |
| Backups | ❌ Needs Improvement |
| Antivirus Software | ✅ Implemented |
| Legacy System Monitoring | ❌ Needs Improvement |
| Encryption | ❌ Needs Improvement |
| Password Management System | ❌ Needs Improvement |

### Physical / Operational Controls

| Control | Assessment |
|---|---|
| Physical Locks | ✅ Implemented |
| CCTV Surveillance | ✅ Implemented |
| Fire Detection / Prevention | ✅ Implemented |

---

## Key Security Findings

### 1. Excessive Access to Sensitive Data

Least privilege and separation of duties were not properly implemented.

Employees had broad access to internally stored information, creating unnecessary exposure of sensitive data.

**Risk:**  
A compromised or malicious employee account could potentially access more information than necessary.

**Recommended Action:**  
Implement role-based access restrictions using the principles of least privilege and separation of duties.

---

### 2. Lack of Encryption

Customer credit card information was accepted, processed, transmitted, and stored without adequate encryption.

**Risk:**  
If sensitive data is accessed by an unauthorized party, the information may be directly readable and usable.

**Recommended Action:**  
Encrypt sensitive customer and payment information during processing, transmission, and storage.

---

### 3. No Intrusion Detection System

The organization had a firewall, but no IDS was implemented.

**Risk:**  
Suspicious or malicious network activity may not be detected quickly.

**Recommended Action:**  
Deploy an IDS to improve detection and support timely response to potential intrusions.

---

### 4. No Disaster Recovery Plan or Critical Data Backups

Botium Toys did not have a disaster recovery plan or backups of critical data.

**Risk:**  
A major incident could result in significant data loss and affect business continuity.

**Recommended Action:**  
Develop a disaster recovery plan and establish regular backups for critical organizational data.

---

### 5. Weak Password Management

A password policy existed, but its requirements were insufficient. The organization also lacked a centralized password management system.

**Risk:**  
Weak password requirements may increase the likelihood of account compromise.

**Recommended Action:**  
Strengthen password requirements and implement centralized password management to consistently enforce password policies.

---

### 6. Inconsistent Legacy System Management

Legacy systems were being monitored and maintained, but there was no regular schedule and intervention procedures were unclear.

**Risk:**  
Inconsistent maintenance may leave known risks or vulnerabilities unmanaged.

**Recommended Action:**  
Establish scheduled monitoring, maintenance, and clearly defined intervention procedures for legacy systems.

---

## Compliance Assessment

The audit also reviewed practices associated with several compliance areas.

### PCI DSS

Areas reviewed included:

- Access to customer credit card information
- Secure processing and transmission of payment information
- Encryption
- Password management

The assessment identified gaps related to access restrictions, encryption, and password management.

### GDPR

Areas reviewed included:

- Protection of E.U. customer data
- Breach notification
- Asset classification and inventory
- Privacy policies and procedures

One important finding was that organizational assets had been inventoried, but had not been properly classified.

### SOC

Areas reviewed included:

- User access policies
- Confidentiality of sensitive information
- Data integrity
- Data availability

Access control remained a significant concern because internally stored data was accessible too broadly instead of being limited according to authorization and job responsibilities.

---

## Recommendations

Based on the assessment, the following improvements were prioritized:

1. Implement least privilege.
2. Implement separation of duties.
3. Encrypt sensitive customer and payment information.
4. Deploy an Intrusion Detection System.
5. Develop a disaster recovery plan.
6. Maintain backups of critical data.
7. Strengthen password policies.
8. Implement a centralized password management system.
9. Establish regular legacy system monitoring and maintenance.
10. Properly classify organizational assets.

---

## What I Learned

One of the most important lessons from this project was understanding the difference between the **existence of a security control** and the **adequacy and effectiveness of that control**.

During my initial assessment, I focused primarily on the question:

> **"Does this control exist?"**

This caused me to classify some controls incorrectly.

After reviewing the assessment, I realized that a security audit also needs to ask:

> **"Is this control properly implemented and sufficient to address the risk?"**

For example, Botium Toys had a password policy. However, simply having a policy did not mean the control was adequate because its password requirements were too weak.

Similarly:

> **Asset Inventory ≠ Asset Classification**

Knowing which assets exist does not automatically mean those assets have been properly classified according to their sensitivity or importance.

This project helped me shift my approach from:

**Control existence → Yes / No**

to:

**Control existence → Implementation → Adequacy → Effectiveness → Risk Reduction**

This distinction is an important part of evaluating an organization's actual security posture.

---

## Skills Practiced

- Security Auditing
- Risk Assessment
- Security Control Assessment
- Security Gap Analysis
- NIST Cybersecurity Framework concepts
- Administrative, Technical, and Physical Controls
- PCI DSS fundamentals
- GDPR fundamentals
- SOC fundamentals
- Access Control
- Least Privilege
- Separation of Duties
- Security Remediation Planning
- Defense in Depth

---

## Project Files

- `Controls-and-Compliance-Checklist.pdf`
- `README.md`

---

## Project Context

This project was completed as part of the **Google Cybersecurity Professional Certificate**.

Botium Toys is a fictional organization created for educational purposes. The project was used to practice applying cybersecurity risk, control, audit, and compliance concepts in a simulated business environment.
