# Guide
https://www.redhat.com/sysadmin/virsh-subcommands

## virsh domifaddr
'''
The domifaddr subcommand lists all the IP addresses configured for all virtual interfaces in a given VM. It's useful if the VM uses dynamic IP addresses, as it allows you to see the assigned IP address and connect to the VM:

```
# virsh domifaddr rh8-vm01 
 Name       MAC address          Protocol     Address
-------------------------------------------------------------------------------
 vnet6      52:54:00:c8:17:6e    ipv4         192.168.122.19/24
 vnet7      52:54:00:04:4d:ac    ipv4         192.168.64.210/24
```
By default, it lists the IP address leased by a DHCP server. If the hypervisor does not provide this information, you can also use the option --source agent to query the guest operating system (OS) directly via the virtualization agent. This requires a virtualization agent installed in the guest OS.
'''
