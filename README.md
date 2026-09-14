# Emin Yeromian

**CompTIA CySA+ · Security+**

I’m building practical experience in security operations through a Raspberry Pi home lab and an Azure honeypot lab. This portfolio covers what I’ve been working on, including the parts that took more than one attempt.

## Projects

### Raspberry Pi security monitoring lab

DEF CON 34 sparked my curiosity and pushed me to build a lab of my own. That led to a trip to Micro Center and a setup I kept changing as I learned. My goal for the next DEF CON is to get more hands-on with CTFs.

I started with one Raspberry Pi running Kali and Wazuh. I wanted a portable Kali device, but I also needed monitoring that could stay home and keep collecting logs. The build changed as those two jobs became clearer.

| Problem | What I changed |
| --- | --- |
| One Pi was doing both workstation and monitoring work | Split it into a dedicated Ubuntu monitoring hub and a separate Kali Pi |
| Constant log and index writes raised concerns about SD-card wear and storage performance | Moved to NVMe storage |
| The storage clone left the hub's boot partitions ambiguous | Used unique partition IDs and checked that the hub booted with the SD card removed |
| The capture adapter did not appear in Linux | Traced the problem to its USB connection and corrected the cabling |

The hub runs Wazuh, Suricata, Zeek, and Pi-hole, with separate capture and management interfaces. My September project log records network events reaching Wazuh and a controlled Windows process test appearing in its dashboard.

The portable Kali idea has evolved too. Kali now runs from NVMe, connected to my switch, and I access it over SSH without a display.

### Azure honeypot lab

I built a Windows VM in Azure and populated MySQL with fake corporate data. To observe hostile activity, I deliberately disabled Windows Firewall and configured the network security group (NSG) to allow all inbound traffic.

I used KQL to investigate MySQL queries and Windows events. The logs captured destructive SQL targeting the lab data and repeated ransom-note activity. A later sequence targeted an existing note table before inserting another note. The timing suggested automation, but the number of attackers remains uncertain.

For containment, I removed the allow-all inbound NSG rule. I also re-enabled Windows Firewall, changed the weak administrator password, and disabled the Guest account. My lab notes record isolation through Defender for Endpoint. The case study covers the build, investigation, response steps, and what the evidence could establish.

## Tools I’m working with

- **Home lab:** Linux, Wazuh, Suricata, Zeek, Pi-hole
- **Azure lab and study:** Microsoft Sentinel, Defender for Endpoint, KQL, MySQL logs

## Certifications

- CompTIA Cybersecurity Analyst (CySA+)
- CompTIA Security+
- Google Cybersecurity Certificate

## Contact

[Connect with me on LinkedIn](https://www.linkedin.com/in/eminyeromian/). Project summaries with private details removed are available on request.
