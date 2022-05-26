# Files and Folder Permission

###### First of all go to theme directory path, then after apply below commands:

### For files permission
<code>sudo find . -type f -exec chmod 644 {} \;</code>

### For folders permission
<code>sudo find . -type d -exec chmod 755 {} \;</code>

### You can create zip using commands:

<code>zip -r hello-world.zip hello-world</code>

<code>zip -r hello-world-child.zip hello-world-child</code>

<code>zip -r hello-world-addons.zip hello-world-addons</code>

<b><i>But make sure you neeed to navigate themes folder and plugins folder respectively</i></b>


### File / Folder Permission for specific folder

<code>sudo chmod -R 0777 /var/www/html/demo</code>

<code>sudo chown -R www-data:www-data /var/www/html/demo</code>
  
# Restart Apache 2 web server

<code>/etc/init.d/apache2 restart</code>

###### <i>OR</i>

<code>sudo /etc/init.d/apache2 restart</code>

###### <i>OR</i>

<code>sudo service apache2 restart</code>

# To stop Apache 2 web server, enter:

<code>/etc/init.d/apache2 stop</code>

###### <i>OR</i>

<code>sudo /etc/init.d/apache2 stop</code>

###### <i>OR</i>

<code>sudo service apache2 stop</code>

# SSH

### CREATE TAR FILE

<code>tar -zcvf public_html_10_july_2018.tar.gz public_html/*</code>

### Download Database

<code>mysqldump -u [dbusername] -p [dbpassword] > demo_dev_10_july_2018.sql</code>

### Extract TAR

<code>tar -zxvf FILENAME.tar.gz</code>


### CREATE DB TAR FILE

<code>tar -zcvf rm_wp_live_22-July-2022.tar.gz rm_wp_live_22-July-2022.sql</code>
