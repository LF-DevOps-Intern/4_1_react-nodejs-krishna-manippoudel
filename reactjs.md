```
React JS
    Install React.js.
    Creating a React Application and print message "Hello React.js"
    Change the default port 3000 to 3001
```

> As we have already installed npm during node js installation. (Reference Picture npm_version_check.png)

    Let's install create-react-app package of React js to be able to initiate react project.

    npm install -g create-react-app

    After the create-react-app package is installed We can create the react app project using following command:

    create-react-app intern-devops (Reference Picture react-app-project-initilization.png)


    After the app has been created, We can create  a .env file in project root dir to change the port from 3000 to 3001.

    Now for starting the react app:

    npm start

    For changing the landing page output we edited the App.js in /src dir in project folder and added following line:

    ```

        import React from 'react';
        import './App.css';
        
        function App() {
            return ( 
            <h1> Hello World! </h1>
            );
        }
        
        export default App;
    ```

