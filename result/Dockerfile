#
# EPITECH PROJECT, 2021
# Tek2
# File description:
# Dockerfile
#

FROM node:12-alpine

WORKDIR /app
COPY package*.json ./

EXPOSE 80

RUN npm install

COPY . /app
CMD [ "node", "server.js" ]