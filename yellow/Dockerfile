###################################################################
# This is templating file of Dockerfile. It will help you to      #
# complete all required instructions for building the Dockerfile. #
###################################################################

# 1.1.1 | Use the following base image "node:17.0-alpine3.14"
FROM node:17.0-alpine3.14
# 1.1.2 | Working directory inside the containers should be "/app"
WORKDIR /app
# 1.1.3 | Copy "package*.json" file(s) to working directory
COPY package*.json /app
# 1.1.4 | Install "npm=7.17.0-r0" package manager, then install dependency packages
#Alphine Linux usa apk no apt-get
RUN apk update && apk upgrade && npm install -g npm@7.17.0 && npm install 
# 1.1.5 | Copy "app.js" file to working directory
COPY app.js /app
# 1.1.6 | Copy the "index.pug" and "favicon.ico" files to the "/app/views" directory
RUN mkdir -p /app/views
COPY index.pug /app/views
COPY favicon.ico /app/views
# 1.1.7 | The port "80" should be exposed by the container
EXPOSE 80
# 1.1.8 | The container must execute the command "node app.js" in run time
CMD ["node", "app.js"]

