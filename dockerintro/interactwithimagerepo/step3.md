Push the new image to the repository

1. Tag the new image to point to the repository/registry

    `docker tag ubuntu:16.04 host01:5000/nginx-new`{{execute HOST2}}
    
2. Push the image to the repository

    `docker push host01:5000/nginx-new`{{execute HOST2}}
    
3. Stop and remove the container and then the image

    `docker stop $CID`{{execute HOST2}}
    `docker rm $CID`{{execute HOST2}}
    `docker rmi nginx-new`{{execute HOST2}}
