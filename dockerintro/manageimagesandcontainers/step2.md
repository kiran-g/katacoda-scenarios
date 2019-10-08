Edit a file in the running container instance
1. List running containers

    `docker ps`{{execute}}
    
2. Find the container id of the most recently started container

    `CID=$(docker ps -lq)`{{execute}}
    
3. Excute shell in the running container 

    `docker exec -it $CID   /bin/sh`{{execute}}    
    
    Note: Navigate the filesystem and view the files and processes inside the container
    
4. Create a new HTML file inside the docker container and add some random text

    `echo "WEBTEST" > /usr/share/nginx/html/index1.html`{{execute}}
    
    Note: This command is executed inside the container
    
5. Now try accessing the webpage at:

    https://[[HOST_SUBDOMAIN]]-80-[[KATACODA_HOST]].environments.katacoda.com/index1.html
    
6. Exit the docker container's shell using 'exit' command

    `exit`{{execute}}
 
7. Stop the container

    `docker stop  $CID`{{execute}}

    



