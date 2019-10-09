Create a docker image with the c application

1. Create an empty Dockerfile

    `Dockerfile`{{open}} (Click here)
 
    Note: Dockerfile contains the instructions to create an image
 
2. Copy the following code into it:

<pre class="file" data-target="clipboard">
#This is the base image to be used when an image is made from scratch 
FROM scratch

#Add the executable to the image
ADD hello /

#Set the default command to be run when this image is run as a container  
CMD ["/hello"]
</pre>

3. Now build the docker image using the following command with name "hello":

    `docker build --tag hello .`{{execute}}

4. Verify using docker images command
    
    `docker images`{{execute}}
    
5. Run this image as a container:

    `docker run hello`{{execute}}


