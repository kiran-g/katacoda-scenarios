Commit changes made to a running container part 2

1. Commit the changes to a new image

    `docker commit --author "Katacoda Scenario" --message "Added web page" $CID nginx-new`{{execute}}

2. Check the container details

    `docker inspect  $CID`{{execute}}

3. Stop the container

    `docker stop  $CID`{{execute}}
    
3. Check the container status

    `docker ps -a | grep  $CID`{{execute}}
 
4. Remove the container 

    `docker rm  $CID`{{execute}}

3. Check the container status again and confirm that the conatiner is removed

    `docker ps -a | grep  $CID`{{execute}}
