# Splunk Log Analysis Lab

## Objective
Use Splunk to ingest and analyze Linux authentication logs to identify user activity and privileged actions.

## Environment
- Ubuntu (VirtualBox)
- Splunk Enterprise
- Linux auth.log

## Steps Performed
- Installed Splunk using .deb package
- Started Splunk and accessed web interface
- Uploaded auth.log into Splunk
- Searched logs using Splunk queries

## Key Searches
- index=main
- index=main sudo
- index=main attacker
- index=main "session opened"
- index=main "session closed"

## Key Findings
- Identified sudo activity performed by user `vanier`
- Observed privilege escalation from `vanier` to `root`
- Detected user switch to `attacker` account
- Built a timeline of attacker session (open → close)
- Determined activity was expected based on lab behavior

## Skills Practiced
- SIEM usage (Splunk)
- Log ingestion
- Event searching and filtering
- Privilege escalation analysis
- Timeline reconstruction

## Interview Takeaway
Used Splunk to ingest and analyze Linux authentication logs, identify privileged user activity, and reconstruct a timeline of events including user switching and session activity.
