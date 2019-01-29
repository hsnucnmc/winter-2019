Author: @cnmc25th

# FreeBSD Installation

# Build and Install Custom Kernel

create vm
general
vm id 自訂
name  自訂

OS
iso image freebsd 12
type other

CPU
core 2

Memory
1G

沒打都預設
Distribution select
doc、lib32、pots、src

選IPv4而非IPv6

時區自己讀英文

System Configuration
sshd、ntpd

創帳號
Login group is asample. Invite asample into other groups?  wheel
Shell tcsh

(之後裝某個東西時需要額外設hostname)




重灌
Opinions
Boot oder
edit
boot device 1 CD-Rom
boot device 2 Disk 'ide0'
