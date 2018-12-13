# golden-snippets

 use:

express and
morgan 

Install Node.js. and npm. npm is installed with Node.js

Placed inside the root project directory

`$ cd <your_angularjs_project>`
The next command creates package.json

`$ npm init`
Install express ==> Fast, unopinionated, minimalist for node:

`$ npm install express --save`
Install morgan ==> HTTP request logger middleware for node.js

`$ npm install morgan --save`
create file server.js`


add the following code in server.js file

// Required Modules
`var express    = require("express");
var morgan     = require("morgan");
var app        = express();`

var port = process.env.PORT || 3002;

app.use(morgan("dev"));
app.use(express.static("./"));

app.get("/", function(req, res) {
    res.sendFile("./index.html"); //index.html file of your angularjs application
});

// Start Server
app.listen(port, function () {
    console.log( "Express server listening on port " + port);
});
Finally run your AngularJS project in localhost server:

$ node server.js

		// const itemRemovedArray = $scope.csvHeaderList
		// 	.slice(0, index)
		// 	.concat($scope.csvHeaderList.slice(index + 1));

