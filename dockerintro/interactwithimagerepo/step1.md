Run a local registry/reposotory in the host machine. Install and run an nginx image on the same host

Note: Getting the credentials with write access for a public docker registry  for this scenario was hard. So instead we are hosting our own  private registry in the same host

1. Run the repo/registry server on the host as a docker container (pull from  dockerhub)
    
    `docker run -d -p 5000:5000 --restart=always --name registry registry:2`{{execute}}

2. Pull an nginx (a lightweight static webserver) image from the default repo, ie dockerhub

    `docker pull nginx:alpine`{{execute}}

3. Run the image

    `docker run -d -p 80:80  nginx:alpine`{{execute}}
   

