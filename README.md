# Django-REST-React-App
A template repo using Django REST API for the backend and React App as the frontend.


# How it works?
This repo is based on our Django-REST-API-Template repo. Here, we create a new React app called "ui" that will talk to the Django backend using REST APIs.

Since this is a demo project, our objective here is simple. We will create a simple React component that will read data from the SQLite DB and display them out to the end user.

# How to run?
    Step 1: Clone the repo
            git clone https://github.com/digitallyamar/Django-REST-React-App.git
            cd Django-REST-React-App

    Step 2: Create Python virtual environment
            python3 -m venv venv
            source venv/bin/activate
			pip install django djangorestframework

	Step 3: Run webpack to build React app "ui" using command:
			cd ui
			npm init -y
			npm i webpack webpack-cli --save-dev
			npm i @babel/core babel-loader @babel/preset-env @babel/preset-react --save-dev
			npm i react react-dom --save-dev
			npm run dev

	Step 3:	Run our Django server using the command:
			cd ../
			python3 manage.py migrate
            python3 manage.py runserver

			Your React App should be ready and running at:
			http://127.0.0.1:8000/

			But you will find the window empty as you have not yet added any content to your DB.
			So go ahead and add some data first:
			http://127.0.0.1:8000/api/todo

# Using MongoDB with Django
In order to use MongoDB with Django, we will make use of a Python library called Djongo. Djongo will act as a translator layer between the SQL queries to the MongoDB queries and helps us to continue using the default Django ORM.

To keep our Django REST React App code available for both SQLite DB and MongoDB, we have created a separate branch to work with MongoDB. This new branch is simply called Djongo. 

So switching between main branch and the Djongo branch of this repo will switch the type of DB used.
