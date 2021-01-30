Installing Supervisor
==============

.. Note:: If you don't have root access to your server, ignore this section.

==============
For Centos
==============
Running following commands:
1. Installing 

.. code-block:: console

	yum install supervisor

2. vim /etc/supervisord.conf edit section program as following:


.. code-block:: console

	[program:laravel-worker]
	command=php /path_to_source_folder/artisan queue:work 
	process_name=%(program_name)s_%(process_num)02d
	numprocs=8 
	priority=999 
	autostart=true
	autorestart=true  
	startsecs=1
	startretries=3
	user=apache
	redirect_stderr=true
	stdout_logfile=/path/to/log/worker.log
	
3. Auto run

.. code-block:: console

	systemctl enable supervisord to autorun at start

4. Start the service

.. code-block:: console

systemctl restart supervisord to restart the service

==============
For Redhat/Debian
==============
1. Installing

.. code-block:: console

	sudo apt-get install supervisor

2. Configuration

Supervisor configuration files are typically stored in the /etc/supervisor/conf.d directory. Within this directory, you may create any number of configuration files that instruct supervisor how your processes should be monitored. For example, let's create a laravel-worker.conf file that starts and monitors queue:work processes:


.. code-block:: console

	[program:laravel-worker]
	process_name=%(program_name)s_%(process_num)02d
	command=php /path_to_source_folder/artisan queue:work --sleep=3 --tries=3 --max-time=3600
	autostart=true
	autorestart=true
	stopasgroup=true
	killasgroup=true
	user=forge
	numprocs=8
	redirect_stderr=true
	stdout_logfile=/path_to_source_folder/worker.log
	stopwaitsecs=3600


| In this example, the numprocs directive will instruct Supervisor to run eight queue:work processes and monitor all of them, automatically restarting them if they fail. You should change the command directive of the configuration to reflect your desired queue connection and worker options.


| For more information on Supervisor, consult the Supervisor documentation.

3. Final 

.. code-block:: console

	sudo supervisorctl reread
	sudo supervisorctl update
	sudo supervisorctl start laravel-worker:*

