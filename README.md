# Find the Bad: Order Form
This lab contains malicious activity for you to identity that was captured in log files. It should only require the installation of Docker and Docker Compose. 

## Disclaimer
This lab is based on real data containing actual malicious indicators. If you attempt to do things such as find and run files, or visit network entities that occur in these logs, you do so at your own risk.

## Setup
1) Download and install [Docker](https://www.docker.com/get-started).
2) Download and install [Docker Compose](https://docs.docker.com/compose/install/) (On Windows Docker Compose should be bundled with the Docker installer, so this step shouldn't be required).
3) Download or clone this repository.
4) Open up a command prompt, make your way to this repository folder on your local machine and run `docker-compose up`.
5) When `docker-compose up` is finished bringing the containers up, open a browser and navigate to `http://localhost:5601` to access the Kibana instance.

## The Lab
This lab is built around using Kibana for identifying and investigating signs of a compromise. The `VT Hunting` Dashboard should provide you the information you need to get started.

### Questions
1) What is the name of the malicious file that has been flagged by VirusTotal?
2) What was the original source of this program and who was it run by, at what time, and on what computer?
3) What persistence mechanism was used by this malware?
4) What other files were created?
5) What typically non-malicious process does this malware appear to abuse? How can you tell?

### Useful Links
- [VirusTotal](https://www.virustotal.com/gui/home/upload)
- [Sysmon Events List](https://docs.microsoft.com/en-ca/sysinternals/downloads/sysmon#events)
- [Sysmon Event ID 15](https://docs.microsoft.com/en-us/sysinternals/downloads/sysmon#event-id-15-filecreatestreamhash)
- [Kibana Query Language](https://www.elastic.co/guide/en/kibana/current/kuery-query.html)
- [MITRE - ATT&CK - Boot or Logon Autostart Execution: Registry Run Keys / Startup Folder](https://attack.mitre.org/techniques/T1547/001/)

### Solution
Available [here](https://findthebad.com/order-form/).