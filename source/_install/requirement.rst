Server requirements
==============

.. Note:: This script can work with some cheaper shared hosting but some features is not available. So to use full featured, We recommend VPS or dedicated server

To be able to operate AMPBuilder on your own server, the server will need to meet the following requirements
 - Apache or Nginx with SSL Enabled(https)
 - PHP >= 7.2.
 - MySQL. 
 - OpenSSL PHP Extension. 
 - PDO PHP Extension. 
 - Mbstring PHP Extension
 - Tokenizer PHP Extension
 - XML PHP Extension
 - ZipArchive PHP Extension
 - Ctype PHP Extension
 - JSON PHP Extension
 - BCMath PHP Extension
 Some features like Messenger Sequence, Broadcast Schedule, Livechat, Chatbot Comment use Laravel Queue. So for better performance, we recommend you install following scripts:
 
 - Redis cache and Php-Redis extension.
 - Supervisor. 
 
 
 

