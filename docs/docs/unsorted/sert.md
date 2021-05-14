*.gosweb.gosuslugi.ru

172.16.37.6


https://codex.so/wildcard-ssl


ок инструкция, но для убунты
https://obu4alka.ru/free-wildcard-lets-encrypt.html

на centos
https://galaxydata.ru/community/lets-encrypt-wildcard-sertifikat-na-centos-7-i-avtomatizaciya-1319
https://grib69.ru/2019/02/08/ustanovka-wildcard-sertifikata-lets-encrypt-na-centos-7/

ещё ubuntu
https://medium.com/@saurabh6790/generate-wildcard-ssl-certificate-using-lets-encrypt-certbot-273e432794d7
https://linux-notes.org/nastrojka-bezopasnogo-soedineniya-https/

https://www.digitalocean.com/community/tutorials/how-to-secure-nginx-with-let-s-encrypt-on-ubuntu-20-04


certbot -d *.gosweb.gosuslugi.ru --manual --preferred-challenges dns certonly --server https://acme-v02.api.letsencrypt.org/directory


certbot -d *.gosweb.gosuslugi.ru --manual --preferred-challenges http certonly --server https://acme-v02.api.letsencrypt.org/directory


certbot -d orlovkn.com --manual --preferred-challenges http certonly --server https://acme-v02.api.letsencrypt.org/directory



## 
yum install certbot

##
certbot -d *.gosweb.gosuslugi.ru --manual --preferred-challenges dns certonly --server https://acme-v02.api.letsencrypt.org/directory


certbot -d *.gosweb.gosuslugi.ru --manual --preferred-challenges dns certonly --server https://acme-v02.api.letsencrypt.org/directory

https://certbot.eff.org/docs/using.html#certbot-command-line-options



certbot -d gosweb.goswebcms.online --manual --preferred-challenges dns certonly --server https://acme-v02.api.letsencrypt.org/directory



certbot certonly --manual -d '*.gosweb.gosuslugi.ru'


certbot renew --cert-name *.gosweb.gosuslugi.ru --nginx




https://2whois.ru/?t=nslookup&data=_acme-challenge.gosweb.gosuslugi.ru&dns_type=txt
https://2whois.ru/?t=nslookup&data=http%3A%2F%2Fcontroller.goswebcms.ru%2F&dns_type=a




/etc/letsencrypt/live/gosweb.gosuslugi.ru/fullchain.pem
   Your key file has been saved at:
   /etc/letsencrypt/live/gosweb.gosuslugi.ru/privkey.pem
   Your cert will expire on 2021-07-17. To obtain a new or tweaked
   version of this certificate in the future, simply run certbot
   again. To non-interactively renew *all* of your certificates, run
   "certbot renew"
 - If you like Certbot, please consider supporting our work by:

   Donating to ISRG / Let's Encrypt:   https://letsencrypt.org/donate
   Donating to EFF:                    https://eff.org/donate-le

[root@p00goswebnlb01 konstantin.orlov]# cd /etc/letsencrypt/live/gosweb.gosuslugi.ru/
[root@p00goswebnlb01 gosweb.gosuslugi.ru]# mc
