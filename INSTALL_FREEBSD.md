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
(上面寫得很足夠了，基本上沒提的都預設，但就算按照正確步驟走，你也有一定機率裝不好，
像我們就遇過fstab出問題，連網卡都出事，後來我重弄一台虛擬機並重灌才解決，另一位
換了六七次的虛擬機都還是出問題，妙的是我裝沒問題的虛擬機和他網卡有問題的虛擬機是同
一台主機，為甚麼網卡還會出問題?)




重灌
Opinions
Boot oder
edit
boot device 1 CD-Rom
boot device 2 Disk 'ide0'
(重灌完後要調回原本的順序，不然你重新開機後會悲劇)
(大概是這樣)
