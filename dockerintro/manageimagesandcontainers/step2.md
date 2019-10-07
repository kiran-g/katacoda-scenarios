Manage the running container instance
1. List running containers

    `docker ps`{{execute}}
    
2. Find the container id 

    `CID=$(docker ps -lq)`{{execute}}
    
3. Excute shell in running contexainer 

    `docker exec -it $CID   /bin/sh`{{execute}}    
    
    Note: Navigate the flesysten and view the files and processes
4. Edit the default HTML file inside the docker container

    `vi /usr/share/nginx/html/index.html`{{execute}}
5. Now try accessing the webpage at:

    https://[[HOST_SUBDOMAIN]]-80-[[KATACODA_HOST]].environments.katacoda.com/index.html



