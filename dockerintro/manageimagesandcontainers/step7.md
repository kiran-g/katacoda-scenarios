Start a container from the new image

1. Check the history of the new image

    `docker history nginx-new`{{execute}}

2. Run the new image

    `docker run -d -p 80:80  nginx-new`{{execute}}    
    
3. Verify that the changed commited to the image is available in the container

    https://[[HOST_SUBDOMAIN]]-80-[[KATACODA_HOST]].environments.katacoda.com/index2.html
   
4. Stop the conatiner 

    `docker stop  $(docker ps -lq)`{{execute}}

5. Remove the conatiner 

    `docker rm  $(docker ps -lq)`{{execute}}      


