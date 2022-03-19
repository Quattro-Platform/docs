# Access Token

### Basic structure
Our access token is a `100 chars long string`, unique per device and per user. When requesting a new access token, your app can pass an additional parameter `name` in order to let the user easily identify his tokens.

### Token lifetime
The access token is short-lived, it means that after the expiration date the token will stop working and your application will need to request a new token via a refresh token request.

### Scopes
At the moment token scopes are not supported as third-party authentication is not enabled. In future versions you 'll be able to retrieve tokens limited to specific scopes.