# aws-mail

[![Build Status](https://travis-ci.org/dcrbsltd/aws-mail.svg)](https://travis-ci.org/dcrbsltd/aws-mail)

Amazon Web Services hosted Email service. Includes Ubuntu + Postfix + Courier IMAP + MySQL + Amavisd-new + SpamAssassin + ClamAV + SASL + TLS + Roundcube + Postgrey, based on the tutorial here http://flurdy.com/docs/postfix/.


## saslauth
Change how SASLAUTHD is run: ```sudo vim /etc/default/saslauthd```
```
  # Toggle this to yes
  START=yes
  # Switch this to be under postfix's spool
  # And add -r so that the realm(domain) is part of the username
  OPTIONS="-r -c -m /var/spool/postfix/var/run/saslauthd"
```