## Project Overview

This project focuses on investigating a phishing alert and applying an incident response playbook to determine whether to escalate it.

As a simulated **Security Operations Center (SOC) Analyst**, I reviewed a suspicious email, evaluated potential phishing indicators, verified the malicious attachment using findings from a previous VirusTotal investigation, and documented the results in an alert ticket.

The primary objectives were to:

- Investigate a phishing alert and identify suspicious email characteristics.
- Follow an incident response playbook and its decision-making process.
- Apply the **5 Ws framework** to understand the incident.
- Determine whether the alert was legitimate or a false positive.
- Document investigation findings and make an appropriate escalation decision.

## Scenario

A financial services company received a phishing alert after an employee downloaded and opened a suspicious email attachment.

The attachment had previously been investigated using VirusTotal and identified as malicious.

As a Level 1 SOC Analyst, my responsibility was to evaluate the alert, follow the organization's phishing incident response playbook, and determine whether the incident required escalation.

### Alert Information

| Field | Details |
|---|---|
| Ticket ID | A-2703 |
| Alert Type | SERVER-MAIL — Phishing attempt, possible malware download |
| Severity | Medium |
| Affected Department | Human Resources |
| Incident Date | July 20, 2022 |
| Final Ticket Status | Escalated |

## Tools and Frameworks

- **Phishing Incident Response Playbook:** Guided the investigation and escalation process.
- **VirusTotal:** Provided previous malware analysis findings for the suspicious attachment.
- **Alert Ticket:** Used to document evidence, findings, and the final response decision.
- **5 Ws Framework:** Helped organize the investigation by identifying who, what, when, where, and why.

## Investigation Process

### 1. Review the Alert

I began by reviewing the alert ticket and its supporting information.

The alert indicated that an employee might have opened a malicious email attachment or clicked a suspicious link.

The alert was classified as **Medium severity**, requiring further investigation.

Following the incident response playbook, I updated the ticket status to **Investigating**.

### 2. Analyze the Suspicious Email

I examined the sender information, subject line, message body, and attachment details.

**Email Information:**

| Field | Details |
|---|---|
| Sender Name | Def Communications |
| Sender Address | 76tguyhh6tgftrt7tg.su |
| Sender IP | 114.114.114.114 |
| Recipient | hr@inergy.com |
| Recipient IP | 176.157.125.93 |
| Subject | Re: Infrastructure Egnieer role |
| Attachment | bfsvc.exe |
| Attachment Type | Executable file (.exe) |

Several suspicious characteristics were identified.

**Sender Identity Inconsistency**

The sender's display name was "Def Communications," while the email signature identified the sender as "Clyde West."

This inconsistency raised concerns about the sender's identity.

**Spelling and Grammatical Errors**

The subject line contained a spelling error: "Egnieer" instead of "Engineer."

The email body also contained grammatical errors, which contributed to the suspicious nature of the message.

**Suspicious Attachment**

The email claimed to contain a resume and cover letter, but the attachment was named `bfsvc.exe`.

An executable file is inconsistent with the typical document formats expected for a job application.

The attachment was also password-protected, with the password provided in the email body.

These characteristics suggested that the message could be an attempt to persuade the recipient to execute malicious software.

### 3. Verify the Malicious Attachment

The attachment's SHA256 hash had already been investigated in a previous VirusTotal malware analysis activity.

**Previous investigation findings:**

- 52 out of 70 security vendors identified the file as malicious.
- The file was associated with backdoor and credential-stealing Trojan classifications.
- The sandbox report identified potentially malicious techniques, including Process Injection (T1055).

These findings supported the conclusion that the attachment was malicious.

### 4. Apply the 5 Ws Framework

I used the 5 Ws to organize the available information and understand the incident.

| Question | Investigation Finding |
|---|---|
| Who? | An external sender identifying as Def Communications sent an email to the HR department. |
| What? | A phishing email containing a malicious executable attachment was received, downloaded, and opened. |
| When? | July 20, 2022, at 09:30:14 AM, according to the email record. |
| Where? | The incident occurred within the email environment of a financial services company. |
| Why? | The email may have been intended to compromise an employee's device or obtain sensitive information. The attacker's exact objective was not confirmed. |

