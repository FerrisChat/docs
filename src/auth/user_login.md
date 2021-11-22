# User Login
## Notes
* Currently, fetching a new token invalidates all previous tokens. This will change in the future.

## Request
POST `/auth`
### Headers
* Email: user's email
* Password: user's password

### Payload
none

## Response
### 200 OK
Payload: JSON object with one field named `token`.
```json
{
  "token": "MTA1NDc4Njk1NDUzODU2MjE4NzY3ODY5NDc2ODY0MA==.BVwW6vC4gw-B6MVJGqqaaGWIw1saNFvEOH7cSLbcmJb53lv-wv4mUHKlpy_c0PiJeXbR57dqMy77iv8a5VZd1g=="
}
```

### 400 Bad Request
Returned if any of the following happen:
* Either header is unset
* Either header contains invalid UTF-8

Payload: none

### 401 Unauthorized
Returned if user email matches but password does not.

Payload: none

### 404 Not Found
Returned if no email matches

Payload: none
