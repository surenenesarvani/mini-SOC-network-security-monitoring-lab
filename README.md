# mini-SOC-network-security-monitoring-lab
Splunk Home SOC: Linux Authentication and Network Threat Monitoring Lab

# phase 1 Setup
Update Ubuntu and install Splunk Enterprise package(FREE)

>wget -O splunk.tgz "https://download.splunk.com/products/splunk/releases/10.2.0/linux/splunk-10.2.0-d749cb17ea65-linux-amd64.tgz"

>tar -xvzf splunk.tgz
>cd splunk/bin

>sudo ./splunk start --accept-license
>sudo /opt/splunk/bin/splunk start --accept-license --run-as-root

sudo useradd -m splunk
sudo -u splunk /opt/splunk/bin/splunk start --accept-license
