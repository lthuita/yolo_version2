FROM node:12.18.4-alpine3.9 AS BACKEND

LABEL maintainer="Luka Thuita <lthuita@gmail.com>"

WORKDIR /backend
COPY . . 

RUN npm install

EXPOSE 5000
CMD [ "npm", "start" ]