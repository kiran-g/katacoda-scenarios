Create the nodejs appliation

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

6. Create the main nodejs application file

 `files/server.js`{{open}} (Click here)

7. Copy the following code into this file

<pre class="file" data-target="clipboard">
'use strict';

const express = require('express');

// Constants
const PORT = 80;
const HOST = '0.0.0.0';

// App
const app = express();
app.get('/', (req, res) => {
  res.send('Hello world from Nodejs\n');
});

app.listen(PORT, HOST);
console.log(`Running on http://${HOST}:${PORT}`);
</pre>

8. Test the application

`node server.js`{{execute}}
