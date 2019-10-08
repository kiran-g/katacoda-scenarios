Run a local registry/reposotory in host 1. Install and run an nginx image on host 2

1. Install the repo/registry in host 1
    
    `docker run -d -p 5000:5000 --restart=always --name registry registry:2`{{execute HOST1}}

2. In host 2 pull an image from the default repo, ie docker hub

    `docker pull nginx:alpine`{{execute HOST2}}

3. Run the image in host 2

    `docker run -d -p 80:80  nginx:alpine`{{execute HOST2}}
   

