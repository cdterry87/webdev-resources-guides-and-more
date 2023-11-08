# Digital Ocean Setup Guides

- [Link a Domain](https://www.digitalocean.com/community/tutorials/how-to-point-to-digitalocean-nameservers-from-common-domain-registrars)
- [Initial Server Setup](https://www.digitalocean.com/community/tutorials/initial-server-setup-with-ubuntu-18-04)
- [Setup LAMP stack](https://www.digitalocean.com/community/tutorials/how-to-install-linux-apache-mysql-php-lamp-stack-ubuntu-18-04)
- [Reset MySQL password](https://www.digitalocean.com/community/tutorials/how-to-reset-your-mysql-or-mariadb-root-password-on-ubuntu-18-04)
- [Setup Mod Rewrite in Apache for cleaner URLs](https://www.digitalocean.com/community/tutorials/how-to-rewrite-urls-with-mod_rewrite-for-apache-on-ubuntu-16-04)
- [Install Git](https://www.digitalocean.com/community/tutorials/how-to-install-git-on-ubuntu-18-04)
- [Install Composer](https://www.digitalocean.com/community/tutorials/how-to-install-and-use-composer-on-ubuntu-18-04)
- [Install Node.js](https://www.digitalocean.com/community/tutorials/how-to-install-node-js-on-ubuntu-18-04)
- [Deploy Laravel to DigitalOcean](https://medium.com/@franciscojbarrera/how-to-deploy-laravel-on-digital-ocean-lamp-e69046906fe)

# Digital Ocean Setup [Advanced]

- [Setup Virtual Hosts](https://www.digitalocean.com/community/tutorials/how-to-set-up-apache-virtual-hosts-on-ubuntu-16-04)
- [Setup SSL Certificates with LetsEncrypt](https://www.digitalocean.com/community/tutorials/how-to-secure-apache-with-let-s-encrypt-on-ubuntu-18-04)
- [LetsEncrypt wildcard certificates with cerbot](https://www.digitalocean.com/community/tutorials/how-to-create-let-s-encrypt-wildcard-certificates-with-certbot)

## Setting up SSL Cert with a wildcard with Certbot

> Replace `your-tld.com` below with your Top Level Domain name.

```
sudo certbot certonly --manual --preferred-challenges=dns --server=https://acme-v02.api.letsencrypt.org/directory --agree-tos -d your-tld.com,*.your-tld.com
```

or, if you have the [dns-digitalocean certbot plugin](https://certbot-dns-digitalocean.readthedocs.io/en/stable/) installed:

```
sudo certbot certonly \
  --dns-digitalocean \
  --dns-digitalocean-credentials ~/certbot-creds.ini \
  -d your-tld.com \
  -d '*.your-tld.com'
```
