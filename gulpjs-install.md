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
