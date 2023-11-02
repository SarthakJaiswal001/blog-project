# blog-project
## My learnings in this project.

### What makes an API restful?
1. it uses the standard HTTP methods like get, post, put, patch, delete
2. it should have a standard data format with which it responds. Like JSON output, it should send JSON or XML to the client
3. the client side and server side should be completely separate, this allows both frontend and backend to scale
4. Stateless - each single request and response is complete, without the need to know what happened previously. Each request must contain all the information necessary to process the request, server shouldn't be storing any client-side data or state between the request. It simply means whenever the client side makes a request it contains all the information, for the server side to respond with correct data. This allows to handle multiple requests and servers.
5. Resource-based- Our API must be resource-based which means it must use a unique resource identifier/locator(URI/URL) to locate a resource.

### Different levels of API authentication:
1. no authentication - in this type of API request there is no authentication but we can set a rate limit or number of requests a particular IP address can make at a time. Public APIs have no authentication

2. basic authentication -  in this you provide a username and password when you make an api request, we are simply authenticating ourselves with the API provider. It is done using base64encoded string in the header of the request. username and password will be encoded in base64 and will be sended through authorization header exampple is when we create profile using post request and when we login it sends our base64encoded username and password through authorization header to verify and then it logins. base64 encoded data can be decoded easily thats why http module very useful because it encrypts the data in header using cryptography

3. api key authorization - in this we use a api key to authenticate the user 

4. token based authentication- in this once the user logins using username and password , then it generates a token to be used with the api, so the api doesnt gets involved with username, password instead its the token that is being used to interact with api , token based authentication is called OAuth and oauth 2.0 is industry standard. Like a third part weather app want to interact with google calendar, then we can use google oauth to connect both without username and password as well.

Axios is used to make API requests from our server to another through public API
In Axios when we get the data through API call we do not need to parse it using JSON.parse(), we can directly get the data by using .data 

## If there is something you would like to add then please create an issue. Happy coding

