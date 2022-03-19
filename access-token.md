# Access Token

# First party applications
If your application is part of the first party apps that serve QuattroApp, then the authentication flow is simple.
Just send a request to /oauth/token with username and password paramenters, remember to include the secret token in every request your app send to our APIs.

# Third party applications
In this case you'll need to obtain an auth code from our internal authentication system. Just open the browser to the oauth/authorize endpoint and intercept the redirect response to optain the auth code, then you can excange the user auth code with a fresh access token.

