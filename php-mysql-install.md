# Update PHP

###### Add the right ppa first, do the following:

1. <code>sudo add-apt-repository ppa:ondrej/php</code>
2. <code>sudo apt-get update</code>
3. <code>sudo apt-get -y install php7.4-common php7.4-mysql libapache2-mod-php7.4 php7.4-mcrypt php7.4-mbstring php7.4-curl php7.4-cli php7.4-mysql php7.4-gd php7.4-intl php7.4-xsl php7.4-zip php7.4-xml</code>
4. <code>sudo a2dismod php5.6 sudo a2dismod php7.0 sudo a2dismod php7.1 sudo a2dismod php7.2 sudo a2dismod php7.3 sudo a2dismod php8.0 sudo a2dismod php8.1</code>
5. <code>sudo a2enmod php7.4</code>
6. <code>sudo update-alternatives --set php /usr/bin/php7.4</code>
7. <code>sudo systemctl restart apache2</code>
	
###### REFERENCE LINKs
https://www.digitalocean.com/community/tutorials/how-to-install-php-7-4-and-set-up-a-local-development-environment-on-ubuntu-18-04

https://www.digitalocean.com/community/tutorials/how-to-install-mysql-on-ubuntu-20-04

###### Check PHP version
<code>php -v</code>
	
###### Check PHP module
<code>php -m</code>
	
###### Check Apache version
<code>apache2 -v</code>

# Database Import / Export

### Export

<code>mysqldump -h localhost -u root -p'mysql123' db-wordpess_demo > dump.sql</code>

### Import

<code>mysql -h localhost -u root -p'mysql123' db-wordpess_demo < /home/sys37/Downloads/wordpess-demo.sql</code>
  
