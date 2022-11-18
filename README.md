# Install-wordpress-on-ubunto : نصب وردپرس در ابونتو


###### لینک ویدیو : 
```

```

###### خرید دامنه از نیم چیپ: 
```
https://namecheap.pxf.io/BX7m6W
```
###### خرید دامنه سایت ایرانی: 
```
https://www.hub.shatelhost.com/aff.php?aff=290
```
###### خرید سرور از دیجیتال اوشن : 
```
https://m.do.co/c/0fb522deafa4
```
###### خرید سرور از سایت ایرانی : 
```
https://berbidserver.com/portal/aff.php?aff=53
```
###### خرید سرور از سایت ایرانی : 
```
https://dashboard.azaronline.com/order/?aff=790
```


###### Update & Upgrade Server : آپدیت و آپگرید سرور

``` 
apt update -y && apt upgrade -y 
```

###### Install Apache : نصب آپاچی

```
apt install apache2
```

###### Confirm Apache Installed : تایید نصب آپاچی

```
systemctl status apache2
```

###### Cehck By Server Address : چک کردن آپاچی از طریق آدرس سرور

```
https://Server-ip-address
```

###### Install MySQL : نصب دیتابیس

```
apt install mariadb-server mariadb-client
```

###### SecureMariaDB : امنیت دیتابیس

```
mysql_secure_installation
```

>Change Root Password : N

>Remove anonymous users: Y

>Disallow root login remotely: N

>Remove test database: Y

>Reload privilege table now? : Y


###### Install PHP : نصب پی اچ پی

```
apt install php php-mysql
```

###### Confirm PHP Installed : تایید نصب پی اچ پی

```
nano /var/www/html/info.php
```

```
<?php
phpinfo();
?>
```

###### Cehck By Server Address : چک کردن پی اج پی از طریق آدرس سرور

```
https://Server-ip-address/info.php
```

###### Create DataBase : ساخت دیتابیس

```
mysql -u root -p
```

```
CREATE DATABASE wordpress_db;
```

###### Create Database User: ساخت یوزر برای دیتابیس 

```
CREATE USER 'wp_user'@'localhost' IDENTIFIED BY 'password';
```

###### User Permissions :  دسترسی های لازم برای یوزر

```
GRANT ALL ON wordpress_db.* TO 'wp_user'@'localhost' IDENTIFIED BY 'password';
```

###### Exit of Database :  خروج از دیتابیس

```
FLUSH PRIVILEGES;
Exit;
```

###### Install WP CMS : نصب وردپرس

```
cd /tmp && wget https://wordpress.org/latest.tar.gz
```

###### Unzip WP : اکسترکت کردن فایل زیپ

```
tar -xvf latest.tar.gz
```

###### Change Dir of WP : تغییر دایرکتوری 

```
cp -R wordpress /var/www/html/
```

###### Run to change the ownership

```
chown -R www-data:www-data /var/www/html/wordpress/
```

###### change permission to WP folder

```
chmod -R 755 /var/www/html/wordpress/
```

###### Create Upload Dir: ساخت فولدر آپلود دروردپرس

```
mkdir /var/www/html/wordpress/wp-content/uploads
```

###### Change Permissions of Upload Folder: تغییر دسترسی فولدر آپلود

```
chown -R www-data:www-data /var/www/html/wordpress/wp-content/uploads/
```

###### Install WP by UI: نصب وردپرس

```
https://server-ip-address/wordpress
```