### 5. Determine Whether to Escalate

After reviewing the evidence and following the phishing incident response playbook, I determined that the alert required escalation.

The decision was based on the following findings:

1. The email contained a known malicious executable attachment.
2. The sender information and email content displayed multiple phishing indicators.
3. The employee reportedly downloaded and opened the attachment.
4. Previous VirusTotal analysis supported the malicious classification of the file.
5. Additional investigation was necessary to determine the full impact of the incident.

Based on these findings, I determined that the alert was legitimate rather than a false positive.

### 6. Update the Alert Ticket

I completed the alert ticket by documenting the investigation findings and updating the final status.

**Final Ticket Information:**

| Field | Final Result |
|---|---|
| Ticket ID | A-2703 |
| Severity | Medium |
| Ticket Status | Escalated |
| Escalation Destination | Tier 2 SOC Analyst |
| Reason | Confirmed malicious attachment, phishing indicators, and reported file execution |

The ticket comments summarized the suspicious email characteristics, VirusTotal findings, and reasons for escalation.

## Key Findings

The investigation identified several important security concerns.

**1. Malicious Attachment**

The attachment was an executable file that had previously been identified as malicious through VirusTotal analysis.

**2. Phishing Indicators**

The sender identity inconsistency, spelling errors, and suspicious attachment format provided additional evidence supporting the phishing classification.

**3. Potential Endpoint Compromise**

The employee reportedly downloaded and opened the malicious attachment, creating a potential risk of endpoint compromise.

However, the complete impact of the incident was not established during this investigation.

**4. Escalation Required**

The combination of malicious file evidence and suspicious email characteristics justified escalation to a Tier 2 SOC Analyst for further investigation.

## Skills Demonstrated

- Phishing email analysis
- SOC alert triage
- Incident response playbook execution
- Malware reputation verification
- Identification of phishing indicators
- Security incident documentation
- Alert escalation decision-making
- Application of the 5 Ws investigation framework

## Lessons Learned

This activity helped me understand how SOC analysts use structured procedures to investigate and respond to phishing incidents.

**1. Following an Incident Response Playbook**

A playbook provides a consistent process for evaluating alerts, documenting findings, and determining appropriate response actions.

**2. Correlating Multiple Sources of Evidence**

A suspicious sender address or grammatical error alone does not prove that an email is malicious.

However, when combined with a confirmed malicious attachment and reported file execution, these indicators provide stronger evidence of a security incident.

**3. Distinguishing Evidence from Conclusions**

I learned to distinguish between observed evidence and analytical conclusions.

For example:

- **Evidence:** The attachment was an executable file named `bfsvc.exe`.
- **Evidence:** VirusTotal reported 52 malicious detections out of 70 security vendors.
- **Finding:** The email contained a malicious attachment and displayed multiple phishing indicators.
- **Decision:** Escalate the alert for further investigation and response.

**4. Understanding Escalation Responsibilities**

A Level 1 SOC Analyst does not necessarily need to resolve every incident independently.

When an alert involves confirmed malicious content and potential system compromise, escalation allows more experienced analysts to investigate the incident and determine the appropriate response.

**5. Documenting Investigation Results**

Clear and accurate ticket documentation helps other analysts understand the incident, review the supporting evidence, and continue the investigation efficiently.

## Conclusion

This project provided practical experience investigating a phishing alert and following an incident response playbook.

By reviewing email characteristics, correlating previous malware analysis findings, and documenting the investigation in an alert ticket, I determined that the incident required escalation.

The activity strengthened my understanding of SOC alert triage, phishing investigation, incident documentation, and evidence-based escalation decisions.

---

**Project Type:** Cybersecurity Lab / Phishing Incident Response  
**Focus Areas:** SOC Operations, Phishing Analysis, Incident Response, Alert Triage  
**Related Project:** Malware Analysis Using VirusTotal and the Pyramid of Pain
