Setting up Ghost on a Linux is pretty straight forward.
 
##Dependencies
 
The only dependency needed from your distros repository is Git
 
If you're running a Debian based distribution like Ubuntu use:
 
    sudo apt-get install git
 
Fedora/CentOS or similar would be:
 
    sudo yum install git
 
##Create a user to run Ghost
 
    adduser ghost --shell /bin/bash
    su ghost
    cd
 
##Set up Node Version Manager (NVM)
 
The version of node in your package manager is most likely to old to run Ghost, NVM makes it easy to pick and change the version of Node.js you are using with ease.
 
    curl http://raw.github.com/creationix/nvm/master/install.sh | sh
    source .bash_profile
    nvm ls-remote
 
##Install Node.js
 
    nvm install v0.10.5
 
##Install Ghost
 
    mkdir ghost
    cd ghost
    wget https://en.ghost.org/zip/ghost-0.3.0.zip
    unzip ghost-0.3.0.zip
    npm install --production
    npm start
 
Ok if that all worked alright you should be able to visit your blog here:
 
[http://localhost:2368/][]
