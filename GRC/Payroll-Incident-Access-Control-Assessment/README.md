# Payroll Incident Access Control Assessment

## Project Overview

This project focuses on investigating a suspicious payroll-related incident and evaluating access control weaknesses as part of the **Google Cybersecurity Professional Certificate**.

The objective was to analyze system event logs, identify authorization issues, and recommend improvements to prevent unauthorized access to sensitive business resources.

The assessment included:

- Reviewing system event logs
- Identifying suspicious account activity
- Cross-referencing event logs with employee records
- Evaluating authentication and authorization controls
- Identifying excessive and outdated user privileges
- Recommending access control improvements

---

## Incident Overview

The scenario involved a growing business where a payroll deposit was unexpectedly transferred to an unknown bank account.

The finance manager reported that the payment change was not intentional, and the transaction was stopped before the funds were lost.

As the cybersecurity professional investigating the incident, my responsibility was to review the available records, identify potential access control weaknesses, and recommend security improvements.

---

## Investigation Process

### Step 1: Review System Event Logs

I examined the provided event log to identify suspicious activity associated with the payroll incident.

The investigation identified the following details:

| Attribute | Finding |
|---|---|
| Event Date | October 3, 2023 |
| Event Time | 8:29:57 AM |
| Account | Legal\Administrator |
| Device | Up2-NoGud |
| IP Address | 152.207.255.255 |

These details helped identify the account and device associated with the suspicious event.

### Step 2: Cross-Reference Employee Records

I compared the event log information with the employee directory to investigate the account's authorization status.

The investigation identified:

| Attribute | Finding |
|---|---|
| Employee | Robert Taylor Jr. |
| Role | Contractor – Legal Attorney |
| Access Level | Admin |
| Authorization Start Date | September 4, 2019 |
| Authorization End Date | December 27, 2019 |
| Suspicious Activity Date | October 3, 2023 |

The records indicated that the contractor's authorization period had expired several years before the suspicious activity occurred.

Despite this, the account still appeared to have administrative access.

---

## Access Control Assessment

The investigation focused on two important security concepts:

**Authentication:** Verifying the identity of a user attempting to access a system.

**Authorization:** Determining which resources and actions an authenticated user is permitted to access.

### Identified Issues

**1. Expired Account Access**

The contractor's authorization period ended on December 27, 2019, but the account was associated with activity on October 3, 2023.

**Risk:**

Accounts that remain active after their authorization expires may allow unauthorized individuals to access sensitive organizational resources.

**2. Excessive Administrative Privileges**

The contractor account retained administrative-level access despite its expired authorization period.

**Risk:**

Excessive privileges could allow an unauthorized user to access or modify sensitive business information and systems beyond what is necessary for their role.

---

## Key Security Findings

### 1. Inadequate Account Deprovisioning

The investigation revealed a potential failure to revoke account access after the contractor's authorized employment period ended.

**Risk:**

Outdated accounts may remain available for unauthorized access, increasing the organization's exposure to security incidents.

**Recommended Action:**

Promptly disable or revoke access for inactive, expired, or unauthorized user accounts.

---

### 2. Excessive User Privileges

The contractor account was associated with administrative privileges.

**Risk:**

Administrative permissions may provide broader access than required for the user's responsibilities.

**Recommended Action:**

Assign user permissions based on the principle of least privilege, ensuring that individuals receive only the access necessary to perform their assigned tasks.

---

### 3. Insufficient Access Reviews

The continued presence of an expired account with administrative privileges suggested weaknesses in the organization's access review process.

**Risk:**

Without periodic reviews, outdated accounts and unnecessary permissions may remain undetected.

**Recommended Action:**

Conduct regular reviews of user account status, authorization periods, and assigned permissions.

---

## Recommendations

Based on my investigation, I identified the following improvements:

1. Promptly revoke access for inactive, expired, or unauthorized users.
2. Apply the principle of least privilege when assigning user permissions.
3. Conduct periodic reviews of account status and authorization periods.
4. Regularly evaluate administrative privileges to ensure they remain necessary.
5. Establish consistent procedures for managing access when employees or contractors leave the organization.

These recommendations focus on reducing unauthorized access and strengthening the organization's identity and access management practices.

---

## What I Learned

This project helped me understand how access control weaknesses can create security risks even when an organization maintains user accounts and authorization records.

One important lesson was recognizing that:

**Successful Authentication ≠ Valid Authorization**

An account may successfully access a system even though the user's authorization has expired or the assigned permissions are no longer appropriate.

I also learned the importance of comparing information from multiple sources during a security investigation.

The event logs provided details about suspicious system activity, while the employee directory provided information about the user's role, authorization period, and access privileges.

By combining these records, I was able to identify potential weaknesses that would not have been as apparent from either source alone.

Another important lesson was that access control requires continuous management rather than a one-time permission assignment.

This activity helped me understand the relationship between:

**Event Log Analysis → Identity Verification → Authorization Review → Security Gap Identification → Access Control Improvement**

These steps provide a structured approach to investigating suspicious account activity and improving organizational security.

---

## Skills Practiced

- Identity and Access Management (IAM)
- Access Control Assessment
- Authentication and Authorization
- Security Event Log Analysis
- Account Privilege Review
- Principle of Least Privilege
- User Account Deprovisioning
- Access Control Auditing
- Security Incident Investigation
- Security Gap Analysis
- Risk Mitigation Planning
- Security Documentation

---

## Project Context

This project was completed as part of the **Google Cybersecurity Professional Certificate**.

The activity used a simulated payroll security incident to practice investigating suspicious account activity, reviewing employee authorization records, and identifying access control weaknesses.

The project focused on applying identity and access management principles to reduce the risk of unauthorized access to organizational systems.

The assessment was conducted in a simulated environment and did not involve modifying live accounts or production systems.
