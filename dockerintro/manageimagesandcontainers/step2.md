Manage the running container instance
1. List running containers

    `docker ps`{{execute}}
    
2. Find the container id 

    `CID=$(docker ps -lq)`{{execute}}
    
3. Excute shell in running contexainer 

    `docker exec -it $CID   /bin/sh`{{execute}}    
    
    Note: Navigate the flesysten and view the files and processes
4. Create a new HTML file inside the docker container and add some random text

    `echo "WEBTEST" > /usr/share/nginx/html/index1.html`{{execute}}
    
5. Now try accessing the webpage at:

    https://[[HOST_SUBDOMAIN]]-80-[[KATACODA_HOST]].environments.katacoda.com/index1.html



