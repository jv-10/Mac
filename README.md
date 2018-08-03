# Web Development in Mac #

## Menu
1. [Install Brew](#brew)
2. [Database](#db)
3. [SSH](#ssh)

### <a name="brew"></a>Install Brew

Go to [Brew.bh](https://brew.sh/)

Install Homebrew (package manager)

    /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"

#### Install Dependencies ####
    brew install homebrew/php/php71
    brew install mcrypt php71-mcrypt
    brew install composer
    brew install npm
    brew install mysql
    
    After installing MySQL, authenticate using the CLI e.g
    mysql -uroot

    Then run the following command to use the old authentication method:
    ALTER USER root@localhost IDENTIFIED WITH mysql_native_password BY 'PASSWORD';

    Lastly, flush the privileges:
    FLUSH PRIVILEGES;
    
    composer global require laravel/valet

#### Install Valet ####
    export PATH=$PATH:~/.composer/vendeor/bin
    valet install


#### Navigate to folder ####
    cd .valet
    cd sites


#### Valet Park ####
    valet park
    valet domain loc


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


## Menu
1. [Install Brew](#brew)
2. [Database](#db)
3. [SSH](#ssh)
