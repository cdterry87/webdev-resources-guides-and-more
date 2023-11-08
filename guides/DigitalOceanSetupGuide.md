# Digital Ocean Guide

This is a list of helpful links for setting up a Digital Ocean box for Web Development with PHP.

## Link a Domain

https://www.digitalocean.com/community/tutorials/how-to-point-to-digitalocean-nameservers-from-common-domain-registrars

## Initial Server Setup

https://www.digitalocean.com/community/tutorials/initial-server-setup-with-ubuntu-18-04

## Setup LAMP stack

https://www.digitalocean.com/community/tutorials/how-to-install-linux-apache-mysql-php-lamp-stack-ubuntu-18-04

## Reset MySQL password

https://www.digitalocean.com/community/tutorials/how-to-reset-your-mysql-or-mariadb-root-password-on-ubuntu-18-04

## Setup Mod Rewrite in Apache for cleaner URLs

https://www.digitalocean.com/community/tutorials/how-to-rewrite-urls-with-mod_rewrite-for-apache-on-ubuntu-16-04

## Install Git

https://www.digitalocean.com/community/tutorials/how-to-install-git-on-ubuntu-18-04

## Install Composer and NodeJS

https://www.digitalocean.com/community/tutorials/how-to-install-and-use-composer-on-ubuntu-18-04
https://www.digitalocean.com/community/tutorials/how-to-install-node-js-on-ubuntu-18-04

## Deploy Laravel to DigitalOcean

https://medium.com/@franciscojbarrera/how-to-deploy-laravel-on-digital-ocean-lamp-e69046906fe

## Advanced Setup

### Setup Virtual Hosts

https://www.digitalocean.com/community/tutorials/how-to-set-up-apache-virtual-hosts-on-ubuntu-16-04

### Setup SSL Certificates with LetsEncrypt

https://www.digitalocean.com/community/tutorials/how-to-secure-apache-with-let-s-encrypt-on-ubuntu-18-04

#### Bonus - Setting up SSL Cert with a wildcard

```
sudo certbot certonly --manual --preferred-challenges=dns --server=https://acme-v02.api.letsencrypt.org/directory --agree-tos -d yourtld.com,*.yourtld.com
```
