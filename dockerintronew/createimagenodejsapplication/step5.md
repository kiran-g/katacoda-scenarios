Create a docker image with the nodejs application part 2

1. Create a '.dockerignore' file in the same directory as your Dockerfile
    
    `.dockerignore`{{open}} (Click here)
    
    Note: This file specifies the files which needs to be skipped when copying files to the image
    
2. Copy the following content into the file

<pre class="file" data-target="clipboard">
node_modules
npm-debug.log
</pre>

4. Return to the main directory
    
    `cd ..`{{execute}}
    
3. Now build the docker image using the following command:

    `docker build --tag node-web-app .`{{execute}}

4. Verify using docker command
    
    `docker images`{{execute}}

5. Run this image as a container:

    `docker run -p 80:80 node-web-app`{{execute}}
    
    Note: "-p 80:80" option, maps port 80 from inside the container to the host port 80, thus exposing the application outside the container
    
6. Access the sample webapp in browser

    https://[[HOST_SUBDOMAIN]]-80-[[KATACODA_HOST]].environments.katacoda.com/
