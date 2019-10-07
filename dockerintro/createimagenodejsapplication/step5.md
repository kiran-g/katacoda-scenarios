Create a docker image with the nodejs application part 2

1. Create a '.dockerignore' file in the same directory as your Dockerfile
    
    `.dockerignore`{{open}} (Click here)
2. Copy the following content into the file
    <pre class="file" data-target="clipboard">
node_modules
npm-debug.log
    </pre>
3. Now build the docker image using the following command:
`docker build --tag node-web-app .`{{execute}}

4. Run this image as a container:
`docker run node-web-app`{{execute}}
