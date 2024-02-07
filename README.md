# Suricata Totorial
Tutorial to configurate and deploy the Suricata IDS.

## Introduction

Suricata is an open source signature-based IDS.

* **Host-based intrusion detection system (HIDS):** an application that monitors the activity of the host on which it’s installed.
* **Network-based intrusion detection system (NIDS):** an application that collects and monitors network traffic and network data. It works as sniffer.

### Suricata features
There are three main ways Suricata can be used:
* **Intrusion detection system (IDS):** As a network-based IDS, Suricata can monitor network traffic and alert on suspicious activities and intrusions. Suricata can also be set up as a host-based IDS to monitor the system and network activities of a single host like a computer.
* **Intrusion prevention system (IPS):** Suricata can also function as an intrusion prevention system (IPS) to detect and block malicious activity and traffic. Running Suricata in IPS mode requires additional configuration such as enabling IPS mode.
* **Network security monitoring (NSM):** In this mode, Suricata helps keep networks safe by producing and saving relevant network logs. Suricata can analyze live network traffic, existing packet capture files, and create and save full or conditional packet captures. This can be useful for forensics, incident response, and for testing signatures. For example, you can trigger an alert and capture the live network traffic to generate traffic logs, which you can then analyze to refine detection signatures.

## Suricata in Linux.

### Instalation
1. ```sudo apt update & sudo apt upgrade```
2. ```sudo apt install suricata```

### Configuration
* **/etc/suricata/suricata.yaml**: is the configuration file. Here, you can set the home network, internet adapter or default rules

### Detection Rules:
Rules or signatures are used to identify specific patterns, behavior, and conditions of network traffic that might indicate malicious activity.

These can be found in **/etc/suricata/rules/**:

### Running Suricata

#### Output log files
* **Directory:** /var/log/suricata/

**Log Format:** EVE JSON - Extensible Event Format JavaScrip Object Notation.
**Suricata log types:**
* **Alert logs:** usually this is the output of signatures which have triggered an alert. For example, a signature that detects suspicious traffic across the network.
* **Network telemetry logs:** information about network traffic flows, it is not always security relevant, it’s simply recording what’s happening on a network, such as a connection being made to a specific port.

