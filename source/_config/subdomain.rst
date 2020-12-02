Subdomain Publishing
==============
.. Note:: Login to your DNS Management, add an A record with Host Name field value * and point to your server IP.

==============
Nginx
==============
- Open /etc/nginx/conf.d/yourdomain.conf, find the line
server_name yourdomain

- Change to
server_name yourdomain *.yourdomain

- Restart nginx.

==============
Apache
==============
- Open /etc/httpd/conf/extra/httpd_vhost.conf, add new config
ServerAdmin webmaster@domain.com
DocumentRoot “/home/website”
ServerName domain.com
ServerAlias *.domain.com

- Restart Apache.

==============
cPanel
==============
- Login to cPanel.
- Navigate to the menu ‘Subdomains’ under ‘Domains’ section.
- Create a subdomain‘*’ pointing it to the necessary folder ( you will need to specify the path in the field ‘Document Root’ ).

