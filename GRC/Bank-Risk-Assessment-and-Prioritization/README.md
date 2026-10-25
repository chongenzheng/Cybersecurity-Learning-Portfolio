# Bank Risk Assessment and Prioritization

## Project Overview

This project focuses on conducting a cybersecurity risk assessment for a fictional commercial bank as part of the **Google Cybersecurity Professional Certificate**.

The objective was to evaluate potential security risks affecting the bank's financial assets, assess their likelihood and severity, and prioritize risks based on their potential impact on business operations.

The assessment included:

- Reviewing the bank's operating environment
- Identifying potential risks to financial assets
- Evaluating the likelihood of security incidents
- Assessing the severity of potential consequences
- Calculating risk scores
- Prioritizing risks to support security decision-making

---

## Assessment Scope

The assessment focused on the bank's funds as a critical business asset.

The bank's operating environment included:

- A coastal location with relatively low crime rates
- 100 on-premises employees and 20 remote employees
- 2,000 individual customer accounts
- 200 commercial customer accounts
- Strict financial regulations
- Daily access to funds and financial records to meet Federal Reserve requirements

The goal was to determine which risks could most significantly affect the bank's financial assets, operational continuity, and information security.

---

## Risk Identification

Five potential risks were identified in the provided risk register.

| Risk | Description |
|---|---|
| Business Email Compromise | An employee is tricked into sharing confidential information |
| Compromised User Database | Customer data is poorly encrypted |
| Financial Records Leak | A database server containing backed-up data is publicly accessible |
| Theft | The bank's safe is left unlocked |
| Supply Chain Disruption | Delivery delays occur due to natural disasters |

These risks involve different aspects of cybersecurity, including social engineering, data protection, physical security, and business continuity.

---

## Risk Scoring Methodology

I evaluated each risk using two factors:

**Likelihood:** The probability of a security event occurring.

**Severity:** The potential impact of the event on the bank's operations, finances, customers, and regulatory obligations.

Both factors were evaluated using a scale of 1 to 3.

### Likelihood Scale

| Score | Description |
|---|---|
| 1 | Low likelihood |
| 2 | Moderate likelihood |
| 3 | High likelihood |

### Severity Scale

| Score | Description |
|---|---|
| 1 | Low severity |
| 2 | Moderate severity |
| 3 | High severity |

### Risk Calculation

The overall risk score was calculated using:

**Risk Score = Likelihood × Severity**

The resulting score ranges from 1 to 9, with higher scores indicating greater priority for risk management.

---

## Risk Assessment Results

| Risk | Likelihood | Severity | Priority |
|---|---|---|---|
| Business Email Compromise | 2 | 2 | 4 |
| Compromised User Database | 2 | 3 | 6 |
| Financial Records Leak | 3 | 3 | 9 |
| Theft | 1 | 2 | 2 |
| Supply Chain Disruption | 1 | 1 | 1 |

Based on these scores, Business Email Compromise received the highest priority, followed by Compromised User Database and Financial Records Leak.

---

## Key Security Findings

### 1. Business Email Compromise

An employee could be deceived into disclosing confidential information through a social engineering attack.

**Likelihood: 3 | Severity: 3 | Risk Score: 9**

**Risk:**

A successful attack could expose sensitive information, compromise accounts, and potentially cause financial losses.

**Recommended Action:**

Provide security awareness training, implement phishing-resistant multi-factor authentication, and establish verification procedures for sensitive requests.

---

### 2. Compromised User Database

Customer data is inadequately encrypted, increasing the risk of sensitive information exposure.

**Likelihood: 2 | Severity: 3 | Risk Score: 6**

**Risk:**

Unauthorized access could expose customer information, cause financial losses, and create regulatory compliance issues.

**Recommended Action:**

Strengthen database encryption, restrict access to authorized personnel, and regularly review database security configurations.

---

### 3. Financial Records Leak

A database server containing backed-up financial records is publicly accessible.

**Likelihood: 2 | Severity: 2 | Risk Score: 4**

**Risk:**

Unauthorized individuals could access confidential financial records, potentially causing privacy violations and reputational damage.

**Recommended Action:**

Remove unnecessary public access, enforce access controls, and review backup storage configurations.

---

### 4. Physical Theft

The bank's safe is left unlocked, creating an opportunity for unauthorized physical access.

**Likelihood: 1 | Severity: 2 | Risk Score: 2**

**Risk:**

Unauthorized access to the safe could result in financial losses or theft of valuable assets.

**Recommended Action:**

Enforce physical access controls, establish procedures for securing the safe, and conduct regular physical security checks.

---

### 5. Supply Chain Disruption

Natural disasters could delay deliveries and interrupt business operations.

**Likelihood: 1 | Severity: 1 | Risk Score: 1**

**Risk:**

Delivery delays could affect the bank's ability to maintain normal operations and access necessary resources.

**Recommended Action:**

Develop contingency plans, identify alternative suppliers, and review business continuity procedures.

---

## Recommendations

Based on the risk assessment, the following improvements were identified:

1. Prioritize protection against business email compromise.
2. Strengthen encryption and access controls for customer databases.
3. Restrict public access to financial records and backup systems.
4. Improve physical security procedures for valuable assets.
5. Establish contingency plans for potential supply chain disruptions.
6. Periodically reassess risks as the operating environment changes.

---

## What I Learned

This project helped me understand how cybersecurity risk assessments support decision-making and resource prioritization.

One important lesson was recognizing the difference between **Likelihood** and **Severity**.

Likelihood evaluates how probable a security event is, while severity measures the potential consequences if that event occurs.

I also learned that:

**Risk Priority ≠ Likelihood Alone**

A security event with a moderate likelihood may still require significant attention if its potential consequences are severe.

For example, the compromised user database received a likelihood score of 2 but a severity score of 3, resulting in a risk score of 6.

This activity helped me understand the relationship between:

**Risk Identification → Likelihood Assessment → Severity Assessment → Risk Scoring → Risk Prioritization**

These steps provide a structured approach to evaluating cybersecurity risks and identifying where security resources should be focused.

---

## Skills Practiced

- Cybersecurity Risk Assessment
- Risk Identification
- Risk Register Documentation
- Likelihood Assessment
- Impact and Severity Analysis
- Quantitative Risk Scoring
- Risk Prioritization
- Security Risk Mitigation Planning
- NIST Cybersecurity Framework Concepts
- Business Continuity Fundamentals
- Security Decision-Making

---

## Project Context

This project was completed as part of the **Google Cybersecurity Professional Certificate**.

The activity used a fictional commercial bank scenario to practice identifying security risks, evaluating their likelihood and severity, calculating risk scores, and prioritizing risks based on their potential business impact.

The assessment was conducted as an educational exercise using the provided risk register and a simplified risk-scoring methodology.
