Create the nodejs appliation Part 1

1. First 'cd' into the code directory

    `cd /root/code`{{execute}}

2. Create the nodejs application folder

    `mkdir files; cd files`{{execute}}
 
3. Create 'package.json' file 

    `files/package.json`{{open}} (Click here)

4. Copy the following code into this file

<pre class="file" data-target="clipboard">
{
"name": "docker_web_app",
"version": "1.0.0",
"description": "Node.js on Docker",
"author": "First Last <first.last@example.com>",
"main": "server.js",
"scripts": {
"start": "node server.js"
},
"dependencies": {
"express": "^4.16.1"
}
}
</pre>

5. Install the npm dependencies 

    `npm install`{{execute}}


