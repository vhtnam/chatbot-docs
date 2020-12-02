Creating a new database
==============
First thing you want to do before installing AMPBuilder is to create a new database on your mysql server. If you already know how to do this/or have already created one just skip to the next step.




==============
cPanel
==============
 - Log into cPanel.
 - Under Databases, click MySQL Databases.
 - In the New Database field, type a name for the database.
 - Click Create Database.
 - Click Go Back. 
 
==============
phpMyAdmin
==============
 - Log into phpMyAdmin.
 - Click on the database tab in the top menu.
 - Enter the name you want to call your new database.
 - Click "Create" and then you're done!
 
==============
Linux Command line
==============

First we’ll login to the MySQL server from the command line with the following command:

	mysql -u root -p

In this case, I’ve specified the user root with the -u flag, and then used the -p flag so MySQL prompts for a password. Enter your current password to complete the login.

If you need to change your root (or any other) password in the database, then follow this tutorial on changing a password for MySQL via the command line.

You should now be at a MySQL prompt that looks very similar to this:

	mysql>

To create a database with the name tutorial_database type the following command:

CREATE DATABASE amp_database;

If a database of the same name already exists, then a new database will not be created and you’ll receive this error:

ERROR 1007 (HY000): Can't create database 'amp_database'; database exists

To avoid seeing this error use the following command instead:

CREATE DATABASE IF NOT EXISTS amp_database;

The above command will only create the database amp_database if a database of that name does not already exist.