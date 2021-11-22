# FerrisChat API Documentation

Welcome to the world of FerrisChat!

We're so glad that you decided to check out our API and possibly build something incredible!

### API Endpoints

The following endpoints may be used to connect:
```
https://ferris.chat/api/v0 (deprecated)
https://api.ferris.chat/v0
```

### Bugs

Bugs are bound to occur, so if you find one, please file it [here](https://github.com/FerrisChat/Server/issues/new?assignees=tazz4843&labels=bug&template=api_bug_report.yml&title=%5B500%5D%3A+).

### Bot Development Communities

Currently there are no established bot development communities, so check back here soon!

### Ping Endpoint

If you just wish to see if the API is online, either check [the status page](https://status.ferris.chat), or request `GET https://api.ferris.chat/v0/ping`. It will return a `200 OK` if online.

### Implicit Return Codes

All endpoints should be assumed to return HTTP 500 on error.
Nearly all HTTP 500 bodies contain JSON data structured as follows:

| Name | Type | Description |
| --- | --- | --- |
| reason | String | reason for the 500 |
| is_bug | bool | if this is a bug |
| link | Option\<String> | URL to report this at if this is a bug |

We cannot fix a 500 if you don't report it!
Make sure to add as much info as you can to your report that way
we can narrow it down as fast as possible.

### `u128` Return Types
128 bit unsigned integers are not available in some languages.
To help you work around this, every field of type `u128` also comes with a `string` variant.
For example: 
```json
{
  "id": 953168419309560759306499915776,
  "id_string": "953168419309560759306499915776"
}
```
If your language's JSON decoding implementation throws a fatal error upon finding a 128 bit integer,
you must find a different library to decode the JSON that does not throw a fatal error.
Otherwise, you can simply ignore the `id` field and only use `id_string`.