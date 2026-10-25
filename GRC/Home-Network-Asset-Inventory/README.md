# Home Network Asset Inventory and Classification

## Project Overview

This project focuses on creating an asset inventory and classifying network devices based on their information sensitivity as part of the **Google Cybersecurity Professional Certificate**.

The objective was to identify devices connected to a home office network, document their characteristics, evaluate potential security risks, and determine which assets require additional protection.

The activity included:

- Identifying devices connected to a home network
- Documenting network access, ownership, and location
- Reviewing the types of information stored on each device
- Evaluating potential security risks
- Classifying assets based on information sensitivity

---

## Asset Identification

The scope of this activity covered six devices connected to or potentially accessing a home office network.

| Asset | Network Access | Owner | Location |
|---|---|---|---|
| Network Router | Continuous | Internet Service Provider (ISP) | On-premises |
| Desktop | Occasional | Homeowner | On-premises |
| Guest Smartphone | Occasional | Friend | On and Off-premises |
| TV | Occasional | Homeowner | On-premises |
| Smartphone | Occasional | Homeowner | On and Off-premises |
| CCTV Camera | Continuous | Homeowner | On-premises |

The goal was to understand how different devices interact with the network and identify which assets may contain sensitive information or introduce security risks.

---

## Asset Sensitivity Classification

I evaluated each asset based on the information it may contain, its access requirements, and the potential impact of unauthorized access.

Four sensitivity levels were used:

| Classification | Access Designation |
|---|---|
| Restricted | Need-to-know |
| Confidential | Limited to specific users |
| Internal-only | Authorized internal users |
| Public | Anyone |

### Asset Classification Results

| Asset | Sensitivity | Reason |
|---|---|---|
| Network Router | Confidential | Provides network connectivity and requires restricted administrative access |
| Desktop | Restricted | May contain private information and sensitive personal data |
| Guest Smartphone | Internal-only | Connects to the home network but should have limited access to internal resources |
| TV | Internal-only | Uses network connectivity for streaming and other services |
| Smartphone | Restricted | May contain private information, credentials, and personal data |
| CCTV Camera | Confidential | May capture sensitive footage of activities inside the home |

These classifications reflect the potential sensitivity and security impact of each device within the home office scenario.

---

## Key Security Findings

### 1. Network Router Access

The network router provides connectivity for devices on the home network.

**Risk:**

Unauthorized administrative access could allow an attacker to modify network settings, disrupt connectivity, or compromise network security.

**Recommended Action:**

Restrict router administration to authorized users, use strong administrator credentials, and keep router firmware updated.

---

### 2. Sensitive Information on Personal Devices

Desktop computers and smartphones may store personal photos, account credentials, and other sensitive information.

**Risk:**

Unauthorized access could expose private information or compromise personal accounts.

**Recommended Action:**

Implement strong authentication, enable device encryption, and regularly install security updates.

---

### 3. Guest Device Access

Guest smartphones may connect to the home network without being managed by the homeowner.

**Risk:**

A compromised guest device could potentially expose other devices or resources on the same network.

**Recommended Action:**

Use a separate guest Wi-Fi network and restrict guest access to internal devices and sensitive resources.

---

### 4. CCTV Camera Privacy

CCTV cameras continuously monitor and record activities around the home.

**Risk:**

Unauthorized access could expose private video footage and reveal sensitive information about household activities.

**Recommended Action:**

Use strong authentication, update camera firmware, and restrict access to camera recordings and management interfaces.

---

## Recommendations

Based on the asset inventory and sensitivity classification, the following security improvements were identified:

1. Restrict administrative access to the network router.
2. Protect sensitive information stored on desktops and smartphones.
3. Separate guest devices from trusted internal network resources.
4. Secure CCTV camera access and recordings.
5. Regularly update device firmware and software.
6. Maintain and periodically review the asset inventory.

---

## What I Learned

This project helped me understand the importance of **asset management as a foundation of cybersecurity risk management**.

One important lesson was recognizing that:

**Asset Inventory ≠ Asset Classification**

An asset inventory identifies which devices exist within a network, while asset classification determines how sensitive those assets are and what level of protection they may require.

I also learned that devices with similar functions may require different security classifications depending on the information they store and the potential impact of unauthorized access.

For example, a smartphone used only for basic communication may have different security requirements from a smartphone containing banking credentials and other sensitive information.

This activity helped me understand the relationship between:

**Asset Identification → Asset Evaluation → Sensitivity Classification → Security Prioritization**

These steps provide a foundation for identifying risks and making informed decisions about protecting information assets.

---

## Skills Practiced

- IT Asset Management
- Asset Inventory Documentation
- Information Sensitivity Classification
- Basic Risk Assessment
- Access Control
- Least Privilege
- Confidentiality, Integrity, and Availability (CIA Triad)
- Security Risk Identification
- Security Documentation

---

## Project Context

This project was completed as part of the **Google Cybersecurity Professional Certificate**.

The activity used a home office network scenario to practice identifying assets, documenting their characteristics, and assigning sensitivity classifications.

The project demonstrates the application of foundational cybersecurity asset management and risk assessment concepts in a practical scenario.
