# UdacityFullstackServerConfiguration
Server information for AWS Lightsail project hosting an anime fan site

---
## Server Info
IP address: 52.1.134.59

SSH port: 2200

---
## URL
[http://ec2-52-1-134-59.compute-1.amazonaws.com/](http://ec2-52-1-134-59.compute-1.amazonaws.com/)

---
## Software Used
[Amazon Lightsail](https://amazonlightsail.com/) - hosting

[Ubuntu](https://www.ubuntu.com/) - OS

[Flask](http://flask.pocoo.org/) - microframework for Python based on Werkzeug and Jinja 2

[SQL Alchemy](http://www.sqlalchemy.org/) - SQL toolkit and Object Relational Mapper

[Google OAuth 2.0 Client](https://github.com/google/oauth2client) - Python library for accessing resources protected by OAuth 2.0

[PostgreSQL](https://www.postgresql.org/) - object-relational database system

[Appache2](https://httpd.apache.org/) - HTTP server

[mod_wsgi](https://modwsgi.readthedocs.io/en/develop/) - Apache module which can host any Python web application which supports the Python WSGI specification

---
## Configuration

Amazon Lightsail

* Change the SSH port from 22 to 2200 locally and update Lightsail settings by updating /etc/ssh/sshd_config
* Set up Uncomplicated Firewall (UFW) to only allow incoming connections for SSH (port 2200), HTTP (port 80), and NTP (port 123)

Ubuntu

* Create a new user account
* Give that account the permission to sudo
* Create an SSH key pair for that account using ssh-keygen

PostgreSQL

* Create a new database user with limited permissions
* Run database setup and seed files to populate database and tables

Appache2

* Configure Apache to handle requests using the WSGI module
* Set path to project folder on local machine so the server can find the resources

mod_wsgi

* Create wgi file for importing project as an application that can be served


---
## Resources and Support

Github - Google OAuth 2.0

Stackoverflow

[Flask documentation](http://flask.pocoo.org/docs/0.12/deploying/mod_wsgi/) - configuration of Appache2 with mod_wsgi

[Lightsail documentation](https://amazonlightsail.com/docs/) - server configuration, setting routes, SSH, creation of user keys

Udacity - Lightsail setup, creating users, configuring UFW for different ports and protocols
