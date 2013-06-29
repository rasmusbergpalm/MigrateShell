MigrateShell
============

Really really simple migrations for CakePHP
# Why?
 Database migrations is a non-trivial problem in any application. There are tons of CakePHP plugins/shells/scripts for handling it, but most revolve around the idea of schemas. Schemas are great in theory but I've found them lacking in reality. What I really wanted was to be able to control exactly what happened when I ran my migrations, with as little CakePHP magic involved as possible.
 
# How?

MigrateShell is extremely simple: It runs a set of SQL scripts in the correct order, and keeps track of what has been migrated. When you want to do a migration, simply create a SQL script, put it in the migrations folder and run the shell.

 - Download MigrateShell.php and place it in app/Console/Command/MigrateShell.php
 - Create a folder app/Config/Schema/migrations
 - Place your SQL migration scripts in that folder, with a sequential naming scheme, e.g. '1.sql, 2.sql ... 12.sql' or '20120521162532-init.sql, 20130629130510-upgrade.sql', etc.
 - ``` $cake migrate ```