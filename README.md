# Web Development in Mac #

## Menu
1. [Install Brew](#brew)
2. [Database](#db)


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

## Menu
1. [Install Brew](#brew)
2. [Database](#db)

