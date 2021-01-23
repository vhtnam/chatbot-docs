Configuration Queue and Job
==============

For Centos
1. sudo yum install redis -y
2. sudo systemctl enable redis
2. sudo systemctl start redis.service

For Redhat

1. sudo apt install redis-server
2. sudo nano /etc/redis/redis.conf
3. sudo systemctl restart redis.service

Setting Queue

1. Open Administration page.
2. Navigate to Settings page.
3. Open Queue page.
3. In the queue dropdown, select Redis.
4. Click Save.


