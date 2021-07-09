### STAGE 1: Build ###
FROM node:14 as build-deps
RUN mkdir /app
WORKDIR /app
COPY . /app
RUN npm install
CMD npm start