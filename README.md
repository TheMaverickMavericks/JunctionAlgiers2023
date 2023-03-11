# JunctionAlgiers2023
The Mavericks team repo for Junction Algiers 2023 Hackathon, Kyo Conseil Challenge


Repo Code for Generating Micro Services Features : https://github.com/S-Amine/micro_django
Repo Code for Live Streaming Kyo ChatGpt Server : https://github.com/ahmedtouahria/kyo-chatgpt-live-streaming
Repo Code for Kyo ChatGpt Chrome Extension : [22:05, 3/11/2023] Ahmed Twhria: https://github.com/ahmedtouahria/kyo-chatgpt-chrome-extension
Repo Code for Email Service Server : https://github.com/S-Amine/email_service
Repo Code for Mobile Application Kyo : https://github.com/AbdeldjalilChougui/kyo_challenge

Youtube video for the project : https://www.youtube.com/watch?v=YsBYEUN4tok

Kyo Assistant Ux Study : https://drive.google.com/file/d/1rsnk4Uyk_YVxjOM5agvnMl2rNuPTe5nO/view

Miro High Level Architecture : https://miro.com/app/board/uXjVPiDTivc=/



This project provides a prototype of a cookiecutter Django template for quickly creating microservices. It uses RabbitMQ for communication, Django for backend logic, Celery for background tasks, Supervisorctl, Gunicorn, the Pika library, and Postgres. We invite you to use it and contribute.

Custom Django command to run Rabbitmq consumer: ./manage.py rabbitmq_consume which is persistent and attempts to reconnect if something goes wrong.
Script for auto deployment in production: installer.py in a fresh Ubuntu server which the user has to input data in. The script installs OS dependencies, Python libraries in a virtualenv, installs Postgres and creates the user and the database, creates Supervisor conf files, generates .env file, and runs the processes in the background.
Django app to interact with the Rabbitmq broker.
File called messages.py to consume messages from the Rabbitmq.
Integration for Celery that makes the import of the Celery application via the celery_app variable.
Load task modules from all registered Django apps, autodiscover from tasks.py files inside Django apps.
RabbitMq and Celeries settings from the Django setting file.
Bash script called start_celery_worker.sh to start celery worker faster in the development stage.
Bash script called start_rabbitmq_consumer.sh to start the rabbitmq message consumer quickly in the development stage.
