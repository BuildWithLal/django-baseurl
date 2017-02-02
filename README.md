For configurations we are folloing 12factor to keep configurations out of GIT repository
https://12factor.net/

Our Configurations i.e secret_key, debug, smtp settings, database credentials etc are in config/.env file

We are using django-environ to read .env file and keep configurations in environment variables

To Deploy a project locally or on production we are using Python Fabric
http://www.fabfile.org/


