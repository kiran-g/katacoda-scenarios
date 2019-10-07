Create a docker image with the c application

Create an empty Dockerfile
 `Dockerfile`{{open}} (Click here)
 
Copy the following code into it:
FROM scratch
ADD hello /
CMD ["/hello"]
</pre>

Now build the docker image using the following command:
`docker build --tag hello .`{{execute}}

