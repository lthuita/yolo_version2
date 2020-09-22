FROM node:latest AS BACKEND

LABEL maintainer="Luka Thuita <lthuita@gmail.com>"

WORKDIR /backend
COPY . . 

RUN npm install

EXPOSE 5000
CMD [ "npm", "start" ]