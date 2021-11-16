```
Node JS:
    Install Node js on local VM.
    Create 2 API's running on ports 6080 and 7080 with mesaages
    "Hello Node JS" and "Node JS installed successfully" respectively.
    Install pm2 tool and create 4 clusters of bothe Node's.
    Delete all 4 clusters one-by-one
```

> I installed nodejs on my CentOs 8 VM.

    sudo yum install nodejs (Reference Picture node_version.png)

    Similarly I installed npm using yum as well.

    sudo yum install npm (Reference Picture npm_version_check.png)

    Similarly install pm2 tool.

    sudo npm i -g pm2 

    Now we have successfully installed node , pm2 and npm.

    Let's create a api.js and api2.js file to host it in port 6080,7080

    ```
    //api.js
    var http = require('http');
    http.createServer(function(req,res){
                res.writeHead(200, { 'Content-Type': 'text/plain' });
                res.end('Hello Node Js');
    }).listen(6080);

    //api2.js
    var http = require('http');
    http.createServer(function(req,res){
                res.writeHead(200, { 'Content-Type': 'text/plain' });
                res.end('Node Js installed successfully');
    }).listen(7080);

    ```

    After that we run the instance using pm2. (Reference Picture running_multiple_node.png)
    # In dir /var/www/node_server

    pm2 start api.js

    We can pass -i flag to run the multiple cluster of the application as well.

    pm2 start api.js -i 4

    We can also pass -f flag to forcefully restart the server by adding cluster as well.

    As, Now We have ran multiple instances we can stop them by providing the id in pm2 (Reference Picture stopping_pm2_process.png):
    pm2 stop <id-of-cluster>




