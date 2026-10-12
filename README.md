# Emin Yeromian

**CompTIA CySA+ · Security+**

I'm pursuing a cybersecurity degree and building hands-on experience for cybersecurity and networking roles. My projects focus on Linux, network monitoring, log analysis, and incident investigation. I also have a background in retail leadership.

## Projects

### Raspberry Pi security monitoring lab

I built an Ubuntu monitoring hub around Wazuh, Suricata, Zeek, and Pi-hole, with separate management and capture interfaces. A second Pi runs Kali from NVMe, connects to my switch, and is accessed over SSH without a display.

I started with one Pi doing both jobs. Splitting them let monitoring stay home while Kali had its own role. Along the way, I worked through storage and capture issues:

| Problem | What I changed |
| --- | --- |
| One Pi handled both Kali and monitoring | Split the work between an Ubuntu hub and a separate Kali Pi |
| Constant log and index writes raised concerns about SD-card wear and storage performance | Moved to NVMe storage |
| The storage clone left the hub's boot partitions ambiguous | Used unique partition IDs and checked that the hub booted with the SD card removed |
| The capture adapter did not appear in Linux | Traced the issue to its USB connection and corrected the cabling |

I checked DNS resolution and blocking through Pi-hole from both the hub and Kali. I also configured Wazuh to accept UniFi syslog over UDP and TCP and verified both listeners. My September project log records network events reaching Wazuh and a controlled Windows process test appearing in its dashboard. I also used a Python health-check script to check services, log freshness, alerts, and network interfaces.

[Read the home SOC walkthrough](docs/home-soc-walkthrough.md) for the layout, troubleshooting, and a repeatable Windows test procedure.

DEF CON 34 pushed me to build a lab of my own. My goal for the next DEF CON is to get more hands-on with CTFs.

### Azure honeypot lab

I built an Azure honeypot with synthetic corporate data in MySQL. I used KQL and SQL to investigate destructive database queries and ransom-note activity, and documented the incident timeline and containment.

My follow-up work included tightening inbound NSG access, re-enabling Windows Firewall, updating administrator credentials, and disabling the Guest account. My lab notes also record isolation through Defender for Endpoint.

## Tools I'm working with

- **Home lab:** Linux, Wazuh, Suricata, Zeek, Pi-hole, SSH
- **Azure lab and study:** Microsoft Sentinel, Defender for Endpoint, KQL, MySQL logs

I'm also studying for the CCNA.

## Certifications

- CompTIA Cybersecurity Analyst (CySA+)
- CompTIA Security+
- Google Cybersecurity Certificate

## Contact

[Connect with me on LinkedIn](https://www.linkedin.com/in/eminyeromian/). Project summaries with private details removed are available on request.

