# ansible-role-transmission
## Description
Install and configure transmission server instance : https://transmissionbt.com/
This role uses the amazing linuxserver.io docker image : linuxserver/transmission .

Features :
 - enable/disable web interface
 - web interface authentication
 - configure download and upload limits
 - timezone configuration

## Role installation
`git clone https://github.com/Xat59/ansible-role-transmission
cd ansible-role-transmission
ansible-galaxy install -p roles/ mongrelion.docker`

## Variables
