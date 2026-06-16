\# Wazuh Installation on Ubuntu Server Using PuTTY



\## Objective



This project demonstrates the installation of Wazuh SIEM on Ubuntu Server and remote administration using PuTTY over SSH.



\---



\## System Requirements



\* Ubuntu Server 22.04 LTS

\* 8 GB RAM

\* 4 CPU Cores

\* PuTTY

\* Internet Connection

\* Wazuh 4.13.1



\---



\## Step 1: Ubuntu Server Setup



Ubuntu Server virtual machine was started successfully.



!\[Ubuntu Login](screenshots/01\_ubuntu\_login.png)



\---



\## Step 2: Obtain IP Address



Command used:



```bash

hostname -I

```



Example output:



```text

192.168.68.104

```



Screenshot:



!\[IP Address](screenshots/02\_ip\_address.png)



\---



\## Step 3: Install SSH



Commands used:



```bash

sudo apt update

sudo apt install openssh-server -y

sudo systemctl status ssh

```



Screenshot:



!\[SSH Installation](screenshots/03\_ssh\_installation.png)



\---



\## Step 4: Connect Using PuTTY



PuTTY was configured using:



\* Host Name: 192.168.68.104

\* Port: 22

\* Connection Type: SSH



Screenshot:



!\[PuTTY Connection](screenshots/04\_putty\_connection.png)



\---



\## Step 5: Install Wazuh



Commands:



```bash

curl -sO https://packages.wazuh.com/4.13/wazuh-install.sh

chmod +x wazuh-install.sh

sudo ./wazuh-install.sh -a

```



Components installed:



\* Wazuh Indexer

\* Wazuh Manager

\* Filebeat

\* Wazuh Dashboard



\---



\## Step 6: Installation Success



Installation completed successfully.



Login credentials:



\* Username: admin

\* Password: Generated during installation



\---



\## Step 7: Access Dashboard



Open browser:



```text

https://192.168.68.104

```



Login using admin credentials.



\---



\## Conclusion



Wazuh SIEM was successfully installed on Ubuntu Server. Remote access using PuTTY was verified, and the dashboard was accessed successfully.



