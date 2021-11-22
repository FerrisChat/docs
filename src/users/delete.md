# Delete a User

**WARNING**: this action is immediate and irreversible.

This will NOT delete your messages. A different endpoint for that is coming soon.

## Request
DELETE `/users/{user_id}`

## Response
### 204 No Content

### 403 Forbidden
Returned if the authenticated user is not the same as the one this delete targets.

### 404 Not Found
Returned if the requested user cannot be found.
