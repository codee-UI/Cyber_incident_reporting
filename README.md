# Cybersecurity Incident Report: DNS & ICMP Network Traffic Analysis

## Overview

This repository documents a cybersecurity network traffic analysis exercise using **tcpdump** to investigate a website connectivity issue.

The objective was to identify:

- Which network protocols were involved
- Which service was affected
- What the packet capture revealed
- The likely cause of the incident
- Appropriate next troubleshooting steps

The investigation focused on **DNS traffic over UDP** and **ICMP error responses**.

---

## Scenario

Users reported that they were unable to access:

`www.yummyrecipesforme.com`

When attempting to load the website, the browser returned:

`destination port unreachable`

To investigate the issue, network traffic was captured using **tcpdump**.

The browser attempted to resolve the website's domain name by sending a DNS query to the DNS server.

Instead of receiving a valid DNS response, the client received an ICMP error indicating:

`udp port 53 unreachable`

---

## Network Traffic Summary

The packet capture showed repeated communication between:

- **Client IP:** `192.51.100.15`
- **DNS Server IP:** `203.0.113.2`

The client attempted to send DNS queries using UDP.

The DNS server responded with ICMP error messages instead of valid DNS responses.

---

## Protocols Identified

| Protocol | Purpose | Role in Incident |
|---|---|---|
| UDP | Connectionless transport protocol | Used to send DNS requests |
| DNS | Resolves domain names to IP addresses | Failed to respond on port 53 |
| ICMP | Reports network errors and reachability issues | Reported destination port unreachable |
| HTTPS | Secure web communication | Could not proceed because DNS resolution failed |

---

## Port Identified

The affected port was:

`UDP Port 53`

Port 53 is commonly used by the **Domain Name System (DNS)**.

The ICMP response:

`udp port 53 unreachable`

indicates that the DNS request could not be delivered to an active service listening on UDP port 53.

---

## Part 1: Problem Summary

### UDP Analysis

The UDP traffic indicates that the client computer attempted to send DNS queries to the DNS server at:

`203.0.113.2`

The requests were intended to resolve the IP address associated with:

`www.yummyrecipesforme.com`

### ICMP Response

Instead of a DNS response, the client received an ICMP error:

`udp port 53 unreachable`

This indicates that the UDP packet reached the destination system, but no service was available to process the request on port 53.

### Most Likely Immediate Issue

The DNS service was unavailable or not listening on UDP port 53.

Because DNS resolution failed, the browser could not retrieve the IP address required to connect to the web server.

---

## Part 2: Incident Analysis

### Time of Incident

The packet capture shows the incident occurring at approximately:

`13:24:32`

This corresponds to approximately:

`1:24 PM`

### How the Incident Was Identified

Customers reported that the website could not be accessed.

The cybersecurity analyst reproduced the same issue and received the same destination port unreachable message.

The analyst then used tcpdump to capture and inspect the network traffic.

---

## Investigation Actions

The investigation included:

1. Attempting to access the affected website
2. Reproducing the reported error
3. Capturing network traffic using tcpdump
4. Identifying outgoing UDP DNS queries
5. Identifying incoming ICMP error messages
6. Reviewing the destination port
7. Determining that port 53 was unreachable

---

## Key Findings

The investigation identified the following:

- The client sent DNS requests using UDP.
- The destination was the DNS server at `203.0.113.2`.
- The requests targeted UDP port 53.
- No valid DNS response was returned.
- ICMP reported that UDP port 53 was unreachable.
- The same error occurred repeatedly.
- DNS resolution failed.
- The browser could not obtain the IP address of the requested website.
- The HTTPS connection could therefore not proceed.

---

## Root Cause Assessment

The available evidence indicates that the immediate problem is:

**DNS service unavailability on UDP port 53**

Possible underlying causes include:

- DNS service stopped or failed
- DNS server misconfiguration
- Firewall blocking UDP port 53
- Network access control rule preventing DNS communication
- Service listening on an incorrect interface or port
- DNS server outage

The packet capture confirms the failure of DNS communication but does not provide enough evidence to determine the exact underlying cause.

---

## Recommended Troubleshooting Steps

The following actions should be performed:

1. Verify that the DNS service is running.
2. Confirm that the DNS server is listening on UDP port 53.
3. Check firewall rules affecting UDP port 53.
4. Review DNS server configuration.
5. Inspect DNS service logs.
6. Test DNS resolution directly.
7. Confirm network connectivity between client and DNS server.
8. Restart or restore the DNS service if required.
9. Verify that normal DNS responses are returned after remediation.

---

## Incident Flow

```text
User attempts to access website
          |
          v
Browser requests DNS resolution
          |
          v
UDP DNS query sent to port 53
          |
          v
DNS server does not process request
          |
          v
ICMP error returned
"udp port 53 unreachable"
          |
          v
DNS resolution fails
          |
          v
Website IP address unavailable
          |
          v
HTTPS connection cannot proceed
```

---

## Key Technical Conclusion

The protocol producing the error message is:

**ICMP**

The affected application-layer service is:

**DNS**

The affected transport protocol is:

**UDP**

The affected port is:

**53**

The issue is therefore best summarized as:

**DNS resolution failure caused by UDP port 53 being unreachable.**

---

## Skills Demonstrated

This activity demonstrates practical understanding of:

- Network traffic analysis
- TCP/IP model
- DNS
- UDP
- ICMP
- Port analysis
- tcpdump
- Incident investigation
- Network troubleshooting
- Cybersecurity incident reporting

---

## Tools Used

- tcpdump
- Network protocol analysis
- DNS traffic inspection
- ICMP error interpretation

---

## Repository Purpose

This repository is part of a cybersecurity learning and portfolio project focused on practical network traffic analysis and incident investigation.

It demonstrates the ability to:

- Interpret packet capture data
- Identify affected protocols
- Analyze network errors
- Determine affected services
- Document findings clearly
- Recommend logical troubleshooting steps

---

## Disclaimer

This project is based on a simulated cybersecurity training scenario and is intended for educational and portfolio purposes.

It does not represent a real-world security incident.

---

## Keywords

`Cybersecurity` `Network Security` `tcpdump` `DNS` `ICMP` `UDP` `Port 53` `Network Traffic Analysis` `Incident Response` `Packet Analysis` `Network Troubleshooting`
