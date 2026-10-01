# Splunk Configuration

This folder documents the Splunk configuration used in the Network Intrusion Detection and SOC Monitoring project.

## Configuration

- **Data Source:** Suricata `eve.json`
- **Input Method:** Splunk Universal Forwarder
- **Sourcetype:** `suricata`
- **Index:** `main`
- **Receiving Port:** `9997`
- **Log File:** `/var/log/suricata/eve.json`

## Data Flow

Kali Linux → Suricata → eve.json → Splunk Universal Forwarder → Splunk Enterprise

## Purpose

Splunk Enterprise was used to search, analyze, and visualize Suricata security alerts through a SOC dashboard.
