Run a local registry/reposotory in host 1. Install and run an nginx image on host 2
Note: Getting a docker registry with write access for this scenario was hard. So intead of a public registry we are hosting our own  private registry in the same host

1. Run the repo/registry server on the host as a docker container 
    
    `docker run -d -p 5000:5000 --restart=always --name registry registry:2`{{execute}}

2. Pull an image from the default repo, ie docker hub

    `docker pull nginx:alpine`{{execute}}

3. Run the image

    `docker run -d -p 80:80  nginx:alpine`{{execute}}
   

