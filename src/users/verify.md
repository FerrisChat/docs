# Verify a User's Email

# Part 1
This sends an email to the email linked to the user's account.

## Request
POST `/verify`

## Response
### 200 OK
Payload: JSON object with one field: `message`

### 304 Not Modified
Returned if the user is already verified.

### 409 Conflict
Returned if any of the following are true:
* This user is already verified.

# Part 2
Clicking the link in the email sent to the user brings them here.

## Request
No `Authorization` header needed.

GET `/verify/{token}`

## Response
### 200 OK
Payload: JSON object with one field: `message`

### 404 Not Found
Returned if the token is not found. Note tokens expire after 1 hour.
