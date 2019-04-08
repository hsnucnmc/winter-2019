# DNS
## Requirements
- Setup a DNS server with BIND
  - Serve your own domain name
  - Add a MX record for your mail server
  - Add at least two record for your web server for name-based virtual host
    - For example, www.{your domain} for web page and mail.{your domain} for webmail



設定ip 
用 root 的身分編輯 /etc/rc.conf 

ifconfig_em0="inet 140.131.149.49(自己的)  netmask 255.255.255.0"

defaultrouter="140.131.149.254

leave editer,save



service netif restart

service routing restart

