# Backend styles

Http Status Codes
--------------

Status codes for common escenarious:

* General:
	- `424 Failed Dependency`: If the social access token is for a valid user but the user doesn't exist on the db.
	- `401 Unauthorized`: If the social access token is invalid (checked with facebook or google sdk).
	- `200 ok`: If the user exists in the db, should return the session token.
	- `403 Forbidden`: The user might be authenticated but does not have the necessary permissions to
	- `412 Precondition Failed`: The server doesn't meet the preconditions to process the request (i.e. invalid state or validation)

* Force update:
	- `426`: If the user have an app version that should be updated.    

Naming Convention
------------------

* Variables: lower case with - as divider like: `first-name`.

Errors
--------------

All errors from backend should have in body:

```
{
  "errors": {
    "field1": "message1",
    "field2": "message2"
  }
}
```
