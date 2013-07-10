Behat Testing App
=================

Hi guys!

### Pre-requisites!

Make sure you have the "sqlite" extension for PHP Installed!

### Setup

1) Clone this somewhere under your web server root directory:

    git clone git@github.com:weaverryan/simple-silex-start.git behat-test

2) To make this web accessible, you have a few options:

a)  Setup a virtualhost that points to the **web** directory and add an entry
    to your `/etc/hosts` file. The site will be accessible at whatever hostname
    you setup.
  
b) Use PHP 5.4's (if you have this version) built-in web server:
  
```
  cd web
  php -S localhost:8000
```

Your site will be accessible at `http://localhost:8000`. Just let this "hang"
and open up a new terminal tab.

c) Do nothing! As long as you cloned this under your web server document
root, just surf to it. It will be something like `http://localhost/behat-test/web`
  
3) Have Composer download all of the external libraries:

```
curl -sS https://getcomposer.org/installer | php
php composer.phar install --prefer-dist
```

4) Fix some directory permissions

```
mkdir data
chmod -R 777 data/
```

5) Build up the database!

Access the site (see step 2). Click "Admin" on the navigation, then click
the "Reset DB" link on the left. You should just see a simple JSON message.
If you did, it worked and you're all setup!