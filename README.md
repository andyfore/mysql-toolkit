# mysql-toolkit
Helper script designed to assist with common operations used to maintain and care for MySQL databases.

**Script name** mysql-toolkit

*Created* 2015-07-07

*Original Author* Andrew Fore [andy.fore@arfore.com](mailto:andy.fore@arfore.com)

**File List**

* mysql-toolkit - this is the main script file

**Usage**

The script looks for two commandline options:

-f forces the script to run even if you don't specify a password for the user.

-g indicates if you would like to dump the user grants

-u allows you to specify a username for the MySQL commands to operate as

For example, the following would specify that the grants table be dumped and that the MySQL operations be run as the root user.  If the username is not specified at runtime, then the assumption is made that the *root* user will be used.

Also, the script operations expect the use of a password.  If no password is specified during the script run then the script will exit.  To force the script to operate without a user password, use the *-f* commandline option at runtime.  Note that running the script without providing a password will generate an error if the user actually has a password.

```bash
# mysql-toolkit -g -u root
```
