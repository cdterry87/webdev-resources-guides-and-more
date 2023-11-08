# Setup WSL for Web Development on Windows

## Enable/Install WSL

Open a command prompt (as administrator) and type:

```
Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
```

Then go to the Microsoft Store and type `Ubuntu` into the search. Install Ubuntu, and then Launch it when the install is complete.

When the terminal opens and the install is complete, you should be prompted to create your user account. Create your username and password.

## Setup Git

```
git config --global user.name "Your Name"
git config --global user.email "youremail@domain.com"
```

## Get cURL

```
sudo apt-get install curl
```

## Install NVM and Node

```
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.35.2/install.sh | bash
```

Then close and reopen Ubuntu terminal and then type:

```
nvm install node
```

## Install Vue CLI

```
npm install -g @vue/CLI
```

## Install Apache

```
sudo apt update
sudo apt install apache2
sudo service apache2 start
```

### Apache Commands

```
sudo service apache2 start
sudo service apache2 restart
sudo service apache2 stop
```

By default, the DocumentRoot is set to `/var/www/html`. To change it:

```
sudo vi /etc/apache2/sites-available/000-default.conf
sudo service apache2 restart
```

Change DocumentRoot from `DocumentRoot /var/www/html` to your own specified directory.

You may also want to change the permissions on your DocumentRoot directory. If you changed your DocumentRoot directory using the instructions above, change `/var/www/html` in the example below to the directory you specified.

```
sudo chown your-user:your-user -R /var/www/html
```

## Install MySQL

```
sudo apt install mysql-server
sudo service mysql start
sudo mysql
```

To set a password for mysql's root user

```
ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY 'password';
FLUSH PRIVILEGES;
SELECT user,authentication_string,plugin,host FROM mysql.user;
exit;
```

## Install PHP

```
sudo apt install php libapache2-mod-php php-mysql
```

Allow Apache to serve .php files

```
sudo vi /etc/apache2/mods-enabled/dir.conf
```

Modify it to look like this:

```
<IfModule mod_dir.c>
    DirectoryIndex index.php index.html index.cgi index.pl index.xhtml index.htm
</IfModule>
```

Then restart Apache

```
sudo service apache2 restart
```

Install php cli

```
sudo apt install php-cli
```

Install phpmyadmin

```
sudo apt install phpmyadmin php-mbstring php-gettext
```

When installing phpmyadmin, a prompt will come up to specify a password for phpmyadmin. After specifying a password, you will need to specify the webserver. Press "SPACE" to select apache2 then click Enter.

```
sudo phpenmod mbstring
sudo service apache2 restart
```

Then test it by going to [http://localhost/phpmyadmin] in a browser

## Install Composer

```
cd ~
curl -sS https://getcomposer.org/installer -o composer-setup.php
sudo php composer-setup.php --install-dir=/usr/local/bin --filename=composer
php composer-setup.php
sudo mv composer.phar /usr/local/bin/composer
```

## Install Laravel Installer

```
composer global require laravel/installer
echo 'export PATH="$PATH:$HOME/.composer/vendor/bin"' >> ~/.bashrc
```

Test it with the following command:

```
cd /var/www/
laravel new project
```
