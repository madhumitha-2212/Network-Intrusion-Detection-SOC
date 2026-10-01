# Network Intrusion Detection & SOC Monitoring

A cybersecurity project that integrates **Suricata IDS** with **Splunk SIEM** for network traffic monitoring, intrusion detection, security event analysis, and SOC dashboard visualization.

## Architecture

Kali Linux → Suricata IDS → eve.json → Splunk Universal Forwarder → Splunk Enterprise → SOC Dashboard

## Technologies

- Kali Linux
- Suricata IDS
- Splunk Enterprise
- Splunk Universal Forwarder
- Nmap
- TCP/IP Networking
- SIEM
- Network Intrusion Detection

## Key Features

- Real-time network traffic monitoring using Suricata
- Detection of suspicious network activity
- Nmap scan detection
- Custom Suricata detection rule
- JSON-based security event logging
- Forwarding Suricata events to Splunk
- Security event investigation using Splunk Search
- SOC monitoring dashboard
- Alert severity, source IP, and protocol analysis

## Custom Detection Rule

The project includes a custom Suricata rule for detecting access to the Splunk Web service:

```text
alert tcp any any -> 192.168.56.101 8000 (msg:"CUSTOM SOC Test - Access to Splunk Web"; sid:1000001; rev:1;)


```
## Testing

The system was tested using controlled Nmap scans against the Windows Splunk host. Suricata successfully detected the Nmap activity and forwarded the resulting security events to Splunk.

## Project Flow

Network Traffic -> Suricata IDS -> Security Events -> eve.json -> Splunk Universal Forwarder -> Splunk Enterprise -> SOC Monitoring Dashboard -> Security Analysis

## Note

This project was developed in a controlled virtual lab environment using Kali Linux and Windows virtual machines.
