
# PASTA Threat Modeling — Sneaker Marketplace Application

**Category:** Cybersecurity / Threat Modeling / Application Security  
**Framework:** PASTA (Process for Attack Simulation and Threat Analysis)  
**Exercise:** Seven-stage threat model for a mobile marketplace connecting sneaker buyers and sellers  
**Materials:** My completed PASTA worksheet and course exemplar

## 1. Activity Overview

The scenario involves a sneaker marketplace mobile application that connects sellers and buyers. Users can create accounts, communicate with sellers, rate sellers, and complete payments. The exercise uses the seven PASTA stages to identify business objectives, relevant technologies, data flows, threats, vulnerabilities, attack paths, and risk-reducing controls.

**Objective:** Practice linking technical vulnerabilities to realistic business threats and identifying proportionate controls before application launch.

## 2. My Original Analysis — Seven PASTA Stages

### Stage I — Define Business and Security Objectives

I identified the main business goal as connecting buyers and sellers and enabling transactions. Because the app handles sensitive information and payments, I noted potential compliance considerations including PCI DSS, consumer protection, privacy requirements such as GDPR/CCPA where applicable, online marketplace obligations, and sales tax requirements.

**Reflection:** My response identified relevant compliance considerations, but the assignment asked for **2–3 concrete business requirements**. A clearer set would be: (1) create and manage accounts, (2) process payments, and (3) protect customer/payment data. Applicability of particular laws depends on the marketplace's operations and jurisdictions; PCI DSS is an industry standard, not a statute.

### Stage II — Define the Technical Scope

**Technologies in my submission:** API, PKI, SHA-256, SQL.

I initially prioritized **SHA-256 and PKI**, reasoning that they protect sensitive information and secure communications, followed by APIs because they connect application components.

**Reflection:** The course exemplar also includes **AES**, which I omitted. Prioritizing the **API attack surface** is more compelling for a marketplace because APIs connect users, accounts, orders, and payments. SHA-256 is a hash function, **not encryption**; its security benefit depends on the specific use case. Passwords should use a dedicated password-hashing algorithm such as Argon2id, not plain SHA-256.

### Stage III — Decompose the Application

I included a **login/sign-up data-flow diagram** connecting the user, identity-handling process, and database, with credential-related data flows.

**Reflection:** The diagram provides a starting point. A stronger model would label trust boundaries, distinguish credential verification from data storage, and also model payment and buyer–seller interactions. The provided exercise diagram was a sample, not a full production architecture.

### Stage IV — Threat Analysis

I identified two scenarios:

1. **Insider tampering:** an insider modifies product information or seller reviews, influencing purchasing decisions.
2. **External SQL injection:** an unauthorized actor attacks database-backed functionality, potentially affecting confidentiality, integrity, or availability.

**Reflection:** These are defensible threat scenarios, although the exemplar uses the shorter categories **Injection** and **Session Hijacking**. SQL injection does not necessarily cause a crash; its effects depend on the query, permissions, and application behavior.

### Stage V — Vulnerability Analysis

I focused on SQL injection risk due to insufficient handling of user input and the limitations of relying only on cryptographic protections.

**Reflection:** This needs a more precise root cause: **dynamic SQL built from untrusted input without parameterized queries / prepared statements**. Input validation is useful, but input filtering alone is not a reliable substitute. The exemplar additionally highlights a **broken API token** as a possible weakness.

### Stage VI — Attack Modeling

My worksheet included a sample attack tree with **User Data** as the target and branches for **API Attack** and **DOM-based XSS**, associated with weaknesses in authentication and input handling.

**Reflection:** This shows alternative attack paths but does not align perfectly with my earlier emphasis on insider tampering and SQL injection. A stronger attack tree would explicitly map **threat actor → entry point → weakness → action → affected asset**, and would distinguish authentication failures from authorization failures.

### Stage VII — Risk Analysis and Impact

I proposed these controls:

1. **Prepared statements and input validation** to mitigate SQL injection.
2. **Safe DOM APIs** to mitigate DOM-based XSS.
3. **Session timestamps / expiration** to limit the lifetime of a stolen session.
4. **Firewalls and intrusion detection** to reduce or detect suspicious access.

**Reflection:** These controls are relevant, but their mechanisms should be described accurately. Prepared statements keep SQL structure separate from parameter values; sanitization alone does not guarantee protection. For DOM XSS, use `textContent` for text and avoid unsafe sinks such as untrusted `innerHTML`. Session expiry reduces the window for misuse but does not stop theft of an active session; pair it with Secure/HttpOnly cookies, session rotation, revocation, and reauthentication for sensitive actions. Firewalls/IDS provide layered protection, not a replacement for secure application logic.

## 3. Comparison With the Course Exemplar

