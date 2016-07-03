Letsencrypt-nginx is a Bash script that generates config files for Nginx.
The script follows these steps :

1. Ask the user to type the vHost server name (ie. example.com).
2. Ask the user to type the webroot path (ie. /var/www/example.com).
3. Generate a config file sample (HTTPS-less) and restart Nginx daemon.
4. Start letsencrypt's certbot and generate a 2048 bit DH key.
5. Generate a new config (letsencrypt-https compatible).
6. Restart Nginx daemon.

Warning: Before launching this script, please make sure that the A/AAAA fields are properly propagated and are correct (ie. example.com's A/AAAA field must contain webserver's IP adress) ; else, letsencrypt's certbot will fail.

This script is not affiliated to Letsencrypt Certificate Authority.
