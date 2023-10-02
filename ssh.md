# OpenSSH

## 1. Installing OpenSSH (client and server)

### Ubuntu

`sudo apt update && sudo apt install openssh-server openssh-client`

### CentOS

`sudo dnf install openssh-server openssh-clients`

### connecting to the server

_Ex: ssh -p 2267 john@192.168.0.100_  
`ssh -p 22 username@server_ip`  
`ssh -p 22 -l username server_ip`  
_verbose_  
`ssh -v -p 22 username@server_ip`

## 2. Controlling the SSHd daemon

### checking its status

_Ubuntu_  
`sudo systemctl status ssh`  
_Centos_  
`sudo systemctl status sshd`

## stopping the daemon

_Ubuntu_  
`sudo systemctl stop ssh`  
`sudo systemctl stop sshd`

### restarting the daemon

_Ubuntu_  
`sudo systemctl restart ssh`  
_Centos_  
`sudo systemctl restart sshd`

### enabling at boot time

_Ubuntu_  
`sudo systemctl enable ssh`  
_Centos_
`sudo systemctl enable sshd`

_Ubuntu_  
`sudo systemctl is-enabled ssh`  
_Centos_  
`sudo systemctl is-enabled sshd`

## 3. Securing the SSHd daemon

### change the configuration file (/etc/ssh/sshd_config) and then restart the server

`man sshd_config`

a) Change the port

  <pre>Port 2278</pre>

b) Disable direct root login

  <pre>PermitRootLogin no</pre>

c) Limit Users’ SSH access

  <pre>AllowUsers stud u1 u2 john</pre>

d) Filter SSH access at the firewall level (iptables)

e) Activate Public Key Authentication and Disable Password Authentication

f) Use only SSH Protocol version 2

g) Other configurations:

  <pre>`ClientAliveInterval 300`  
  `ClientAliveCountMax 0`  
  `MaxAuthTries 2`  
  `MaxStartUps 3`  
  `LoginGraceTime 20`  
  </pre>
