# NIST Cybersecurity Framework: ICMP Flood Incident Analysis

**Category:** Network Security / Incident Response  
**Framework:** NIST Cybersecurity Framework (CSF)  
**Attack Type:** Denial-of-Service (DoS), ICMP Flood  
**Concepts:** Firewall Configuration, IDS/IPS, Network Monitoring, Incident Response

## 1. Project Overview

This project focuses on analyzing a simulated Denial-of-Service (DoS) attack against a multimedia organization using the National Institute of Standards and Technology Cybersecurity Framework (NIST CSF).

The organization experienced a network outage after an attacker exploited a misconfigured firewall to overwhelm its internal network with ICMP packets.

The objective was to investigate the incident, identify the affected systems, evaluate the security measures implemented, and develop an incident response strategy using the five NIST CSF functions presented in the exercise.

### Learning Objectives

- Understand how ICMP flood attacks disrupt network availability.
- Identify security vulnerabilities associated with firewall misconfigurations.
- Apply the NIST Cybersecurity Framework to incident analysis.
- Understand the roles of firewalls, IDS/IPS, and network monitoring.
- Develop incident response and recovery strategies.
- Practice documenting cybersecurity incidents.

## 2. Incident Scenario

A multimedia organization providing web design, graphic design, and social media marketing services experienced a network security incident.

During the attack, the organization's network services suddenly stopped responding to incoming ICMP packets.

The cybersecurity team investigated the incident and discovered that an attacker had exploited an improperly configured firewall to flood the internal network with ICMP ping requests.

The attack overwhelmed the network and resulted in approximately two hours of service disruption.

To contain the attack, the cybersecurity team blocked the malicious traffic, temporarily disabled non-critical network services, and restored critical services.

## 3. Attack Analysis

### Attack Type: ICMP Flood

An ICMP flood is a type of Denial-of-Service attack that attempts to overwhelm a target with excessive ICMP packets.

ICMP is commonly used by network diagnostic tools such as `ping` to test network connectivity.

In this scenario, the attacker exploited a firewall configuration weakness to send excessive ICMP requests into the organization's internal network.

As a result, legitimate network traffic could not access necessary resources, causing network services to become unavailable.

### Identified Vulnerability

The primary vulnerability was an improperly configured firewall that failed to adequately restrict incoming ICMP traffic.

This allowed excessive ICMP requests to reach the organization's network.

### Impact

- Approximately two hours of network service disruption.
- Internal network resources became temporarily unavailable.
- Legitimate network traffic could not access required services.
- Critical network services required restoration.

The available scenario establishes an availability incident. It does not provide evidence of data theft or confirm that the attack originated from multiple distributed sources.

## 4. Applying the NIST Cybersecurity Framework

The incident was analyzed using the five NIST CSF functions presented in the training exercise.

### 4.1 Identify

**Objective:** Identify affected systems, security vulnerabilities, and potential risks.

The cybersecurity team investigated the network infrastructure, devices, and access policies to determine the cause and scope of the incident.

The investigation identified an unusually large volume of incoming ICMP packets and an improperly configured firewall.

The attack disrupted the organization's internal network and affected access to network resources.

**Key Findings:**

- Excessive incoming ICMP traffic.
- Insufficient firewall traffic restrictions.
- Network services became unresponsive.
- Critical network resources required protection and restoration.

### 4.2 Protect

**Objective:** Implement security controls to reduce the likelihood and impact of similar attacks.

Following the investigation, the cybersecurity team implemented several security improvements.

**Security Measures:**

1. **Firewall Rate Limiting:** Restrict the rate of incoming ICMP packets to reduce the risk of network saturation.
2. **Source IP Verification:** Implement source IP filtering to help identify and restrict suspicious or spoofed traffic.
3. **IDS/IPS:** Deploy intrusion detection and prevention capabilities to identify suspicious network activity and block traffic where appropriate.
4. **Network Monitoring:** Implement monitoring software to identify abnormal network traffic patterns.

These measures provide multiple defensive layers to improve network security.

### 4.3 Detect

**Objective:** Identify suspicious activity and improve the organization's ability to detect future attacks.

