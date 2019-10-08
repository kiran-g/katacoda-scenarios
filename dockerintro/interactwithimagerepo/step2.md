Update the image

1. Find the container id of the most recently started container

    `CID=$(docker ps -lq)`{{execute HOST2}}
    
2. Create an HTML file and copy it to the running container:

    `echo "TEST" > index2.html `{{execute HOST2}}  
    
    `docker cp   index2.html $CID:/usr/share/nginx/html/`{{execute HOST2}}
    
3. Commit the changes to a new image

    `docker commit --author "Katacoda Scenario" --message "Added web page" $CID nginx-new`{{execute HOST2}}    
 

