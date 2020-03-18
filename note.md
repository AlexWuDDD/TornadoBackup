# Note

1. Tornado suports any valid HTTP method(GET, POST, DELETE, HEAD, OPTIONS)
2. 我们可以在回调函数里挨个定义

## 404 Not Found

Tornado wiil automatically return a 404(Not Found)response code if the path of the HTTP request doesn't match ant pattern associated with a **RequestHandler** class

## 400 Bad Request

If you call get_argument without a default, and no argument with the given name is found, Tornado will automatically return a 400(Bad REquest) response code.

## 405 Method Not Allowed

If an incoming request uses an HTTP method that the matching **RequestHandler** doesn't define (e.g. the request is POST but the handler class only defines a get method), Tornado will return a 405(Method Not Allowed)response code

## 500 Internal Server Error

Tornado will return 500(Internal Server Error)when it encounters any errors that aren't severe enough to cause the program to exit. Any uncaught exceptions in your code will also cause Tornado to return a 500 response code.

## 200 OK

If the response was successful and no other status code was set, Tornado will return a 200(OK) response code by default.