The cybersecurity team implemented firewall logging, intrusion detection capabilities, and network monitoring software.

These tools can help identify abnormal traffic patterns and generate alerts when suspicious activity is detected.

**Detection Strategy:**

- Continuously monitor incoming network traffic.
- Analyze firewall logs.
- Detect unusual increases in ICMP traffic.
- Investigate suspicious network behavior.
- Generate alerts when traffic exceeds expected thresholds.

Continuous monitoring can help security teams identify attacks earlier and reduce response times.

### 4.4 Respond

**Objective:** Contain security incidents, reduce their impact, and coordinate incident response activities.

During the incident, the cybersecurity team blocked malicious ICMP traffic and temporarily stopped non-critical network services.

For future incidents, the organization should establish a documented incident response procedure.

**Incident Response Procedure:**

1. Identify and confirm suspicious network activity.
2. Analyze firewall and network monitoring logs.
3. Apply appropriate filtering or rate-limiting measures to contain malicious traffic.
4. Isolate affected systems when necessary.
5. Prioritize the availability of critical network services.
6. Notify relevant internal stakeholders.
7. Document the incident and investigate its root cause.

Following containment, the cybersecurity team should review the effectiveness of its response and update security procedures where necessary.

### 4.5 Recover

**Objective:** Restore affected systems and network services to normal operation.

During the incident, the cybersecurity team blocked incoming malicious ICMP traffic, stopped non-critical services, and restored critical network services.

**Recovery Procedure:**

1. Confirm that the malicious traffic has been blocked or sufficiently mitigated.
2. Verify that firewall configurations are functioning as intended.
3. Assess the condition of affected network systems.
4. Prioritize the restoration of critical network services.
5. Verify that restored services are functioning correctly.
6. Gradually restore non-critical network services.
7. Continue monitoring network traffic for renewed attacks.

Recovery should prioritize critical business operations while ensuring that restored systems remain protected.

## 5. Security Improvements

The incident demonstrated the importance of combining preventive security controls with continuous network monitoring and structured incident response procedures.

| Security Measure | Purpose |
|---|---|
| Firewall rate limiting | Restrict excessive ICMP traffic |
| Source IP verification | Help identify and filter suspicious traffic |
| IDS/IPS | Detect and potentially block malicious activity |
| Network monitoring | Identify abnormal traffic patterns |
| Incident response procedures | Improve containment and recovery |

These controls should be regularly reviewed and adjusted as network infrastructure and security requirements change.

## 6. Key Takeaways

**1. Network availability is a critical security objective.**

DoS attacks can disrupt business operations even without compromising confidential information.

**2. Firewall configuration is essential.**

Deploying a firewall alone does not guarantee protection. Firewall rules must be configured and maintained according to organizational requirements.

**3. Monitoring improves incident detection.**

Firewall logs, intrusion detection systems, and network monitoring tools provide valuable information for identifying suspicious activity.

**4. Incident response requires preparation.**

Documented procedures help security teams contain attacks, prioritize critical services, and coordinate recovery activities.

**5. Security frameworks provide a structured approach.**

The NIST CSF helps organizations organize cybersecurity activities and continuously improve their security practices.

## 7. Reflections and Future Improvements

This exercise helped me understand how an ICMP flood can affect network availability and how the NIST Cybersecurity Framework can be applied to incident analysis.

It also demonstrated the importance of regularly reviewing firewall configurations, implementing appropriate security controls, and developing effective incident response procedures.

**Future Improvements:**

- Practice analyzing ICMP traffic using Wireshark and tcpdump.
- Study firewall rate limiting and traffic-filtering configurations.
- Explore IDS/IPS detection rules.
- Learn how network monitoring systems identify abnormal traffic.
- Investigate the differences between DoS and DDoS mitigation.
- Study the additional Govern function introduced in NIST CSF 2.0.

## Disclaimer

This project is based on a simulated cybersecurity incident from a training exercise. The findings and reported response actions are derived from the provided scenario and incident report. Additional recommendations are proposed improvements and have not been implemented or tested in a production environment.
