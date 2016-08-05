## Warning
**This script is being fixed, you should not use it now !**

## Requirements:

To run letsencrypt-nginx-gen, you will need the following packages :
Markup : * Nginx
  * Git
  * php5-fpm
  * bc
  * bash.

## Instructions 

To add a new HTTPS vHost to your Nginx configuration, just execute new_vhost as root (or with sudo).

If you use new_vhost frequently, you may want to copy new_vhost to a folder of your $PATH (ie. /usr/sbin/).


Letsencrypt-nginx is a Bash script that generates config files for Nginx.
The script follows these steps :

1. Ask the user to type the vHost server name (ie. example.com).
2. Ask the user to type the webroot path (ie. /var/www/example.com).
3. Generate a config file sample (HTTPS-less) and restart Nginx daemon.
4. Start letsencrypt's certbot and generate a 2048 bit DH key.
5. Generate a new config (letsencrypt-https compatible).
6. Restart Nginx daemon.

Warning: Before launching this script, please make sure that the A/AAAA fields are properly propagated and correct (ie. example.com's A/AAAA field must contain webserver's IP adress) ; else, LetsEncrypt's certbot will fail.

## Etc
This script is not affiliated to Letsencrypt Certificate Authority.
