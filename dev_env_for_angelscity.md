# Prepare development environment of AngelsCity on Ubuntu


## Install LAMP
AngelsCity will run on MySQL db, to install MySQL db, tasksel is recommended way to install LAMP server.

    sudo apt-get install tasksel
    sudo tasksel
    sudo apt-get install phpmyadmin

## Create virtualenv

    virtualenv -p python3 --no-site-packages ~/virtualenv/py3dj8
where `-p` specify python exec name, `--no-site-packages` make a clean copy of current python3 environment, `~/virtualenv/py3dj8` is your virtualenv path for developing AngelsCity

## Active virtualenv
    source virtualenv/py3dj8/bin/activate

## Prerequisites
    sudo apt-get install libmysqlclient-dev
    sudo apt-get install python3-dev

## Install requirements
    pip install -r requirements.txt

## Test
### Create test project
	mkdir projectpath
	cd projectpath
	django-admin startproject projectname
### Configure database settings
	vim projectname/projectname/settings.py

Change DataBase settings as following:

	DATABASES = {
    	'default': {
        	'ENGINE': 'django.db.backends.mysql',
	        'OPTIONS': {
    	        'read_default_file': '/path/to/my.cnf',
        	},
	    }
	}

my.cnf:

	[client]
	database = NAME
	user = USER
	password = PASSWORD
	default-character-set = utf8
### Create database
	mysql -u root -p
	create database dbname;

### Migrate data
	python manage.py migrate

### Run server
	python manage.py runserver

Make sure above commands are running under your virtualenv

--------------
## zsh related plugins
    vim ~/.zshrc

add django plugin as following:

    plugins=(git, django, virtualenv, pip)