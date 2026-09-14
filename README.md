# Emin Yeromian

**CompTIA CySA+ · Security+**

I’m building practical experience in security operations through a Raspberry Pi home lab and an Azure honeypot lab. This portfolio covers what I’ve been working on, including the parts that took more than one attempt.

## Projects

### Raspberry Pi security monitoring lab

DEF CON 34 sparked my curiosity and pushed me to build a lab of my own. That led to a trip to Micro Center and a setup I kept changing as I learned. My goal for the next DEF CON is to get more hands-on with CTFs.

I started with one Raspberry Pi running Kali and Wazuh. As the plan changed, I split the setup into a dedicated Ubuntu monitoring hub and a separate Kali workstation. I wanted the hub to stay home and collect logs while keeping the workstation available for other lab work.

The monitoring setup brings together Wazuh, Suricata, Zeek, and Pi-hole. The hub moved from microSD to NVMe storage and uses mirrored network traffic, with separate interfaces for capture and management.

My September project notes record a test alert reaching Wazuh. They also cover the changes to the original plan and the troubleshooting behind them. At that review, workstation recovery and some alert tuning were still open.

### Azure honeypot lab

I built a Windows VM in Azure and populated MySQL with fake corporate data. To observe hostile activity, I deliberately disabled Windows Firewall and configured the network security group (NSG) to allow all inbound traffic.

I used KQL to investigate MySQL queries and Windows events. The logs captured destructive SQL targeting the lab data and repeated ransom-note activity. A later sequence targeted an existing note table before inserting another note. The timing suggested automation, but the number of attackers remains uncertain.

For containment, I removed the allow-all inbound NSG rule. My lab notes also record isolation through Defender for Endpoint. The case study covers the build, investigation, containment steps, and what the evidence could establish.

## Tools I’m working with

- **Home lab:** Linux, Wazuh, Suricata, Zeek, Pi-hole
- **Azure lab and study:** Microsoft Sentinel, Defender for Endpoint, KQL, MySQL logs

## Certifications

- CompTIA Cybersecurity Analyst (CySA+)
- CompTIA Security+
- Google Cybersecurity Certificate

## Contact

[Connect with me on LinkedIn](https://www.linkedin.com/in/eminyeromian/). Project summaries with private details removed are available on request.
