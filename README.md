# Emin Yeromian

**CompTIA CySA+ · Security+**

I’m building practical experience in security operations through a Raspberry Pi home lab and a guided Azure honeypot project. This portfolio covers what I’ve been working on, including the parts that took more than one attempt.

## Projects

### Raspberry Pi security monitoring lab

I started with one Raspberry Pi running Kali and Wazuh. As the plan changed, I split the setup into a dedicated Ubuntu monitoring hub and a separate Kali workstation. I wanted the hub to stay home and collect logs while keeping the workstation available for other lab work.

The monitoring setup brings together Wazuh, Suricata, Zeek, and Pi-hole. The hub moved from microSD to NVMe storage and uses mirrored network traffic, with separate interfaces for capture and management.

My September project notes record a test alert reaching Wazuh. They also cover the changes to the original plan and the troubleshooting behind them. At that review, workstation recovery and some alert tuning were still open.

### Azure honeypot investigation

A guided cyber range project focused on MySQL activity on a Windows host in Azure. The case study follows database sessions containing destructive SQL statements and ransom-note activity, using query logs and Defender for Endpoint exports.

The report separates what the evidence shows from what remains uncertain. A stored ransom note supports an extortion finding; it does not, by itself, prove data theft. The available Windows logons also do not establish an RDP compromise.

## Tools I’m working with

- **Home lab:** Linux, Wazuh, Suricata, Zeek, Pi-hole
- **Azure lab and study:** Microsoft Sentinel, Defender for Endpoint, KQL, MySQL logs

## Certifications

- CompTIA Cybersecurity Analyst (CySA+)
- CompTIA Security+
- Google Cybersecurity Certificate

## Contact

[Connect with me on LinkedIn](https://www.linkedin.com/in/eminyeromian/). Project summaries with private details removed are available on request.
