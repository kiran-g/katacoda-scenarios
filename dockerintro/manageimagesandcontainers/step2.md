Manage the running container instance
1. List running containers

    `docker ps`{{execute}}
    
2. Fine the container id 

    `CID=$(docker ps -lq)`{{execute}}
    
3. Excute shell in running contexainer 

    `docker exec -it $CID   /bin/sh`{{execute}}    
    
    Note: Navigate the flesysten and view the files and processes



