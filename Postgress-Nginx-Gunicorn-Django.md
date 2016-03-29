


##How To Install and Configure Django with Postgres, Nginx, and Gunicorn  

Before anything else, make sure all packages installed are upto date. Root to your directory and run:  
        
        sudo apt-get update  
        
        sudo apt-get upgrade  
        
        
###Install and create a viretual Environment  
Installing vthe viretual env is quite simple. Just run the following command:  
        sudo apt-get install python-virtualenv  
        
 Now create the virtual env with a name of your choice, I suggest one related to the current project.  
        
        sudo virtualenv /<root folder>/<virtualenv name>  
        
A directory will be created with the environment name.  


###Install Django  
Activate the virtual environment so as to install packages needed for the project  
        source ./<env name>/bin/activate  
        
We can now install Django with the virtual env active. To do this, we'll use **pip** a Python package manager much like Easy install. Here's the commnad you'll run:  

        pip install Django  
        
Getting errors o using pip?  
This should Do;  
        sudo apt-get install python-pip  
        
        
 
        
###Install PostgreSQL  

Most Django Devs prefer PostrgeSQL as their database server. It's much more robust than MySQL and it works well with the Django ORM.  
We won't be needing the virtual environment for this step, run the following command to deactivate:  
        deactivate
        
First off we have to install dependaencies for PostrgeSQL to work with Django with the command:  
        
        sudo apt-get install libpq-dev python-dev
        
  Then istall PostrgeSQL like so:   
        
        sudo apt-get install postgresql postgresql-contrib  
        
We're now ready to roll!   


###Install NGINX  
NGINX is and incredibly fast and light-weight web server. We will use it to serve up our static files for our Django app.  

        sudo apt-get install nginx
        