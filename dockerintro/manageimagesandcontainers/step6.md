Mount  a volume with the container

1. Create a new directory at "/root/code/volume" in the host machine

    `mkdir /root/code/volume`{{execute}}
    
2. Create an HTML file inside it

    `volume/index3.html`{{open}} (Click here to create the file and then add some text) 
    
3. Run the new image again with the this host directory mounted as a volume on the nginx  web root of the container 

    `docker run -d -p 80:80 -v /root/code/volume/:/usr/share/nginx/html/  nginx-new`{{execute}} 

4. Verify the webpage at:

    https://[[HOST_SUBDOMAIN]]-80-[[KATACODA_HOST]].environments.katacoda.com/index3.html 
 
5. Stop the conatiner 

    `docker stop  $(docker ps -lq)`{{execute}}

6. Remove the container 

    `docker rm  $(docker ps -lq)`{{execute}}     
 
7. Remove the image 

    `docker rmi  nginx-new`{{execute}}
 
8. Verify in image list to confirm that the image is removed

    `docker images`{{execute}}
