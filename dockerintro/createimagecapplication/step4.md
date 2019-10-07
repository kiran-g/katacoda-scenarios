Create a docker image with the c application

1. Create an empty Dockerfile

    `Dockerfile`{{open}} (Click here)
 
2. Copy the following code into it:

<pre class="file" data-target="clipboard">
FROM scratch
ADD hello /
CMD ["/hello"]
</pre>

3. Now build the docker image using the following command:

    `docker build --tag hello .`{{execute}}

4. Verify using docker command
    
    `docker images`{{execute}}
    
5. Run this image as a container:

    `docker run hello`{{execute}}


