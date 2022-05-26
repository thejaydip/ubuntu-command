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


# Mount File Systems in Linux

###### For example, to mount the //ServerIP/ServerShare file system to the /mnt/directory directory you would use:

<code>sudo mount //ServerIP/ServerShare /mnt/directory -o username=[username],password=[password],file_mode=0777,dir_mode=0777</code>

# Database Import / Export

### Export

<code>mysqldump -h localhost -u root -p'mysql123' db-wordpess_demo > dump.sql</code>

### Import

<code>mysql -h localhost -u root -p'mysql123' db-wordpess_demo < /home/sys37/Downloads/wordpess-demo.sql</code>

# How to Install GIT

<code>git --version</code>

<code>sudo apt update</code>

<code>sudo apt install git</code>


### Setting Up Git

Configuration can be achieved by using the git config command.

<code>git config --global user.name "Your Name"</code>

<code>git config --global user.email "youremail@domain.com"</code>

We can display all of the configuration items that have been set by typing:

<code>git config --list</code>

###### REFERENCE LINK: https://www.digitalocean.com/community/tutorials/how-to-install-git-on-ubuntu-20-04


# How to Uninstall GIT

To remove just git package itself from Ubuntu 14.04 execute on terminal:

<code>sudo apt-get remove git</code>

Uninstall git and it's dependent packages

<code>sudo apt-get remove --auto-remove git</code>

Purging git

<code>sudo apt-get purge git</code>

<code>sudo apt-get purge --auto-remove git</code>


# How to use GIT
 
###### Take latest clone from git repo.
<code>git clone https://github.com/[username]/[repository-name].git</code>
enter Username and password

###### Check total branch in existing project:
<code>git branch</code>
 
###### Switch new branch for development:
<code>git checkout -b develop</code>
 
###### Take latest pull of new created branch:
<code>git pull origin develop</code>
 
###### Add New File in your git project
Run <code>git status</code> command to check list of updated files.
 
###### Add all updated files in git using
<code>git add -A</code>

###### Commit all files in git using:
<code>git commit -m "All files uploaded"</code>

###### Now push all files in git using:
<code>git push origin develop</code>
  
###### REFERENCE LINK: <a href="https://github.com/joshnh/Git-Commands" target="_blank">https://github.com/joshnh/Git-Commands</a>

# How to Install composer

###### Install composer globally composer using this article https://www.digitalocean.com/community/tutorials/how-to-install-and-use-composer-on-ubuntu-20-04
 
###### Open terminal and type <code>whereis composer</code>, composer should be installed on this path <i>/usr/local/bin/composer</i>
 
###### Execute below all command one by one: 
 
<code>composer global require squizlabs/php_codesniffer</code>
 
<code>composer global require wp-coding-standards/wpcs</code>
 
<code>composer global require phpcompatibility/php-compatibility</code>
 
<code>composer global require dealerdirect/phpcodesniffer-composer-installer</code>
 
###### Install extension on visual code editor:
 (i)   PHP Intelephense - Ben Mewburn<br />
 (ii)  phpcs - Ioannis Kappas<br />
 (iii) WordPress Hooks Intellisense - johnbillion<br />
	
### Add below scripts settings.json configuration in visual code ( ctrl + shft + p ):
 
```json
{
    "php.validate.executablePath": "/usr/bin/php",
    "phpcs.enable": true,
    "phpcs.executablePath" : "/home/[system-name]/.config/composer/vendor/bin/phpcs",
    "phpcs.standard": "WordPress",
    "[php]": {
    	"editor.defaultFormatter": "bmewburn.vscode-intelephense-client"
     },
}
```
<i>[system-name] - like sys31 or systemdell etc...</i>
 
###### Add phpcs.xml and .editorconfig files in the theme directory.
 
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

# How to Install Gulp.js on Ubuntu

### Step 1 – Installing Node.js

###### First of all, you need to install node.js on your system. Use following set of commands to add node.js PPA in your Ubuntu system and install it.

<code>sudo apt-get install python-software-properties</code>

<code>curl -sL https://deb.nodesource.com/setup_12.x | sudo -E bash -</code>

<code>sudo apt-get install nodejs</code>

###### Make sure you have successfully installed node.js and NPM on your system

<code>node --version</code>

<code>npm --version</code>

### Step 2 – Create Sample Application with NPM

###### Gulp can be easily use in your existing Node.js application. You just need to install Gulp package for Node.js in your project. For this tutorial, I am creating a sample Node.js application with NPM.

<code>mkdir gulp-project && cd gulp-project</code>

<code>npm init</code>

###### This command will prompt the required information to initialize a new empty project under the current directory.

###### Input all the required details for your application. At the end, it will show you the details you input and ask you to confirm.

###### About to write to /root/gulp-project/package.json:
```json
{
  "name": "gulp-project",
  "version": "1.0.0",
  "description": "First gulp application by Tecadmin",
  "main": "index.js",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1"
  },
  "keywords": [
    "gulp",
    "app"
  ],
  "author": "TecAdmin",
  "license": "ISC"
}
```
###### Is this OK? (yes)


###### Just press enter to save all details in package.json file.

### Step 3 – Install Gulp.js on Ubuntu

###### Once you have an node.js application. Use the following commands to install Gulp CLI globally on your system.

<code>npm install -g gulp-cli</code>

###### Also install the gulp package in your application. Swith to your application directory and execute the following command.

<code>npm install --save-dev gulp</code>

###### All done, Let’s check the installed version of Gulp CLI on your system and Gulp module in your application with the following command.

<code>gulp --version</code>

### Step 4 – Gulp Hello World Example

###### As you have gulp package added your application and installed gulp-cli on your system.

###### Next, create a gulpfile.js under the application root directory.

###### Add a sample code of gulp hello world example program.

```js
var gulp = require('gulp');

gulp.task('hello', function(done) {
  console.log('Hello World!!!');
  done();
})
```

###### Save your file and close.

###### Next run the gulp task with the following command under the application.

<code>gulp hello</code>
	
### Install required gulp modules
<code>npm install gulp-sourcemaps node-sass gulp-clean-css gulp-webserver gulp-sass gulp-ruby-sass gulp-autoprefixer gulp-minify-css gulp-rename gulp-changed gulp-imagemin gulp-concat gulp-uglify main-bower-files gulp-watch gulp-livereload browser-sync --save-dev</code>
  

###### REFERENCE LINK: https://www.digitalocean.com/community/tutorials/how-to-get-started-with-gulp-js-on-your-vps
