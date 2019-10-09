Pull the new image from the local repository

1. Pull the new image

    `docker pull localhost:5000/nginx-new`{{execute}}
 
2. Run the image

    `docker run -d -p 80:80  localhost:5000/nginx-new`{{execute}}
    
3. Verify by accessing the webpage at:

    https://[[HOST_SUBDOMAIN]]-80-[[KATACODA_HOST]].environments.katacoda.com/index2.html 
