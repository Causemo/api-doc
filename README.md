Causemo API
====================
WORK IN PROGRESS

Authentication
--------------
Causemo authentication server is an oauth2 server which requires every API request to include an authentication token in the header. This ensures the request is coming from a trusted source. How do you integrate with Causemo authentication service, read the [authentication guide](https://github.com/Causemo/api-doc/blob/master/sections/authentication.md) to get started.

API
--------------
Causemo API is divided into multiple parts. This relates to the scope of the authentication token provided by the Causemo authentication server. In order to access a particular part of the API, your token must have it as part of its scope.
- [SDK API Guide](https://github.com/Causemo/api-doc/blob/master/sections/api/1/sdk/README.md) 
- [Web API Guide](https://github.com/Causemo/api-doc/blob/master/sections/api/1/web/README.md) 
- [App API Guide](https://github.com/Causemo/api-doc/blob/master/sections/api/1/app/README.md) 
