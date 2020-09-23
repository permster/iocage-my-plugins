# iocage-my-plugins
Plugin manifest files for iocage.

## Prerequisites
A \*BSD system with the iocage jailmanager.

## Installing Plugins
Download a plugin manifest file to your local file system.
```
fetch https://raw.githubusercontent.com/permster/iocage-my-plugins/master/lidarr.json
```
Install the plugin using static IP or DHCP.

* Using static IP.  Adjust host interface and IP address as needed.
```
iocage fetch --plugin-name plugin_name.json -n jail_name ip4_addr="re0|192.168.0.100"
```
* Using DHCP.
```
iocage fetch --plugin-name plugin_name.json -n jail_name dhcp=on vnet=on bpf=yes
```