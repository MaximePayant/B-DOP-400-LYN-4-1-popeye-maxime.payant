#
# EPITECH PROJECT, 2021
# Tek2
# File description:
# Dockerfile
#

FROM python:latest

WORKDIR /app
COPY requirements.txt /app

EXPOSE 80

RUN pip3 install -r requirements.txt

COPY . /app
CMD [ "python3", "./app.py" ]