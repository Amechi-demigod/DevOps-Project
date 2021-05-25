cd ~/Downloads
$ sudo chmod 0400 Project1.pem
$ ssh -i Project1.pem ubuntu@3.8.136.164
$ sudo apt update
$ sudo apt install apache2
$ sudo systemctl status apache2
$ curl http://3.8.136.164:80
http://3.8.136.164:80r
Screenshot 2021-05-25 at 12.07.20![image](https://user-images.githubusercontent.com/84720654/119505368-c8e8a080-bd64-11eb-8c09-0500e5f38a37.png)
#Installing Mysql
$ sudo apt install mysql-server
$ sudo mysql_secure_installation
$ sudo mysql
Screenshot 2021-05-25 at 12.11.54![image](https://user-images.githubusercontent.com/84720654/119505544-fa616c00-bd64-11eb-9de7-d80de426cf5b.png)
#Installing PHP
$ sudo apt install php libapache2-mod-php php-mysql
$ php -v
Screenshot 2021-05-25 at 12.16.08![image](https://user-images.githubusercontent.com/84720654/119506270-a99e4300-bd65-11eb-94bd-67cc6f888158.png)
$ sudo mkdir /var/www/projectlamp
$ sudo vi /etc/apache2/sites-available/projectlamp.conf
$ sudo ls /etc/apache2/sites-available
Screenshot 2021-05-25 at 12.16.08![image](https://user-images.githubusercontent.com/84720654/119506483-db170e80-bd65-11eb-9281-313d70037ce7.png)
$ sudo a2ensite projectlamp
$ sudo a2dissite 000-default
$ sudo apache2ctl configtest
$ sudo systemctl reload apache2
echo 'Hello LAMP from hostname' $(curl -s http://169.254.169.254/latest/meta-data/public-hostname) 'http://3.8.136.164/' $(curl -s http://169.254.169.254/latest/meta-data/public-ipv4) > /var/www/projectlamp/index.html
http://3.8.136.164:80
Screenshot 2021-05-25 at 12.25.32![image](https://user-images.githubusercontent.com/84720654/119506831-334e1080-bd66-11eb-84b4-cc55a9bb81b9.png)
$ sudo vim /etc/apache2/mods-enabled/dir.conf
Screenshot 2021-05-25 at 12.28.06![image](https://user-images.githubusercontent.com/84720654/119506949-4d87ee80-bd66-11eb-83ad-0f910104b75b.png)
$ sudo systemctl reload apache2
$ vim /var/www/projectlamp/index.php
Screenshot 2021-05-25 at 12.29.23![image](https://user-images.githubusercontent.com/84720654/119507100-70b29e00-bd66-11eb-8c65-bcbbf38ef8d7.png)

