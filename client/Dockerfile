FROM node:latest AS CLIENT

LABEL maintainer="Luka Thuita <lthuita@gmail.com>"

WORKDIR /client
COPY . .  
RUN npm install
RUN npm run build
RUN npm install -g serve

EXPOSE 3000
CMD ["serve","-s", "build", "-l", "3000"]
