# SOC-monitoring-lab
Splunk Home SOC: Linux Authentication and Network Threat Monitoring Lab

## Work in Progress
This project is currently in progress and being expanded.

## Overview
This project is a hands-on Splunk home lab built on Ubuntu in VMware Workstation to practice security monitoring, log analysis, and basic detection engineering. The goal of the project is to ingest Linux authentication and firewall logs into Splunk, build searches and dashboards, and detect suspicious activity such as SSH brute-force attempts, failed sudo activity, and blocked network traffic.

## Why I Built This Project
I wanted to strengthen my hands-on SIEM and security monitoring skills by building a small but practical Splunk project that aligns with my background in network security and enterprise support. This lab helped me apply Linux, log analysis, and troubleshooting skills in a way that is easy to demonstrate on GitHub and LinkedIn.

## Lab environment
- Host system: Intel i7, 32 GB RAM,2 TB storage
- VMware Workstation 16 Pro
- Guest OS: Ubuntu (24.04.4 LTS)
- SIEM platform: Splunk Enterprise 10.2.0(Free version)

## Project Objective
- Install and configure Splunk on Ubuntu
- Ingest Linux authentication and friewall logs
- Validate log ingestion and basic searches
- Build dashboards for authentication and network monitoring
- Expand the lab with Microsoft Azure and Microsoft Sentinel

## Installation steps

### Download Splunk Enterprise

Update Ubuntu and install Splunk Enterprise package(FREE)
>wget -O splunk.tgz "https://download.splunk.com/products/splunk/releases/10.2.0/linux/splunk-10.2.0-d749cb17ea65-linux-amd64.tgz"

### Extract the package
>tar -xvzf splunk.tgz
>cd splunk/bin

### Start Splunk and accept the license
>sudo ./splunk start --accept-license
>sudo /opt/splunk/bin/splunk start --accept-license --run-as-root

### Run Splunk as a dedicated user
sudo useradd -m splunk
sudo -u splunk /opt/splunk/bin/splunk start --accept-license

### Log Sources

<img width="1024" height="559" alt="image" src="https://github.com/user-attachments/assets/68c0d625-234d-478c-b8a1-b2ab6678f1dd" />

 
# Grant read permissions on the target log files to that group
sudo chmod 640 /var/log/auth.log /var/log/ufw.log /var/log/syslog

# Restart Splunk to apply the group changes
sudo -u splunk /opt/splunk/bin/splunk restart        
 
- /var/log/ufw.log
- /var/log/auth.log
- /var/log/syslog

## Current State

This project is currently in progress.

- Splunk is ingesting Ubuntu UFW and Linux security logs from a local VM.
- The lab is running on Ubuntu in a local virtualized environment.
- Current focus is validating log ingestion, basic searches, and dashboard development.
- Next step is expanding the lab with Microsoft Azure and Microsoft Sentinel.
