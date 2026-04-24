# Homelab Security Journey

## Overview
This repository documents my hands-on homelab journey as I build practical experience in IT, Linux, system administration, and cybersecurity. The lab is focused on learning by doing through structured projects covering process monitoring, file permissions, authentication log analysis, incident investigation, and SIEM-based detection with Splunk.

---

## Screenshots

### System Monitoring
![System Monitor](https://raw.githubusercontent.com/vaniersfrancis/homelab-security-journey/main/projects/system-monitor-lab/screenshots/htop.png)

### Splunk Log Analysis
![Splunk Dashboard](https://raw.githubusercontent.com/vaniersfrancis/homelab-security-journey/main/projects/splunk-log-analysis-lab/screenshots/Screenshot%20from%202026-04-13%2016-40-48.png)

---

## Featured Lab Projects

# Cybersecurity Homelab – Attack Detection & SIEM Monitoring

This project demonstrates a hands-on cybersecurity lab focused on detecting and analyzing attack activity using a Cowrie SSH honeypot and Splunk SIEM.

## Key Features
- Deployed Cowrie SSH honeypot to capture brute-force login attempts
- Ingested logs into Splunk SIEM for analysis
- Built detection queries to extract attacker IPs, usernames, and passwords
- Created a monitoring dashboard to visualize attack patterns
- Implemented alerting to detect repeated authentication attempts

## Technologies Used
- Ubuntu Linux
- Splunk SIEM
- Cowrie Honeypot
- VirtualBox

## Skills Demonstrated
- Log Analysis
- Threat Detection
- SIEM Monitoring
- Linux Administration

### System Monitor Lab
Used Linux tools such as `htop`, `ps`, `grep`, `sleep`, and `kill` to observe active processes, identify running tasks, and manage background activity.

### File Permissions & Access Control Lab
Used `chmod` and a separate test user to practice least privilege, file hardening, and unauthorized access prevention in Linux.

### Log Analysis Lab
Reviewed `/var/log/auth.log` to identify session activity, `sudo` usage, and user-switch events, building a basic understanding of authentication monitoring and log-based investigation.

### Incident Investigation Lab
Investigated simulated suspicious activity by reviewing Linux processes, user sessions, authentication logs, and system activity to collect evidence and document findings.

### Splunk Log Analysis Lab
Installed Splunk Enterprise on Ubuntu, configured live monitoring of authentication logs, and ingested `/var/log/auth.log` into a SIEM. Created alerts to detect attacker activity and brute force attempts, and built dashboards to visualize failed login trends and system activity.

---

## Tools & Technologies
- Ubuntu Linux
- VirtualBox
- Splunk Enterprise (SIEM, alerts, dashboards)
- Git
- GitHub
- Linux Command Line
- Authentication Logs (`/var/log/auth.log`)
- Process Monitoring Tools (`htop`, `ps`, `grep`, `kill`)
- Networking / Service Review (`ss`)

---

## Skills Gained
- Linux system navigation and administration
- Process monitoring and management
- File permissions and access control
- Authentication log analysis
- Incident investigation and timeline reconstruction
- SIEM usage with Splunk
- Alert creation and detection logic
- Dashboard visualization
- Git and GitHub project documentation

---

## Challenges & Resolutions

### Splunk Not Detecting New Logs
**Issue:** After uploading `auth.log`, new terminal activity was not appearing in Splunk and alerts were not triggering.

**Cause:** Logs were uploaded as a static file instead of being monitored in real time.

**Resolution:** Configured Splunk to monitor `/var/log/auth.log` directly, enabling live log ingestion and real-time detection.

---

### Alerts Not Triggering
**Issue:** Alerts were not triggering despite correct search queries.

**Cause:** Time range did not include the timestamps of the ingested logs.

**Resolution:** Adjusted alert time range and later resolved fully by enabling live log monitoring so alerts could trigger on new events.

---

### Failed Login Simulation Not Working
**Issue:** Attempted to simulate failed logins using a non-existent user, which did not generate proper authentication failure logs.

**Cause:** The system rejected the user before authentication occurred.

**Resolution:** Used a valid user account with incorrect passwords to generate real failed login events for detection.

---

### Understanding SIEM Data Flow
**Issue:** Initial confusion between terminal activity and what Splunk was actually ingesting.

**Cause:** Misunderstanding the difference between system logs and user commands.

**Resolution:** Learned that SIEM tools monitor log sources (e.g., `/var/log/auth.log`), not the terminal itself, and adjusted data ingestion approach accordingly.

---

## Current Focus
- Strengthening Linux and cybersecurity fundamentals
- Building SIEM and detection skills with Splunk
- Practicing blue-team style investigation workflows
- Preparing for CompTIA Security+ (SY0-701)
