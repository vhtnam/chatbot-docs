Custom Domain Publishing
==============
.. Note:: Login to your DNS Management, add an A record with Host Name field value @ and point to your server IP.

==============
Server config
==============
If your server hosted on a VPS or a dedicated server, make sure your sitebuilder is the default site on this server.

==============
Nginx
==============
- Open /etc/nginx/conf.d/yourdomain.conf, find the line
listen 80

- Change to
listen 80 default_server

- Restart nginx.

==============
Apache
==============
- Open /etc/httpd/conf/extra/httpd_vhost.conf, add new config
<VirtualHost *:80>
ServerAdmin webmaster@domain.com
DocumentRoot “/home/website”
</VirtualHost> 

- Restart Apache.

