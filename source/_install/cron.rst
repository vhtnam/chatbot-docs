Cron Job
==============

| Create a new cron job follow this syntax
| 
| * * * * * path_to_php_script/php /path_to_source_folder/artisan schedule:run >> /dev/null 2>&1
| 
| path_to_php_script: path to PHP Execute File
| path_to_source_folder: path to root folder where you install this script