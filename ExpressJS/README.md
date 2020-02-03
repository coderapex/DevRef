# ExpressJS DevRef

## Express Basics

### Setting Up Express

To install express, we use the `npm install express` command in the terminal. Using Express we set up an instance of our web app like this:

```javascript
// Express to run server and routes
const express = require("express");

// Start up an instance of app
const app = express();
```

### Connecting Additional Packages

Once we have created an instance of our app using Express, we can connect the other packages we have installed on the command line to our app in our code with the `.use()` method.

`app.use(packageName());`

### Creating Routes

```javascript
app.get("/all", sendData);

function sendData(request, response) {
  response.send(projectData);
}
```

You could also just pass a function in as the second parameter to `.get()` like this:

```javascript
app.get("/all", function(request, response) {
  response.send(projectData);
});
```

Or even with an arrow function like this:

```javascript
app.get("/all", (request, response) => {
  response.send(projectData);
});
```

## Popular Packages To Use With Express

### `body-parser` Package

Express version 4 and above require extra middle-ware layer to handle a POST request. This middle-ware is called as `bodyParser`. This used to be an internal part of Express framework, but now you have to install it separately.

```javascript
/* Connecting body-parser */
const bodyParser = require("body-parser");
/* Middleware*/
//Here we are configuring express to use body-parser as middle-ware.
app.use(bodyParser.urlencoded({ extended: false }));
app.use(bodyParser.json());
// Cors for cross origin allowance
const cors = require("cors");
app.use(cors());
```
