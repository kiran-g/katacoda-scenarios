Edit a file in the running container instance

1. List running containers

    `docker ps`{{execute}}
    
2. Find the container id of the most recently started container

    `docker ps -lq`{{execute}}

3. Save this container id in a variable to be used in later commands

    `CID=$(docker ps -lq)`{{execute}}
        
4. Excute the shell in the running container 

    `docker exec -it $CID   /bin/sh`{{execute}}    
    
    Note: Navigate the filesystem and view the files and processes inside the container. 
    Check the web root of the webserver
    
    `ls /usr/share/nginx/html/`{{execute}}
    
5. Create a new HTML file inside the docker container and add some random text

    `echo "WEBTEST" > /usr/share/nginx/html/index1.html`{{execute}}
    
    Note: This command is executed inside the container
    
6. Now try accessing the webpage at:

    https://[[HOST_SUBDOMAIN]]-80-[[KATACODA_HOST]].environments.katacoda.com/index1.html
    
7. Exit the docker container's shell using 'exit' command

    `exit`{{execute}}
    
    Note: Do not click this again after the container shell exists. It will kill the host shell and stop the scenario
 
8. Stop the container

    `docker stop  $CID`{{execute}}

    



