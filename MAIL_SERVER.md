Setup a working POP3 & IMAP server using Dovecot (port 110 & 143)

http://izero.pixnet.net/blog/post/17061915

/usr/local/etc/dovecot/example-config % sudo cp dovecot.conf /usr/local/etc/dovecot

/usr/local/etc/dovecot  sudo ee dovecot.conf

設成protocols = imap pop3 

跳過設定 ssl key file

sudo cp -r /usr/local/etc/dovecot/example-config/conf.d /usr/local/etc/dovecot

/usr/local/etc/dovecot/conf.d  rm 10-ssl.conf

/usr/local/etc/rc.d sudo ./dovecot onestart
