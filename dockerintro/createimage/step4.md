Create a docker image with the c application

Create an empty Dockerfile
 `Dockerfile`{{open}} (Click here)
 
Copy the following code into it:
<pre class="file" data-target="clipboard">
FROM scratch
ADD hello /
CMD ["/hello"]
</pre>

Now build the docker image using the following command:
`docker build --tag hello .`{{execute}}

Run this image as a container:
`docker run hello`{{execute}}


