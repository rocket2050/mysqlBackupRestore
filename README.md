Role Name
=========

This role takes mysql backup including all cases(Full, Single database, Single table in a database) and restores it, further uploads backup to S3 bucket

Assumption
--------------

Aws Cli is pre-installed on the mysql server

Role Variable
------------

mySql_backup_file: "/opt/backup.sql"

mySql_userName: "root"

mySql_password: "opstree123"

mySql_databaseName: "opstree"

mySql_tableName: "DevOps"

backup_dir: "/opt/"

s3_bucket_name: "backupMysql"

full_data_backup: "true"

database_backup: "false"

table_backup: "false"

restore_backup: "true"

restore_database: "false"

Here if you want to backup mysql only then set full_data_backup as "true" and other as false, accordingly you can set other parameter as true or false depending on your need.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

- hosts: mysql_hosts
  roles:
     - { role: sandy724.MYSQLBackupRestorer }

License
-------

BSD

Author Information
------------------
www.opstree.com

blog.opstree.com
