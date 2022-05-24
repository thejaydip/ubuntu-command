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

Hello
