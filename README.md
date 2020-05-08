<h1>Steps to configure ubuntu PC with mysql and apche</h1>
<pre>
1) sudo apt-get update
2) sudo apt-get install apache2
3) sudo apt-get install mysql-server mysql-client

- sudo mysql
- ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY 'root';
- FLUSH PRIVILEGES;

4) sudo add-apt-repository ppa:ondrej/php
    sudo apt-get update
  sudo apt-get upgrade

sudo apt-get install php7.2 php7.2-mysql php7.2-curl php7.2-json php7.2-cgi php-mbstring php7.2-mbstring php7.2-gettext libapache2-mod-php7.2 && sudo apt-get install php7.1 php7.1-mysql php7.1-curl php7.1-json php7.1-cgi php-mbstring php7.1-mbstring php7.1-gettext libapache2-mod-php7.1 && sudo apt-get install php7.0 php7.0-mysql php7.0-curl php7.0-json php7.0-cgi php-mbstring php7.0-mbstring php7.0-gettext libapache2-mod-php7.0 && sudo apt-get install php7.3 php7.3-mysql php7.3-curl php7.3-json php7.3-cgi php-mbstring php7.3-mbstring php7.3-gettext libapache2-mod-php7.3 && sudo apt-get install php5.6 php5.6-mysql php5.6-curl php5.6-json php5.6-cgi php-mbstring php5.6-mbstring php5.6-gettext libapache2-mod-php5.6 && sudo apt-get install php7.4 php7.4-mysql php7.4-curl php7.4-json php7.4-cgi php-mbstring php7.4-mbstring php7.4-gettext libapache2-mod-php7.4

sudo service apache2 restart

5) sudo nano /var/www/html/test.php
    <?php phpinfo(); ?>
6) sudo service apache2 restart
7) sudo apt-get install phpmyadmin
8) sudo nano /etc/apache2/apache2.conf
Include /etc/phpmyadmin/apache.conf >> add this line in the end.

sudo nano /etc/apache2/sites-available/000-default.conf

<Directory /var/www/html>
Options Indexes FollowSymLinks
AllowOverride All
Require all granted
</Directory>

=> run below commands to activate rewrite module.
sudo a2enmod rewrite
sudo service apache2 restart
</pre>
