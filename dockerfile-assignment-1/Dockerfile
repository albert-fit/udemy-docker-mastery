#Based on the official Node image with the Alpine branch
FROM node:6-alpine

#expose port 3000
EXPOSE 3000
# Update the apk package manager and install tini
RUN apk add --update tini 

RUN mkdir -p /usr/src/app 

WORKDIR /usr/src/app

#copy the package.json file to the working directory
COPY package.json package.json

#install the dependencies and clean the cache
RUN npm install && npm cache clean

#copy the rest of the application to the working directory
COPY . .

#run the application
CMD ["tini", "--", "node", "./bin/www"]




# NOTE: The instructions are now in the README.md file in this directory.
