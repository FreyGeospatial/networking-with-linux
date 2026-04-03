# networking-with-linux

## resources:
- [Installing Debian Server](https://www.youtube.com/watch?v=KoGK19GPIYg&t=840s)

## Configuring a NAT
- NAT = network address translation
- its used to allow communication from one network to another, including from host machine to virtual box VM
- with virtual box, by default the VM can connect to the internet through a NAT and to the host VM through a NAT. But it CANNOT (without setting up a NAT Network) connect to other VMs
- this NAT network can be created within virtual box settings UI

![alt text](image.png)

## SSH

- SSH = secure shell
- used to control a remote system from the command line
– you can install ssh if it isnt already installed using `apt install openssh-server`.
- virtual box adds complexity to ssh connections from the host to vm, so we need to use port forwarding

`ifconfig` stands for interface configuration. It displays information about your
  network interfaces, including:

  - Interface names — e.g., en0 (Wi-Fi), lo0 (loopback), eth0 (ethernet)
  - IP addresses — both IPv4 (inet) and IPv6 (inet6)
  - MAC address — (ether)
  - Status — whether the interface is up or down

  It's the macOS/older Unix equivalent of `ip a` on Linux.


Ater getting the ip address of the vm, set up port forwarding on virtualbox.

host ip should be 127.0.0.1
host port could be anything
guest ip is the ip address of the vm
guest port is 22 which is the default for ssh on any machine

ssh into it using: `ssh sysadmin@<ip> where in a port forwarding case is the localhost ip. You should add the port option in this case as wel: `-p <host port specified>`