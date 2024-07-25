# Docker-Python

# Setup Python for Django (virtual environment with venv)
1) Check Python Version : python3 -V
2) Set Python Virtual Environment
3) apt install python3.10-venv
4) python3 -m venv ~/env/dj  ( in our home direc we are creating folder and calling our virtual env dj)
5) Now in your home directory you will see a virtual environment "env" is created and inside dj are packages and libraries are present(goto cd ~ and do ls)

# Changing Python version to our Virtual enviornment Python
1) when you fire "which python3" nawazali_atwork@docker:~$ which python3
/usr/bin/python3
2) To activate the python from our virtual env, there is activate script in env/dj/bin that tells to activate python fire this command :source env/dj/bin/activate
3) If you want to deactivate python form our virtual env, type deactivate

# creating Django project
1) pip install django
2) create django project "django-admin startproject crud" (crud is the project name)
3) Inside crud folder there will bunch of .py files
4) Set up Development Server: Use manage.py file, firing the command shows the url where it will be hosted > python manage.py runserver
5) Because I am running this in vm and not my mac, i need to tell django so that i can load traffic from anywhere. > python manage.py runserver 0.0.0.0:8000
6) Now when you goto browser and do ipadrsofvmmachine:8000 it throws error as DisallowedHost at /
Invalid HTTP_HOST header: 'ipadrsofvmmachine:8000'. You may need to add 'ipadrsofvmmachine' to ALLOWED_HOSTS
7) To fix the above error goto crud folder > crud folder> settings.py. Add the ip addressed in "Allowed Host" field.

# Creating A basic Website in Python Using Django
1) Create the App called Score( do this inside the project folder which is crud): django-admin startapp score
2) the View.py will the file where you can write what your landing page shoud have
3) Modify the urls.py in score and crud folders.
4) fire  python manage.py runserver 0.0.0.0:8000 and open the browser

# Creating Requirement.txt File for docker to install needed packages
1) You would need requirement.txt file having all the mandatory packages like django installed.Libraries and packages in that project, its advisable to have virtual environment so that it takes only needed packages
You can do this by the following: pip3 freeze -l > requirements.txt
