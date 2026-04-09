# Linux Networking: Basics and Beyond

## Outcomes:
- Configure and manage networking services and protocols (TCP/IP, DHCP, DNS) across multiple Linux distributions using both GUI and command-line tools.
- Master essential Linux networking commands and utilities: ip, ping, traceroute, dig, nmcli, SSH, SFTP, SCP, rsync.
- Build, test, and secure Linux network environments with hands-on labs, including static and dynamic IP configuration, and hostname management. 


## useful commands:

`su -` # become root user

`usermod -aG sudo <your_username>` # give sudo permissions to user

`dpkg-reconfigure console-setup` # configures screen resolution

`apt install sudo` # installs sudo

`top` # real time process monitor 
 Key shortcuts while inside top:
  - `q` — quit
  - `k` — kill a process (enter PID)
  - `M` — sort by memory usage
  - `P` — sort by CPU usage

`cat /etc/**release**` # get major/minor version of system

`id <user>` # get info and permissions info on a user

`ip a` fetches networking interfaces

`ip -br -c a` condenses network interface info to just the network interface type (`lo`, `enp3s0`,`wlp2s0` etc) status (e.g., `UP`), and the ipv4 and ipv5 addresses
    - br is for 'brief
    - c is for 'color'
