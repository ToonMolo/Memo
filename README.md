# Memo

## Vitrual host (local)
```
sudo nano /etc/hosts
sudo nano /etc/apache2/extra/httpd-vhosts.conf
sudo apachectl restart
```
## Vitrual host (distant)
```
cd /etc/apache2/sites-available
```
create file example.mywebsite.com.conf
```
<VirtualHost *:80>
        ServerAdmin mail@gmail.com
        ServerName example.mywebsite.com
        DocumentRoot /var/www/folder
        <Directory /var/www/folder>
                DirectoryIndex index.php
                Options Indexes FollowSymLinks MultiViews
                AllowOverride All
                Order allow,deny
                allow from all
        </Directory>
</VirtualHost>
```
```
a2ensite example.mywebsite.com
service apache2 reload
```

## Connect ssh
```
ssh root@ipserver
```
