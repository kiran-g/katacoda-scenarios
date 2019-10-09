Create a docker image with the nodejs application part 1

1. Create an empty Dockerfile

    `Dockerfile`{{open}} (Click here)
 
2. Copy the following code into it:

<pre class="file" data-target="clipboard">
#Base image is node:10. Rest of the instructions below are for changes on top of this base image
FROM node:10

# Create app directory
WORKDIR /usr/src/app

#Copy the package dependency files
COPY files/package*.json ./

#Install the dependncies to the image being created
RUN npm install

# Bundle remaining files includeing the server app file
COPY files/ .

#Expose port 80 in the container to the outside world
EXPOSE 80

#Set the nodejs server application as the default command to be run when this image is run as a container
CMD [ "node", "server.js" ]
</pre>




