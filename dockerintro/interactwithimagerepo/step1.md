Install and run an image

1. Pull an image from the default repo, ie docker hub

    `docker pull nginx:alpine`{{execute HOST2}}

2. Run the image

    `docker run -d -p 80:80  nginx:alpine`{{execute HOST2}}
   
3. Test the webserver

    https://[[HOST_SUBDOMAIN]]-80-[[KATACODA_HOST]].environments.katacoda.com/index.html


