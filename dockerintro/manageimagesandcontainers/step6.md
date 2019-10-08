Mount  a volume with the container

1. Create a new directory at "/root/volume"

    `mkdir /root/volume`{{execute}}
    
2. Create an HTML file inside it

    `echo "VOLUMETEST" > /root/volume/index3.html`{{execute}}
    
3. Run the new image again with t

    `docker run -d -p 80:80 -v /root/volume/:/usr/share/nginx/html/  nginx-new`{{execute}} 

4. Verify the webpage at:

    https://[[HOST_SUBDOMAIN]]-80-[[KATACODA_HOST]].environments.katacoda.com/index3.html 
 
5. Stop the conatiner 

    `docker stop  $(docker ps -lq)`{{execute}}

6. Remove the conatiner 

    `docker rm  $(docker ps -lq)`{{execute}}     
