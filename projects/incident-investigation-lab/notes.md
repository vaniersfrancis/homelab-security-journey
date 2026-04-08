# Incident Investigation Lab

## Objective
Investigate a Linux system for suspicious activity by checking processes, users, logs, and listening ports.

## System
Hostname: ubuntu-sec-lab
Date: Tue Apr 7 09:53:22 PM EDT 2026

## Evidence Collected
- Reviewed a background process using `ps aux | grep sleep`
- Checked active users with `who` and `w`
- Reviewed login history with `last -a | head`
- Checked auth logs with `grep` against `/var/log/auth.log`
- Reviewed listening ports with `ss -tulnp`
- Identified services using `sudo ss -tulnp`

## Key Findings
- A test background process was created and later completed normally
- User session activity was visible on the system
- Auth logs showed `sudo` usage and a session opened for the `attacker` user
- Listening ports were tied to normal system services such as `avahi-daemon`, `systemd-resolve`, and `cupsd`
- No obvious malicious network listener was identified during the lab

## Skills Practiced
- Process review
- User/session review
- Authentication log analysis
- Basic network/service investigation
- Evidence collection and documentation

## Interview Takeaway
I completed a Linux incident investigation lab where I reviewed processes, user sessions, authentication logs, and listening services to document system activity and identify whether anything looked suspicious.
