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
```
$ git clone https://github.com/Xat59/ansible-role-transmission
$ cd ansible-role-transmission
$ ansible-galaxy install -p roles/ mongrelion.docker
```

## Variables
| Name | Description | Default value | Choices |
|------|-------------|---------------|---------|
| **transmission_rpc_enabled** | Enable or disable web interface | true | **true** or **false** |
| **transmission_rpc_username** | Specify the web interface username | xat | |
| **transmission_rpc_password** | Specify the web interface password | xat | |
| **transmission_alt_speed_down** | Configure the alternative download bandwidth limit (in KB/s), when "Turtle mode" is enabled | 64 | |
| **transmission_alt_speed_up** | Configure the alternative upload bandwidth limit (in KB/s), when "Turtle mode" is enabled | 32 | |
| **transmission_speed_limit_down_enabled** | Configure if the download bandwidth is limited in "normal" mode | false | **true** or **false** |
| **transmission_speed_limit_up_enabled** | Configure if the upload bandwidth is limited in "normal" mode | true | **true** or **false** |
| **transmission_speed_limit_down** | If transmission_speed_limit_down_enabled is set to 'True', specify the download bandwidth limit (in KB/s) | 9216 | |
| **transmission_speed_limit_up** | If transmission_speed_limit_up_enabled is set to 'True', specify the upload bandwidth limit (in KB/s) | 3072 | |
| **transmission_dockerhost_published_rpc_port** | Define the web interface port number | 9091 | |
| **transmission_dockerhost_volume_config** | Define the transmission configuration path | /home/docker/etc/transmission | |
| **transmission_dockerhost_volume_download** | Define the transmission download path | /home/docker/var/transmission/Downloads | |
| **transmission_dockerhost_env_timezone** | Define the transmission timezone | 'Europe/Paris' | List available here : https://en.wikipedia.org/wiki/List_of_tz_database_time_zones |
