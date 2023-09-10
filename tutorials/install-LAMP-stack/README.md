# install LAMP (Linux, Apache, MariaDB/MySQL, PHP) Stack

## Update packages

```
  dnf update
```

## Install services to run a LAMP server

- Install Apache Web Server:

```
sudo dnf install httpd
Once the installation is complete, start the Apache service and enable it to start automatically at boot time:

sudo systemctl start httpd
sudo systemctl enable httpd
```

- Install MariaDB Database Server:

```
sudo dnf install mariadb-server
```

Once the installation is complete, start the MariaDB service and enable it to start automatically at boot time:

```
sudo systemctl start mariadb
sudo systemctl enable mariadb
```

Configure secure connection.

- Install and Configure PHP:

```
  sudo dnf install php php-cli php-common php-gd php-mysqlnd php-pdo
```

```
 sudo nano /etc/php.ini
```

In the file, look for the following lines and modify them as follows:

```
memory_limit = 256M
upload_max_filesize = 128M
post_max_size = 128M
```

- Test the LAMP Stack:

To verify that our LAMP Stack is properly installed and configured, we will create a simple PHP script and run it through Apache.

Create a new file named `info.php` in the Apache web root directory using the following command:

```
sudo nano /var/www/html/info.php
```

Paste the following code into the file:

```php
<?php
phpinfo();
```

Save and close the file.

Now, open your web browser and navigate to `http://your-server-ip/info.php`. You should see a page displaying the PHP configuration information. If you see this page, then your LAMP Stack is up and running.

### Troubleshooting

###### El servidor Apache muestra la pagina como texto plano.

Si el servidor Apache muestra la pagina de PHP como texto plano sigue [estas instrucciones](https://stackoverflow.com/a/35170884).

#### References

[How to Install LAMP Stack on RHEL & CentOS Stream 9](https://tecadmin.net/how-to-install-lamp-stack-on-centos-9/)
