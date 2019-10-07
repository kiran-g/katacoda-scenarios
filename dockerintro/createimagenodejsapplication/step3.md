Create the nodejs appliation Part 2


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
    
9. Access the sample webapp in browser

    https://[[HOST_SUBDOMAIN]]-80-[[KATACODA_HOST]].environments.katacoda.com/
    
10. Press CTRL+C in the terminal window to kill the nodejs app to continue
    
    `clear`{{execute}}
