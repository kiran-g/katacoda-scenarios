Update the image

1. Find the container id of the most recently started container

    `CID=$(docker ps -lq)`{{execute}}
    
2. Create an HTML file and copy it to the running container:

    `echo "REPOTEST" > index2.html `{{execute}}  
    
    `docker cp   index2.html $CID:/usr/share/nginx/html/`{{execute}}
3. Verify by accessing the webpage at:

    https://[[HOST_SUBDOMAIN]]-80-[[KATACODA_HOST]].environments.katacoda.com/index2.html   
    
4. Commit the changes to a new image

    `docker commit --author "Katacoda Scenario" --message "Added web page" $CID nginx-new`{{execute}}    
 

