**Under construction...**

# PyMysqlDump
Small python scripts, which try to make a fast mysql dump (and load), whose ouput is optimized for git usage

# Install PyMysqlDump
The scripts are using python (so you need a python interpreter: see https://www.python.org). Additionally, you need two pacakges:

* mysql-connector-python (https://pypi.org/project/mysql-connector-python/)
* myloginpath (https://pypi.org/project/myloginpath/)

Please install them with the following commands:

```
pip install mysql-connector-python
pip install myloginpath
```

You need to create a `client.cnf` mysql configuration file, which stores the crediantials of an administrator account. These encrypted access information are used by the PyMysqlDump scripts to dump your database as well as load the database from an existing dump. To do this, please use the following command:

```
mysql_config_editor set --login-path=client --host=localhost --user=<USER> --password
```
_The script `mysql_config_editor` is located in the **bin** subdirectory of your mysql location_ 

Currently, this script is only working, if you execute the script on the host, where your mysql server is running. In addition, you must ensure, that your mysql server was called without the `--secure-file-priv` option. 
