# zabbix-misp

Zabbix template for MISP monitoring

## Installation
1. Import template & value mappings (`template.xml`).
2. Add "MISP" template to your hosts / groups.
2. Install `zabbix_misp.sh` script:
```
cp zabbix_misp.sh /usr/local/bin/zabbix_misp.sh
chmod a+rx /usr/local/bin/zabbix_misp.sh
```
4. Allow zabbix user to run `zabbix_misp.sh` as root
```
cp sudoers /etc/sudoers.d/zabbix-misp
```
5. Add MISP specific *UserParameter*s to zabbix-agent:
```
cp misp.conf /etc/zabbix/zabbix_agentd.d/
```
6. Install dependencies (sudo, jq, ...)

### Requirements
 - zabbix 4.0 or newer
 - MISP 2.4.118 or newer
 - jq installed on your MISP server
