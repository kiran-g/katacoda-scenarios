Push the new image to the repository

1. Tag the new image to point to the repository/registry

    `docker tag nginx-new localhost:5000/nginx-new`{{execute}}
    
2. Push the image to the repository

    `docker push host01:5000/nginx-new`{{execute}}
    
3. Stop and remove the container and then the image

    `docker stop $CID`{{execute}}
    `docker rm $CID`{{execute}}
    `docker rmi nginx-new`{{execute}}
