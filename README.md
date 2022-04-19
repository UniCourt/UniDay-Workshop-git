# UniDay-Workshop-git

# 1. What is Curl?
cURL, which stands for client URL, is a command line tool that developers use to transfer data to and from a server. At the most fundamental, cURL lets you talk to a server by specifying the location (in the form of a URL) and the data you want to send. cURL supports several different protocols, including HTTP and HTTPS, and runs on almost every platform. This makes cURL ideal for testing communication from almost any device (as long as it has a command line and network connectivity) from a local server to most edge devices.

# 2. Sending API requests

We can use curl to send API requests. Each request is generally made up of four main parts:

- An endpoint, which is the address (URL) to which we are sending the request.
An HTTP method. The most common methods used are GET, POST, PUT and DELETE.

    * GET is used to retrieve a resource from a server. This could be a file, information, or an image.
    * POST is used to send information to the server.
    * PUT can be used to create or update a resource. This could be used to create or update a record in a database or update the contents of a file.
    * DELETE is used to delete a resource such as a database entry.

These actions for these methods are the recommended actions, but it's up to the API specification and implementation to define what exactly happens.

- Headers, which contain metadata about the request, such as content type, user agent, and so on.

- Body, which is the message body and contains the data that we want to send, if any. Generally, the body is used with POST and PUT methods.

curl command options

There are over two hundred curl options. You can see some of them by typing curl -h in a terminal. The most commonly used command options include these:

-I returns only the HTTPS headers

curl --request GET 'https://api.nasa.gov/planetary/apod?api_key=<myapikey>&date=2020-01-01' -I

4MQemyFDZYWhTNY4xGYPWbXnFzugCRC4YAe3VbnA
