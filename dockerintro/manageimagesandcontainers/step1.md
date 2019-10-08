Docker install and run nginx webserver image and view the default webpage 

1. List local images

    `docker images`{{execute}}

2. Pull nginx(a lightweight static webserver) webserver image 

    `docker pull nginx:alpine`{{execute}}
    
3. Verify that the new image is downloded    

    `docker images`{{execute}}

4. Inspect the image

    `docker image inspect  nginx:alpine`{{execute}}
  
5. Check the history of the image

    `docker history nginx:alpine`{{execute}}
    
    Note: This shows the commit history of this image
    
4. Run the image        

    `docker run -d -p 80:80  nginx:alpine`{{execute}}
 
5. Access the sample webpage in browser

    https://[[HOST_SUBDOMAIN]]-80-[[KATACODA_HOST]].environments.katacoda.com/index.html


