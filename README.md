#


we hope we trust we want this to work 
In Money We Trust - Dan was here!



 REST API starter

This is a Python Flask REST API, serving a simple frontend for use in LBG programs

## Installation

To initialise the project you will need to install several dependencies, open up a git bash terminal from the repo directory and run the command:

~~~ bash
pip install -r requirements.txt
~~~

## Running the application

In order to run the application, from your git bash terminal run:

~~~ bash
python lbg.py
API Listening on http://localhost:8080/index.html
~~~

## Stopping the application

In order to stop the application from the git bash terminal that is running the server press ``CTRL`` + ``C``

## Functionality

### Through the browser

In order to interact with this application through a browser navigate to http://localhost:8080/index.html

There is a full CRUD functionality through the buttons on the web page.

### CREATE

To create the example product run the command:

~~~ bash
curl -s -X POST http://localhost:8080/create -H 'Content-type:application/json' -d '{"name":"example product", "description":"this is an example", "price":9.99}'
~~~

### READ (all)

To read all of the products run the command:

~~~ bash
curl -s -X GET http://localhost:8080/read
~~~

### READ (one)

To read one of the products run the command:

~~~ bash
curl -s -X GET http://localhost:8080/read/<id>
~~~

n.b: For these commands anything surrounded by angled braces <> needs to be replaced by you

### UPDATE

To update one of the products run the command:

~~~ bash
curl -s -X PUT http://localhost:8080/update/<id> -H 'Content-type:application/json'  -d '{"name":"updated product", "description":"its brand new", "price":99.99}'
~~~

n.b: For these commands anything surrounded by angled braces <> needs to be replaced by you

### DELETE

To delete one of the products run the command:

~~~ bash
curl -s -X DELETE http://localhost:8080/delete/<id>
~~~

n.b: For these commands anything surrounded by angled braces <> needs to be replaced by you

## Testing

To run unit/integration tests on this project, make sure the server is running.
In a new terminal window use the command

~~~ bash
python lbg.test.py
~~~

To run acceptance tests on this project, you must first download a webdriver for the browser of your choice and update the path in `.\features\environment.py`. Then make sure the server is running.
In a new terminal window use the command

~~~ bash
behave .\features\restapp.feature
~~~
