# Network Static configuration using Netplan (Ubuntu)

## 1. Stop and disable the Network Manager

`sudo systemctl stop NetworkManager`  
`sudo systemctl disable NetworkManager`  
`sudo systemctl status NetworkManager`  
`sudo systemctl is-enabled NetworkManager`

## 2. Create a YAML file in /etc/netplan

network:

<pre>
version: 2
renderer: networkd
ethernets:
&nbsp;&nbsp;enp0s3:
&nbsp;&nbsp;&nbsp;&nbsp;dhcp4: false
  &nbsp;&nbsp;&nbsp;&nbsp;addresses: 
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- 192.168.0.20/24
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;gateway4: "192.168.0.1"
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;nameservers:
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;addresses: 
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- "8.8.8.8" 
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- "8.8.4.4"
</pre>

## 3. Apply the new config

`sudo netplan apply`

## 4. Check the configuration

`ifconfig`  
`route -a`
