# BASE IMAGE
The base image used for this project is Alpine-based node image for the backend container. The size of the Alpine image compared to other base images like ubuntu really influenced my choice becasue in this IP, it is desired to have the final image size as small as possible.

For the frontend container, latest node image was used and there was no need of the alpine or any kind of linux os since this container will depend on the backend which already has alpine.

For the mongo container, the latest mongo image was used since the database is based on mongodb

# Dockerfile directives used in the creation and running of each container
The dockerfiles were created using the recommended layers;
FROM - the source of the base image
LABEL - created only one label indicating the maintainer
WORKDIR - selected the respective working directories - that is, client and backend
COPY - that chooses the target of the commands to be executed
RUN - indicating the syntax of the commands to be run
CMD - parameters to be used while running the commands

# Git workflow 
Cloned the provided git repo into my localhost
Worked on the assignment by creatin the two dockerfiles and the dockercompose file
Edited the git remote repo 
git init - inside the project's folder
git add .
git commit -----
git push into my repo inside github
This is accessible through - https://github.com/lthuita/yolo 

# Successful running of the applications and if not, debugging measures applied.
At first, my docker-compose up failed due to the image used for the back-end container. I had used alpine:latest and the image creation was failing at the "npm install" point. I checked the logs and i realised that the npm was missing and once i changed the image source to be node:12.18.4-alpine3.9, the backend image was built successfully

The mongo container also failed to build successfully due to asigned ports. I had use the default port but the error was reading that the port is already in use. I changed and the step succeeded.