| Stage | My Submission | Exemplar | What I Learned |
|---|---|---|---|
| I — Objectives | Marketplace goal and a broad set of compliance considerations | Account creation, payment processing, PCI DSS | State concrete functional/security requirements first; assess regulations separately. |
| II — Scope | API, PKI, SHA-256, SQL; prioritized PKI/SHA-256 | API, PKI, AES, SHA-256, SQL; prioritized APIs | Include AES; prioritize based on exposure and sensitive data flows, not only cryptographic importance. |
| III — Decomposition | Login/sign-up data-flow diagram | Sample data-flow diagram | Make trust boundaries and major transaction flows explicit. |
| IV — Threats | Insider tampering; SQL injection | Injection; session hijacking | Both are possible; differentiate a threat category from a detailed scenario. |
| V — Vulnerabilities | Weak input restrictions / SQL injection exposure | Lack of prepared statements; broken API token | Identify specific, testable root causes. |
| VI — Attack Model | API attack and DOM-based XSS branches | Sample attack tree | Keep attack paths consistent with identified threats and vulnerabilities. |
| VII — Controls | Prepared statements, DOM safety, timestamps, firewall/IDS | SHA-256, incident response, password policy, least privilege | Combine targeted technical controls with governance, response, and access controls. |

**Important:** The exemplar is a sample answer, **not proof that all other reasonable answers are wrong**. The exercise does not provide enough implementation evidence to assert that any listed vulnerability actually exists in a deployed application.

## 4. Key Concepts and Corrections

### Threat vs. Vulnerability vs. Attack Path vs. Risk

- **Threat:** An attacker may attempt to steal or alter marketplace data.
- **Vulnerability:** A specific weakness, such as missing object-level authorization or unsafe SQL construction.
- **Attack path:** A plausible sequence connecting an attacker, an entry point, a weakness, and an outcome.
- **Risk:** The likelihood and business impact of that outcome, taking existing safeguards into account.

### Why PASTA Analyzes Threats Before Vulnerabilities

PASTA is risk-driven: first identify meaningful threats to business assets, then investigate the weaknesses that might enable them. The process is iterative—finding a new weakness can justify revisiting the threat analysis.

### Session Expiration Is Not Full Session-Hijacking Protection

Expiration limits how long a stolen session remains useful, but attackers may use it before expiry. Complementary protections include TLS, Secure/HttpOnly/SameSite cookies, strong session identifiers, rotation on login, server-side revocation, and step-up authentication for payments or account changes.

## 5. Improved Risk-to-Control Mapping

| Asset / Business Concern | Threat Scenario | Weakness to Investigate | Controls |
|---|---|---|---|
| Buyer and seller accounts | Session hijacking | Exposed tokens, weak session management | TLS, secure cookie flags, short/appropriate lifetimes, rotation, revocation, sensitive-action reauthentication |
| Product and order records | Unauthorized modification | Missing object/function authorization | Server-side authorization on every request, least privilege, audit logs |
| Marketplace database | SQL injection | String-built SQL from user inputs | Prepared statements, allowlist validation, restricted DB privileges |
| Customer-facing pages | DOM-based XSS | Untrusted input passed to unsafe DOM sinks | `textContent`, contextual output handling, vetted HTML sanitization when needed, CSP defense in depth |
| Payment operations | Payment fraud or data exposure | Overprivileged access or unsafe payment integration | Reputable payment processor, scoped credentials, transaction monitoring, applicable PCI DSS controls |

## 6. Challenges and Lessons Learned

- **Challenge:** I initially equated strong cryptography with the highest-priority technology. **Lesson:** Prioritize based on actual attack surfaces and data flows; encryption and hashing solve different problems.
- **Challenge:** My vulnerability description focused on input restrictions. **Lesson:** Name the precise flaw, such as missing parameterized queries, instead of relying on generic filtering.
- **Challenge:** My attack tree did not fully trace the threats identified earlier. **Lesson:** Maintain traceability across all seven PASTA stages.
- **Challenge:** I considered timestamps a session-hijacking mitigation. **Lesson:** They reduce exposure time but must be combined with session security and revocation.
- **Challenge:** I listed many regulations. **Lesson:** Separate broad legal considerations from confirmed requirements and explain their applicability.

## 7. Next Steps

1. Redraw the DFD with explicit trust boundaries for login, product search, messaging, and checkout.
2. Build an attack tree directly from the identified injection and account/session threats.
3. Add a small risk register with likelihood, impact, affected assets, evidence, and remediation priority.
4. Practice testing a deliberately vulnerable local API for broken object-level authorization and injection, then document the fixes.
5. Apply the same PASTA process to a future university-information website project before deployment.

## 8. Supporting Materials

- `PASTA_worksheet_my_submission.pdf` — my original submitted worksheet.
- `PASTA_worksheet_exemplar.docx` — course-provided sample response.

**Portfolio note:** The worksheet and exemplar are included for personal learning documentation; this README distinguishes my original responses from later analysis and corrections.
  
