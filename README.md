# UsefulLinksSaver

## Description
  The application is designed for comfortable using and saving browser's tabs, when you often have a lot of tabs.
  There are sorting tabs on group, comfortable control of movement between groups, preview site, adding group and tabs in the web application.

## Stack

* Python
* Django 
* Rest Framework
* React
* PostgreSQl
* Bootstrap

## Screenshots

### Main page
![Main screen](./Screenshots/main.png)

### Preview saved link
![Preview](./Screenshots/preview.png)

### Movement link to other group
![dnd](./Screenshots/dragAndDrop.png)

## Steps
### Install required components
    sudo apt-get install python3 python3-pip nodejs npm postgresql postgresql-contrib
    pip install pipenv

### Creare user and database
    sudo -u postgres psql
    CREATE DATABASE "Useful_links_db";
    CREATE USER "Useful_links_db_user" WITH PASSWORD 'Useful_links_db_user';
    ALTER ROLE "Useful_links_db_user" SET client_encoding TO 'utf8';
    ALTER ROLE "Useful_links_db_user" SET default_transaction_isolation TO 'read committed';
    ALTER ROLE "Useful_links_db_user" SET timezone TO 'UTC';
    GRANT ALL PRIVILEGES ON DATABASE "Useful_links_db" TO "Useful_links_db_user";
    \q

### Install application
    git clone https://github.com/DmitryPavlovsky/UsefulLinksSaver.git
    cd UsefulLinkSaver/
    pipenv install --three
    pipenv shell
    cd backend
    python manage.py makemigrations
    python manage.py migrate
    python manage.py runserver
    cd ../frontend/
    npm install 
    npm start

### Run frontend test 
    cd frontend
    npm test

### Run backend test 
    cd backend
    python manage.py test