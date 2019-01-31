# Setup a working POP3 & IMAP server using Dovecot (port 110 & 143)

http://izero.pixnet.net/blog/post/17061915

```
cd /usr/local/etc/dovecot/example-config 
```

```
\# cp dovecot.conf /usr/local/etc/dovecot
```

```
\# ee /usr/local/etc/dovecot/dovecot.conf
```

設成protocols = imap pop3 
跳過設定
ssl key file

```
sudo cp -r /usr/local/etc/dovecot/example-config/conf.d /usr/local/etc/dovecot
```

```
\# rm /usr/local/etc/dovecot/conf.d/10-ssl.conf
```

```
\# service dovecot
```
<br/>
<br/>

## Troubleshot:

### invalid hostname:<br/>
        解決步驟:輸入hostname "你的名字"(雙引號不用打 <br/>
        再輸入ee /etc/rc.conf <br/>
        修改hostname的名字<br/>
        
        
        
        
        
       Setup POP3s and IMAPs (port 993 & 995)
       
       http://mail.lsps.tp.edu.tw/~gsyan/freebsd2001/mail.html
