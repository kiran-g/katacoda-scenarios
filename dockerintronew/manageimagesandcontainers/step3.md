Commit changes made to a running container  part 1

1. Run the image again     

    `docker run -d -p 80:80  nginx:alpine`{{execute}}
 
2. Find the container id 

    `CID=$(docker ps -lq)`{{execute}}
    
3. Check if the HTML file we created in the previous step still exists by running ls command inside the container

    `docker exec -it $CID   ls /usr/share/nginx/html/index1.html`{{execute}}  
    
    Note: The file will be missing as the changes we made to the previous container instance was not committed back to the image
     
4. Create an HTML file and copy it to the running container:

    `index2.html`{{open}} (Click here to create the file and then add some text)  
    
    `docker cp   code/index2.html $CID:/usr/share/nginx/html/`{{execute}}
    
5. Verify the webpage at:

    https://[[HOST_SUBDOMAIN]]-80-[[KATACODA_HOST]].environments.katacoda.com/index2.html
