Create a docker image with the nodejs application part 1

1. Create an empty Dockerfile

    `Dockerfile`{{open}} (Click here)
 
2. Copy the following code into it:

    <pre class="file" data-target="clipboard">
    FROM node:10

    # Create app directory
    WORKDIR /usr/src/app

    # Install app dependencies
    # A wildcard is used to ensure both package.json AND package-lock.json are copied
    # where available (npm@5+)
    COPY package*.json ./

    RUN npm install
    # If you are building your code for production
    # RUN npm ci --only=production

    # Bundle app source
    COPY . .

    EXPOSE 8080
    CMD [ "node", "server.js" ]
    </pre>




