## [Flask_init](https://github.com/imxana/Flask_init)

A simple flask framework, for B/S web application. 

### Function

* Background management system

* Enable Cors support on all routes, for all origins and methods. 

* SQL-database friendly Supported


### Quick start

Install denpendences:

    pip3 install -r requirements.txt

If you want to use 'flask [command]', set env:

    source deploy.sh

Initialize the database:

    flask initdb
    flask testdb

(If you want to use MySQL db not sqlite, before `flask initdb` set the `SQLALCHEMY_DATABASE_URI`, and make sure the database is existed.)

Then run the Server:

    flask run

Open a browser access to `http://localhost:5000/` and `http://localhost:5000/admin/` to visit your website.


### Global config

Just edit the 'config.py' file, 'Development' as the default.

### Some possible problems

1. Flask command error

This is maybe because two Python were installed in your Mac, and some problem will be remained. 

An eazy way to solve it is to locate and edit the Flask script file `vim $(which flask | head -1)`. And add the python(3) path on the top, for my example:

    #!/usr/local/bin/python3
    #!/usr/local/opt/python/bin/python2.7
    ...

### LICENSE

MIT
