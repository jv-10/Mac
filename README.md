# Web Development in Mac #

## Menu
0. [Install Softwares](#software) (not-required)
1. [Install Brew](#brew)
2. [Install Valet+](#valet)
3. [Setup Workflow](#workflow)
4. [Install npm](#npm)
5. [Database](#db)
6. [SSH](#ssh)
7. [Change php versions](#phpv)

---------------------------------------


### <a name="software"></a>Install Recommended Software

#### Install Chrome ####

<a href="https://www.google.com/chrome/">https://www.google.com/chrome/</a>

#### Install Atom ####

<a href="https://atom.io/">https://atom.io/</a>

#### Install muCommander ####

<a href="https://www.mucommander.com/index.html#download">https://www.mucommander.com/index.html#download</a>

#### Install Sequel Pro ####

<a href="https://sequelpro.com/download">https://sequelpro.com/download</a>

#### Install Postman ####

<a href="https://www.getpostman.com/downloads/">https://www.getpostman.com/downloads/</a>


---------------------------------------


### <a name="brew"></a>Install Brew

Go to [Brew.bh](https://brew.sh/)

Install Homebrew (package manager)

    /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"


---------------------------------------


### <a name="valet"></a>Install Valet+

[Documentation](https://github.com/weprovide/valet-plus)

#### Update Homebrew ####

    brew update

#### Add the Homebrew PHP tap ####

    brew tap henkrehorst/php

#### Install PHP 7.2 ####

    brew install valet-php@7.2

#### Install Composer ####

    brew install composer

#### Install Valet+ ####

    composer global require weprovide/valet-plus

#### Add export ####

    export PATH="$PATH:$HOME/.composer/vendor/bin"  >> ~/.bash_profile

#### Check for common issues ####

    valet fix

#### Install Valet ####
    valet install


---------------------------------------


### <a name="workflow"></a>Setup Workflow

#### Install git ####
    brew install git
  
#### Change Domain for Valet ####
    valet domain loc

#### Setup folders ####

Make folders

    mkdir ~/work/development
    cd ~/work/development

#### Valet park ####

    valet park

#### Create test ####

create folder
    mkdir ~/work/development/test
    cd ~/work/development/test

create index.php
    echo "<?php phpinfo();" > index.php

secure site
    valet secure test

#### Test
  Go to [https://test.loc](https://test.loc), you should see phpinfo().

__________________________________


### <a name="npm"></a>Install npm

    brew install node@8
    brew link node@8

__________________________________


### <a name="db"></a>Database

Download [Sequel Pro](https://www.sequelpro.com/)

#### Set up Database

Fill form as:

    Name: localhost
    Host: 127.0.0.1
    Username: root
    Password: (leave empty)

Check connection

#### Import Database:

    File -> Import



### <a name="ssh"></a>Create SSH

Terminal:

`$ ssh-keygen`

    Generating public/private rsa key pair.
    Enter file in which to save the key (/Users/emmap1/.ssh/id_rsa):

Click enter twice

    Generating public/private rsa key pair.
    Enter file in which to save the key (/Users/emmap1/.ssh/id_rsa):
    Created directory '/Users/emmap1/.ssh'.
    Enter passphrase (empty for no passphrase):
    Enter same passphrase again:
    Your identification has been saved in /Users/emmap1/.ssh/id_rsa.
    Your public key has been saved in /Users/emmap1/.ssh/id_rsa.pub.
    The key fingerprint is:
    4c:80:61:2c:00:3f:9d:dc:08:41:2e:c0:cf:b9:17:69 emmap1@myhost.local 
    The key's randomart image is:
    +--[ RSA 2048]----+
    |*o+ooo.          |
    |.+.=o+ .         |
    |. *.* o .        |
    | . = E o         |
    |    o . S        |
    |   . .           |
    |     .           |
    |                 |
    |                 |
    +-----------------+

Copy SSH

`pbcopy < ~/.ssh/id_rsa.pub`

#### Add to Bitbucket

Go to options and add SSH Key

![picture](https://confluence.atlassian.com/bitbucket/files/304578655/755335794/2/1502737357377/add_ssh_key.png)

__________________________________


### <a name="php v"></a>Change php versions


#### Switching PHP version

Switch PHP version using one of four commands:

    valet use 5.6
    valet use 7.0
    valet use 7.1
    valet use 7.2


## Menu
0. [Install Softwares](#software) (not-required)
1. [Install Brew](#brew)
2. [Install Valet+](#valet)
3. [Setup Workflow](#workflow)
4. [Install npm](#npm)
5. [Database](#db)
6. [SSH](#ssh)
7. [Change php versions](#phpv)
