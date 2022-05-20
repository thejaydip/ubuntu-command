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
