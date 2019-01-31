# Postfix 
> Setup a working SMTP server using Postfix (port 25) <br>
> https://www.freebsd.org/doc/handbook/mail-changingmta.html

Install Postfix via pkg
```
# pkg install postfix
```
go to /etc/rc.conf and add these new line
```
#sendmail
sendmail_enable="NO"
sendmail_submit_enable="NO"
sendmail_outbound_enable="NO"
sendmail_msp_queue_enable="NO"

#postfix
postfix_enable="YES"
```
Then run thess two command to stop sendmail and start postfix
```
# service sendmail stop
# service postfix start
```

# Dovecot
> Setup a working POP3 & IMAP server using Dovecot (port 110 & 143) <br>
> http://izero.pixnet.net/blog/post/17061915

install Dovecot via pkg
```
# pkg install dovecot
```
add these line into /etc/rc.con
```
#dovcot
dovecot_enable="YES"
```
now go to /usr/local/etc/dovecot/example-config and copy the config file
```
# cp dovecot.conf /usr/local/etc/dovecot
```
open up /usr/local/etc/dovecot/dovecot.conf edit this line
```
...
protocols = imap pop3
...
```
設成protocols = imap pop3 
跳過設定
ssl key file

```
sudo cp -r /usr/local/etc/dovecot/example-config/conf.d /usr/local/etc/dovecot
```

```
# rm /usr/local/etc/dovecot/conf.d/10-ssl.conf
```

```
cd /usr/local/etc/rc.d sudo ./dovecot onestart
```
or
```
# service dovecot start
```
<br/>
<br/>

## Troubleshot:

#### invalid hostname:<br/>
        解決步驟:輸入hostname "你的名字"(雙引號不用打 <br/>
        再輸入ee /etc/rc.conf <br/>
        修改hostname的名字<br/>
        
        
        
        
        
       Setup POP3s and IMAPs (port 993 & 995)
       
       http://mail.lsps.tp.edu.tw/~gsyan/freebsd2001/mail.html
