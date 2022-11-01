# recipe-app-api
Recipe APP Project

*time:* 2022 Oct

## What I have done:
* Setup a project with Docker and Docker-Compose
* Configure GitHub Actions to automatically run linting and unit tests
* Write unit tests using the Django Test Framework
* Apply best practice principles including Test Driven Development
* Handle uploading media files with Django
* Customize the Django admin
* Configure a Postgres database
* Deploy the project on AWS EC2

## The correlative course on Udemy:
*Build a Backend REST API with Python & Django - Advanced:*
https://www.udemy.com/course/django-python-advanced/

## Deployment commands on linux:
https://github.com/LondonAppDeveloper/build-a-backend-rest-api-with-python-django-advanced-resources/blob/main/deployment.md#install-and-configure-depdencies

ssh-agent bash

ssh-add .\aws_id_rsa

ssh ec2-user@54.242.131.234   # Public IP will change when restart

cd recipe-app-api/

ls -al

vim .env  # change IP

docker-compose -f docker-compose-deploy.yml up

docker-compose -f docker-compose-deploy.yml run --rm app sh -c "python manage.py createsuperuser"     # create super user