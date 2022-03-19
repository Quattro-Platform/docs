# Authentication

## First party authentication
With this release, developers with direct contact with the company can use direct password authentication. No more authorisation needed! Just create your login page and start using the authentication api.

> {note} First party API keys can only be generated from the company. For third party authentication with tokens generated from the developer console go [here](#third-party-authentication)

### Authentication process

#### 1) Create a secure authentication page
Your application needs a secure login page that can send a POST request through HTTPS to the QuattroApp API.

#### 2) Exchange user credentials for a valid access token
Once the user has inserted the email and password combination you will send a POST request to /oauth/token to validate the user and retrieve an [access token](access-token).

> {note} User accounts can be disabled, be sure to catch this error and display an informative message to the user.

#### 3) Save the refresh token
As we issue short-term access rokens, you will need to refresh it via the refresh token that you've received with the authentication request.

#### 4) Send the access token with every request
In our API every request must be authenticated via header authentication: just send the access token with every request to enable authentication and authorization.

