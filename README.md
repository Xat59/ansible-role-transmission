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
| **transmission_rpc_enabled** | | true | **true** or **false** |
| **transmission_rpc_username** | | xat | |
| **transmission_rpc_password** | | xat | |
| **transmission_alt_speed_down** | | 64 | |
| **transmission_alt_speed_up** | | 32 | |
| **transmission_speed_limit_down_enabled** | | false | **true** or **false** |
| **transmission_speed_limit_up_enabled** | | true | **true** or **false** |
| **transmission_speed_limit_down** | | 9216 | |
| **transmission_speed_limit_up** | | 3072 | |
| **transmission_dockerhost_published_rpc_port** | | 9091 | |
| **transmission_dockerhost_volume_config** | | /home/docker/etc/transmission | |
| **transmission_dockerhost_volume_download** | | /home/docker/var/transmission/Downloads | |
| **transmission_dockerhost_env_timezone** | | 'Europe/Paris' | List available here : https://en.wikipedia.org/wiki/List_of_tz_database_time_zones |
