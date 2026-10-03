# TCP SYN Flood Attack Analysis

**Category:** Networking / Cybersecurity Incident Response  
**Project Type:** Simulated Network Security Incident  
**Tools:** Wireshark (provided TCP/HTTP logs)  
**Protocols:** TCP, HTTP, HTTPS

## 1. Project Overview

This project focuses on investigating a simulated network security incident involving a suspected TCP SYN Flood attack.

In the scenario, employees of a travel agency experienced difficulties accessing the company's website. A monitoring system detected an issue with the web server, and an investigation of network traffic revealed a large volume of incoming TCP SYN requests.

I analyzed the provided network traffic logs, identified characteristics of a potential SYN Flood attack, and examined how the attack could disrupt legitimate network connections.

## 2. Learning Objectives

- Understand the TCP three-way handshake.
- Identify normal and abnormal TCP connection patterns.
- Understand the difference between DoS and DDoS attacks.
- Recognize the characteristics of TCP SYN Flood attacks.
- Analyze network traffic to investigate service availability issues.
- Document findings and propose appropriate mitigation strategies.

## 3. Knowledge Sources

- Cybersecurity training: Network attacks and incident response
- TCP/IP networking fundamentals
- TCP three-way handshake
- Denial-of-Service (DoS) attacks
- Distributed Denial-of-Service (DDoS) attacks
- Wireshark TCP/HTTP traffic analysis

## 4. Hands-on Practice: Incident Investigation

### 4.1 Incident Scenario

Employees of a travel agency reported difficulties accessing the company's website.

An automated monitoring system detected a potential web server issue. When the security analyst attempted to access the website, the connection timed out.

An investigation using packet capture data revealed an unusually high volume of incoming TCP SYN requests.

### 4.2 Understanding the TCP Three-Way Handshake

Under normal circumstances, TCP connections are established through three steps:

1. **SYN:** The client sends a SYN packet to request a connection.
2. **SYN-ACK:** The server acknowledges the request and responds with a SYN-ACK packet.
3. **ACK:** The client sends an ACK packet to complete the connection.

A SYN Flood attack exploits this connection establishment process by generating large numbers of connection requests.

When many connections remain incomplete, they can consume server resources and interfere with legitimate connection attempts.

### 4.3 Network Traffic Analysis

The provided logs contained examples of normal TCP communication and suspicious connection activity.

**Network information:**

| Parameter | Value |
|---|---|
| Suspicious Source IP | 203.0.113.0 |
| Web Server IP | 192.0.2.1 |
| Protocol | TCP |
| Destination Port | 443 |
| Suspicious Activity | Repeated TCP SYN requests |
| Suspected Attack | TCP SYN Flood |

Normal network traffic showed clients successfully completing TCP handshakes and receiving HTTP responses.

In contrast, the suspicious traffic contained repeated connection requests originating from the same IP address.

This pattern, together with the reported service disruption, was consistent with a suspected SYN Flood attack.

### 4.4 Attack Identification

Based on the scenario and traffic patterns, I identified a potential TCP SYN Flood DoS attack.

The available evidence highlighted an individual suspicious source rather than demonstrating a distributed attack involving multiple coordinated sources.

A SYN Flood attack can prevent legitimate clients from establishing connections by overwhelming the server with connection requests.

## 5. Challenges & Troubleshooting

### Identifying Abnormal TCP Traffic

One challenge was distinguishing ordinary TCP connection attempts from potentially malicious traffic.

Examining repeated SYN packets and comparing them with normal TCP handshakes helped identify suspicious behavior.

### Understanding the Impact

Another challenge was understanding how large numbers of TCP connection attempts could disrupt the website.

This exercise helped me understand the relationship between TCP connection establishment, server resource consumption, and service availability.

## 6. Proposed Mitigation Strategies

The following actions could help investigate and mitigate similar incidents:

- Investigate and filter suspicious traffic using firewall rules.
- Review server and firewall logs to identify abnormal connection patterns.
- Consider SYN cookies to reduce resource consumption caused by incomplete TCP connections.
- Implement appropriate connection rate limiting.
- Use network monitoring and DDoS protection services where appropriate.
- Verify that legitimate users can reconnect after mitigation.

Blocking a suspicious IP address may provide temporary relief, but additional investigation is necessary to determine whether other attack sources are involved.

These are proposed strategies and were not implemented during this training exercise.

## 7. Key Takeaways

- TCP uses a three-way handshake to establish reliable connections.
- SYN Flood attacks exploit the TCP connection establishment process.
- Excessive connection attempts can disrupt legitimate access to network services.
- Comparing normal and abnormal network traffic helps identify suspicious activity.
- Network traffic analysis is an important component of cybersecurity incident response.
- Identifying the suspected attack does not automatically establish the full extent or origin of an incident.

## 8. Future Improvements

- [ ] Capture and analyze TCP traffic using Wireshark.
- [ ] Practice identifying SYN, SYN-ACK, and ACK packets.
- [ ] Investigate TCP connection states.
- [ ] Study SYN cookies and connection rate limiting.
- [ ] Compare DoS and DDoS traffic patterns.
- [ ] Conduct controlled network security experiments in an isolated lab environment.

## 9. Project Scope

This project was completed using a simulated cybersecurity scenario and provided network traffic logs.

The investigation focused on interpreting traffic patterns and documenting a suspected SYN Flood attack. No live attack was conducted, and no production network was modified.
