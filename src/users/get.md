# Get a User

## Request
GET `/users/{user_id}`

## Response
### 200 OK
Payload: user object

Guilds are only returned if the authorized user is the same as the one fetching.

### 404 Not Found
Returned if the requested user cannot be found.
