# Data Leak Analysis and Least Privilege Assessment

## Project Overview

This project focuses on analyzing a data leak incident and evaluating access control practices as part of the **Google Cybersecurity Professional Certificate**.

The objective was to identify the factors that contributed to an accidental disclosure of internal documents, review existing security controls, and recommend improvements based on the principle of least privilege.

The assessment included:

- Reviewing a data leak incident
- Identifying access control weaknesses
- Evaluating the implementation of least privilege
- Reviewing NIST SP 800-53 AC-6
- Recommending security control enhancements
- Justifying how the proposed improvements could reduce the risk of future data leaks

---

## Incident Overview

The scenario involved an educational technology company that developed an application to help teachers automatically grade assignments.

The application handled information collected from academic institutions, instructors, parents, and students.

A data leak occurred when a sales representative accidentally shared a link to an internal folder with an external business partner.

### Incident Timeline

1. A sales manager granted team members access to an internal folder containing confidential business information.
2. The folder included documents related to an unreleased product, customer analytics, and promotional materials.
3. The manager did not revoke access after the meeting but instructed employees not to share promotional materials without approval.
4. During a video call, a sales representative accidentally shared the internal folder link instead of the intended promotional materials.
5. The business partner subsequently published the link on the company's social media page.

The incident demonstrated how inadequate access management and accidental information sharing could expose sensitive organizational data.

---

## Security Control Assessment

The primary security control evaluated in this project was:

**Least Privilege**

The principle of least privilege requires users to receive only the access permissions necessary to perform their assigned responsibilities.

### Identified Issues

My assessment identified two primary weaknesses:

**1. Delayed Access Revocation**

Access permissions granted to employees were not revoked promptly after they were no longer needed.

**Risk:**

Unnecessary access permissions increased the possibility of sensitive internal documents being exposed.

**2. Inappropriate Information Sharing**

Internal personnel could accidentally share sensitive documents with external parties.

**Risk:**

Insufficient restrictions on file sharing could allow confidential information to become accessible outside the organization.

---

## NIST Security Framework Review

The assessment referenced the NIST Cybersecurity Framework and NIST Special Publication 800-53.

### NIST Cybersecurity Framework

The provided security plan snapshot mapped data leak protection to the following framework components:

| Component | Description |
|---|---|
| Function | Protect |
| Category | PR.DS: Data Security |
| Subcategory | PR.DS-5: Protections Against Data Leaks |
| Reference | NIST SP 800-53 AC-6 |

This mapping was provided in the activity's security plan snapshot and reflects the framework version used in the course material.

### NIST SP 800-53 AC-6: Least Privilege

NIST SP 800-53 AC-6 addresses the principle of least privilege by requiring organizations to limit access and authorization to what users need to perform their responsibilities.

The provided reference also describes control enhancements, including:

- Restricting access to sensitive resources based on user roles
- Automatically revoking unnecessary access permissions
- Maintaining records of user privileges
- Regularly reviewing user access rights

These practices help organizations reduce unnecessary access to sensitive information.

---

## Key Security Findings

### 1. Inadequate Access Revocation

The sales manager did not revoke access to the internal folder after the meeting.

**Risk:**

Employees retained permissions that were no longer necessary, increasing the possibility of accidental disclosure.

**Recommended Action:**

Automatically revoke temporary or additional access privileges when they are no longer required.

---

### 2. Insufficient Access Monitoring

The incident highlighted the importance of maintaining detailed records of access permissions and user activity.

**Risk:**

Without sufficient access records, identifying responsible users and investigating unauthorized information sharing may become more difficult.

**Recommended Action:**

Maintain records of how user privileges are assigned and used, and conduct regular access reviews.

---

### 3. Inappropriate External Sharing

A sales representative accidentally shared an internal folder link with an external business partner.

**Risk:**

Sensitive internal documents could become accessible to unauthorized external users if sharing permissions are not properly restricted.

**Recommended Action:**

Restrict external sharing of sensitive folders and apply access controls based on user roles and business requirements.

---

## Recommendations

Based on my assessment, I identified the following improvements:

1. Automatically revoke temporary access privileges in a timely manner.
2. Maintain records of user privileges and their usage.
3. Conduct regular reviews of access permissions.
4. Restrict external sharing of sensitive internal resources.
5. Apply the principle of least privilege when granting access to organizational information.

These recommendations focus on reducing unnecessary permissions and improving the organization's ability to manage and monitor access to sensitive data.

---

## Justification

The incident occurred partly because temporary sharing permissions were not revoked promptly, leaving internal documents unnecessarily accessible.

Automatically revoking temporary permissions could reduce the exposure of sensitive information and limit opportunities for accidental disclosure.

Maintaining access records would also improve accountability and support incident investigations by helping security teams determine which users had access to particular resources.

Together, these improvements could strengthen access management and reduce the likelihood of similar incidents.

---

## What I Learned

This project helped me understand that **granting access permissions is only one part of effective access control management**.

One important lesson was recognizing that:

**Authorized Access ≠ Permanently Necessary Access**

A user may initially require access to sensitive information, but those permissions should be reviewed and removed when they are no longer needed.

I also learned that the principle of least privilege involves more than restricting access when accounts are created. It requires continuous management of user permissions throughout their lifecycle.

Another important lesson was the value of maintaining access records. Without sufficient logging and documentation, investigating a data leak and determining how information was exposed can become more difficult.

This activity helped me understand the relationship between:

**Access Authorization → Privilege Management → Access Monitoring → Periodic Review → Risk Reduction**

These practices contribute to stronger information security and data privacy protection.

---

## Skills Practiced

- Data Leak Analysis
- Security Incident Review
- Access Control Assessment
- Principle of Least Privilege
- Privilege Management
- Access Revocation
- User Access Auditing
- Security Control Evaluation
- NIST Cybersecurity Framework Concepts
- NIST SP 800-53 AC-6
- Data Privacy Protection
- Security Remediation Planning

---

## Project Context

This project was completed as part of the **Google Cybersecurity Professional Certificate**.

The activity used a simulated data leak incident at an educational technology company to practice reviewing access control weaknesses and recommending security improvements.

The assessment focused on the principle of least privilege and its application to preventing unauthorized information disclosure.

The project was an educational security control assessment and did not involve implementing changes to a live production environment.
