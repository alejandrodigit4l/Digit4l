# Digit4l
Proyectos versión beta.

Instalacion de laravel:
-------------------------

                                              INSTALATION COMPOSER 

Step 1 — Installing the Dependencies
Before we download and install Composer, we need to make sure our server has all dependencies installed.

First, update the package manager cache by running:

    $ sudo apt-get update

Now, let's install the dependencies. We'll need curl in order to download Composer and php5-cli for installing and running it. git is used by Composer for downloading project dependencies. Everything can be installed with the following command:

    $ sudo apt-get install curl php5-cli git

You can now proceed to the next step.

Step 2 — Downloading and Installing Composer
Composer installation is really simple and can be done with a single command:

    $ curl -sS https://getcomposer.org/installer | sudo php -- --install-dir=/usr/local/bin --filename=composer

This will download and install Composer as a system-wide command named composer, under /usr/local/bin. The output should look like this:

Output
#!/usr/bin/env php
All settings correct for using Composer
Downloading...

Composer successfully installed to: /usr/local/bin/composer
Use it: php /usr/local/bin/composer
To test your installation, run:

      $ composer

And you should get output similar to this:

Output

Composer version 1.0-dev (9859859f1082d94e546aa75746867df127aa0d9e) 2015-08-17 14:57:00

Usage:
 command [options] [arguments]

Options:
 --help (-h)           Display this help message
 --quiet (-q)          Do not output any message
 --verbose (-v|vv|vvv) Increase the verbosity of messages: 1 for normal output, 2 for more verbose output and 3 for debug
 --version (-V)        Display this application version
 --ansi                Force ANSI output
 --no-ansi             Disable ANSI output
 --no-interaction (-n) Do not ask any interactive question
 --profile             Display timing and memory usage information
 --working-dir (-d)    If specified, use the given directory as working directory.

. . .
This means Composer was succesfully installed on your system.

If you prefer to have separate Composer executables for each project you might host on this server, you can simply install it locally, on a per-project basis. This method is also useful when your system user doesn't have permission to install software system-wide. In this case, installation can be done with curl -sS https://getcomposer.org/installer | php - this will generate a composer.phar file in your current directory, which can be executed with php composer.phar [command].


                      INSTALL LARAVEL


Laravel utilizes Composer to manage its dependencies. So, before using Laravel, make sure you have Composer installed on your machine.

Via Composer Create-Project

Alternatively, you may also install Laravel by issuing the Composer create-project command in your terminal:

    $ composer create-project --prefer-dist laravel/laravel blog

Local Development Server

If you have PHP installed locally and you would like to use PHP's built-in development server to serve your application, you may use the serve Artisan command. This command will start a development server at http://localhost:8000:

    $ php artisan serve

Of course, more robust local development options are available via Homestead and Valet.
