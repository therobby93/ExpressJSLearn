# Learning fundamentals of Express JS
My journey with Express. 
* Express provides a minimal interface to build our applications. 
* It provides us the tools that are required to build our app. 
* It is flexible as there are numerous modules available on npm, which can be directly plugged into Express.

## Routing
 *Defining routes like above is very tedious to maintain.
 To separate the routes from our main index.js file, we will use Express.Router. 
 Create a new file called things.js and type the following in it.
 ```
 var express = require('express');
var router = express.Router();

router.get('/', function(req, res){
   res.send('GET route on things.');
});
router.post('/', function(req, res){
   res.send('POST route on things.');
});

//export this router to use in our index.js
module.exports = router;
 ```
 

## HTTP Methods
*1	
GET: The GET method requests a representation of the specified resource. 
Requests using GET should only retrieve data and should have no other effect.

*2	
POST:The POST method requests that the server accept the data enclosed in the request as a 
new object/entity of the resource identified by the URI.

*3	
PUT: The PUT method requests that the server accept the data enclosed in the request as a
modification to existing object identified by the URI. If it does not exist then the PUT method should create one.

*4	
DELETE: The DELETE method requests that the server delete the specified resource.

## Middleware

*Middleware functions are functions that have access to the request object (req), the response object (res), and the next middleware function in the application’s request-response cycle. These functions are used to modify req and res objects for tasks like parsing request bodies, adding response headers, etc.

```
Examples:
----------
var express = require('express');
var app = express();

//Simple request time logger
app.use(function(req, res, next){
   console.log("A new request received at " + Date.now());
   
   //This function call is very important. It tells that more processing is
   //required for the current request and is in the next middleware
   function/route handler.
   next();
});

app.listen(3000);
```

## Serving static files
* Static files are files that clients download as they are from the server. 
* Create a new directory, public. Express, by default does not allow you to serve static files. 
* You need to enable it using the following built-in middleware.

```
<div ng-app = "" ng-controller = "studentController">
   ...
</div>
```

And repeat

```
until finished
```

End with an example of getting some data out of the system or using it for a little demo

## Modules

* Modules are used to separate logics say services, controllers, application etc. and keep the code clean.
* 

### Break down into end to end tests

Explain what these tests test and why

```
Give an example
```

### Other topics that I learned

Forms. ajax, includes,scopes, services, filters and etc

```
In Views:
$routeProvider is the key service which set the configuration of urls, 
map them with the corresponding html page or ng-template, and attach a controller with the same.

```
# Bottom is reference for me 
# Learning how to format the README file

## Deployment

Add additional notes about how to deploy this on a live system

## Built With

* [Dropwizard](http://www.dropwizard.io/1.0.2/docs/) - The web framework used
* [Maven](https://maven.apache.org/) - Dependency Management
* [ROME](https://rometools.github.io/rome/) - Used to generate RSS Feeds

## Contributing

Please read [CONTRIBUTING.md](https://gist.github.com/PurpleBooth/b24679402957c63ec426) for details on our code of conduct, and the process for submitting pull requests to us.

## Versioning

We use [SemVer](http://semver.org/) for versioning. For the versions available, see the [tags on this repository](https://github.com/your/project/tags). 

## Authors

* **Robby Sanchez** - *Initial work* - [PurpleBooth](https://github.com/)

See also the list of [contributors](https://github.com/your/project/contributors) who participated in this project.

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

## Acknowledgments

* Hat tip to anyone who's code was used
* Inspiration
* etc
