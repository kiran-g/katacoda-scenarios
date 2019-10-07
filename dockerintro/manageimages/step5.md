Create a docker image with the nodejs application part 2

1. Create a '.dockerignore' file in the same directory as your Dockerfile
    
    `.dockerignore`{{open}} (Click here)
2. Copy the following content into the file
<pre class="file" data-target="clipboard">
node_modules
npm-debug.log
</pre>

4. Return to the main directory
    
    `cd ..`{{execute}}
    
3. Now build the docker image using the following command:

    `docker build --tag node-web-app .`{{execute}}

4. Run this image as a container:

    `docker run -p 80:80 node-web-app`{{execute}}
    
9. Access the sample webapp in browser

    https://[[HOST_SUBDOMAIN]]-80-[[KATACODA_HOST]].environments.katacoda.com/
