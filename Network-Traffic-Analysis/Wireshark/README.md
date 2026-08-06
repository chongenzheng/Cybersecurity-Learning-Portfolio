# Wireshark Network Traffic Analysis

## Learning Objectives

The goal of this lab was to learn the basic functions of Wireshark and practice capturing, filtering, and visualizing network traffic.

Through this activity, I learned how to:

- Capture live network packets
- Select the correct network interface
- Use display filters to focus on specific protocols
- Identify the default coloring rules for protocols
- Create an I/O graph for network traffic
- Recognize basic TCP, UDP, HTTP, and DNS traffic
- Use Wireshark statistics and packet details for network analysis

## Knowledge Sources

### Video Tutorial
**Master Course**

**Mastering Wireshark: The Complete Tutorial**

The tutorial introduced the main features of Wireshark, including:

- Wireshark installation and interface selection
- Packet capture and PCAP file saving
- Packet List, Packet Details, and Packet Bytes panes
- Capture filters and display filters
- Protocol-based filtering
- Coloring rules
- Wireshark profiles
- Protocol Hierarchy
- Conversations and Endpoints
- I/O Graphs
- TCP three-way handshake
- Follow TCP Stream
- Basic TCP, UDP, DHCP, and DNS analysis

## Hands-on Practice

### 1. Capturing Network Traffic

I opened Wireshark in Kali Linux and selected the active network interface.

While Wireshark was capturing packets, I opened a web browser and visited websites to generate network traffic.

After enough packets were collected, I stopped the capture for analysis.

### 2. Filtering HTTP Traffic

I used the display filter to show only HTTP packets. This filter hides all packets that do not use the HTTP protocol.

Because most modern websites use HTTPS, regular web browsing may not generate many visible HTTP packets. An unencrypted HTTP website can be used to generate HTTP traffic for testing.

### 3. Checking DCE/RPC Coloring Rules

Through Wireshark coloring rules: 
`View → Coloring Rules` to get and customize the color.

Coloring rules make it easier to recognize different protocols and unusual network activity.

### 4. Creating a Traffic Graph: 
`Statistics → I/O Graphs`
The graph displayed the amount of HTTP traffic captured over time.

### 5. Reviewing Packet Details

Wireshark separates packet information into different sections:

- Packet List Pane — shows all captured packets
- Packet Details Pane — shows protocol fields and headers
- Packet Bytes Pane — shows the raw packet data in hexadecimal and ASCII

By selecting an HTTP packet, I could inspect protocol layers such as:

- Ethernet
- Internet Protocol
- Transmission Control Protocol
- Hypertext Transfer Protocol

## Useful Wireshark Filters
- Protocol Filters
- IP Address Filter
- TCP Port Filter
- DNS Port Filter
- Combined Filter
- HTTP or HTTPS Port

## Challenges and Troubleshooting
### Challenge 1: No HTTP Packets Appeared

At first, filtering with HTTP may return few or no results.

This happens because most websites now use HTTPS. HTTPS traffic is encrypted and is typically displayed as TLS rather than HTTP.

To solve this issue, I generated traffic using a website that still supports unencrypted HTTP.

### Challenge 2: Choosing the Correct Interface

Wireshark may display several interfaces.

If the wrong interface is selected, little or no traffic will appear. I identified the active interface by checking which interface showed changing traffic activity before starting the capture.

### Challenge 3: Understanding Capture and Display Filters

Capture filters and display filters perform different tasks:

A capture filter decides which packets are collected.
A display filter hides packets after they have already been captured.

Packets excluded by a capture filter cannot be recovered from that capture. Display filters are safer for beginner analysis because the original packets remain available.

## Key Takeaways

Wireshark is a packet analysis tool that helps users understand what is happening on a network.

The most important skill is learning how to use filters. Without filters, a packet capture can contain thousands of packets, making it difficult to analyze.

I also learned that Wireshark does not automatically explain whether every packet is normal or malicious. The analyst must understand network protocols, ports, packet flags, and normal traffic behavior.

The I/O Graph, Coloring Rules, Protocol Hierarchy, Conversations, and Endpoints features can help identify traffic patterns and unusual network activity.

This lab provided practical experience with basic network traffic capture and analysis.

## Future Improvements

In future practice, I plan to:

- Practice using Follow TCP Stream
- Compare HTTP and HTTPS traffic
- Analyze DNS queries and responses
- Identify TCP reset packets
- Observe Nmap scanning traffic in Wireshark
- Practice analyzing PCAP files from cybersecurity challenges
- Learn how Wireshark is used in SOC investigations

