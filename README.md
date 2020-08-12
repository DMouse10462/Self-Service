[Self-Service.js](https://github.com/DMouse10462/Self-Service)
===============

> Node.js API for Youngstown State University's Self-Service Banner.

-----

## Fork Information

This is a fork of the Saint Mary's University repository to accomodate the pages at YSU. Much of the functionality is still broken, and features will generally only be implemented on an as-needed basis. All credentials-based methods are untested and probably broken. Contributions are welcome.

## Installation

```bash
npm install github:DMouse10462/Self-Service --save
```

## Usage - NOT TESTED

```javascript
//
var selfService = require("self-service-banner");

// Login Credentials for Authentication - UNIMPLEMENTED
var creds = {
   "username": "A-Number",
   "password": "123567890"
};

// Create your connection instance.
var s = new selfService;

// Authenticate your connection by logging in with your credentials. - UNIMPLEMENTED
s.login({"username": creds.username, "password": creds.password }, function(error, response, localService) {
    if (!error) {
      // Successful
      localService.weekAtAGlance({ /*'startDate': new Date()*/ }, function(error, response, courses) {
          if (!error) {
              // Successful
              console.log("Completed!", courses);
          } else {
              // An error occured
              throw error;
          }
      });

    } else {
        // An Error occured.
        throw error;
    }

});


```

-----

## For Contributors

1) Use Git to clone this repository.

2) Download all of your dependencies.

```bash
npm install
```

3) Create your credentials file: `./credentials.json`

```json
{
    "username": "A-Number",
    "password": "password"
}
```

4) Test your credentials by running the built-in Unit Tests.

```bash
npm test
```
