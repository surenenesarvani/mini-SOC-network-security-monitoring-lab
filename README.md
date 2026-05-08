# SOC-monitoring-lab
Splunk Home SOC: Linux Authentication and Network Threat Monitoring Lab

## Overview
This project is a hands-on Splunk home lab built on Ubuntu in VMware Workstation to practice security monitoring, log analysis, and basic detection engineering. The goal of the project is to ingest Linux authentication and firewall logs into Splunk, build searches and dashboards, and detect suspicious activity such as SSH brute-force attempts, failed sudo activity, and blocked network traffic.

## Why I Built This Project
I wanted to strengthen my hands-on SIEM and security monitoring skills by building a small but practical Splunk project that aligns with my background in network security and enterprise support. This lab helped me apply Linux, log analysis, and troubleshooting skills in a way that is easy to demonstrate on GitHub and LinkedIn.

## Lab environment
- Host system: Intel i7, 32 GB RAM,2 TB storage
- VMware Workstation 16 Pro
- Guest OS: Ubuntu (24.04.4 LTS)
- SIEM platform: Splunk Enterprise 10.2.0(Free version)

# Project Objective
- Install and configure Splunk on Ubuntu
- Ingest Linux authentication and friewall logs


# Installation steps
Update Ubuntu and install Splunk Enterprise package(FREE)

>wget -O splunk.tgz "https://download.splunk.com/products/splunk/releases/10.2.0/linux/splunk-10.2.0-d749cb17ea65-linux-amd64.tgz"

>tar -xvzf splunk.tgz
>cd splunk/bin

>sudo ./splunk start --accept-license
>sudo /opt/splunk/bin/splunk start --accept-license --run-as-root

sudo useradd -m splunk
sudo -u splunk /opt/splunk/bin/splunk start --accept-license
