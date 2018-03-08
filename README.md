This project should create a small PHP sandbox environment ready for the user to upload the PHP application in it's root directory.

It is assumed that Nginx, PHP-FPM, MySQL/MariaDB are installed and configured.

Currently the playbook is compatible with Ubuntu only.

When triggering the script:
* The user must provide the FQDN of which the application will be served from.
* Specify to create a database or not

The logical sequence should be:
1. Create a directory for the application based on the user input i.e. ```/var/www/www.example.com```
2. Put index.php in the root directory ```/var/www/www.example.com/index.php```
3. If a database is required, then create a new database, database user and password.
4. Create a new nginx virtual host for serving the new application
