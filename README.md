# Title

The limit is 50 characters and should be in the imperative, present tense (**«change»**, not **«changed»** or **«changes»**) to be consistent with generated messages from commands like git merge. When we write in the imperative, we tell someone what applying the commit will do.

**Tip**: Your subject should be able to complete the sentence: *If applied, this commit will **&lt;your subject line here&gt;**.*

## Challenge

1. Create an OpenAPI specification file in JSON format to define a basic API with a single endpoint. 
2. Commit this file with title.

### Resources

You can see an open api specs example below:

```json
{
  "openapi": "3.0.0",
  "info": {
    "title": "User API",
    "version": "1.0.0",
    "description": "An example OpenAPI Specification for a user-related API."
  },
  "paths": {
    "/user/{userId}": {
      "get": {
        "summary": "Get user information by ID",
        "parameters": [
          {
            "name": "userId",
            "in": "path",
            "required": true,
            "schema": {
              "type": "integer"
            },
            "description": "ID of the user to retrieve"
          }
        ],
        "responses": {
          "200": {
            "description": "Successful response",
            "content": {
              "application/json": {
                "example": {
                  "userId": 123,
                  "username": "john_doe",
                  "email": "john@example.com"
                }
              }
            }
          },
          "404": {
            "description": "User not found",
            "content": {
              "application/json": {
                "example": {
                  "error": "User not found"
                }
              }
            }
          }
        }
      }
    }
  }
}
```

In this example:

* The API has a single endpoint /user/{userId} that supports the HTTP GET method.
* The parameters section defines a path parameter userId of type integer.
* The responses section includes two possible responses: a successful response with HTTP status 200 and a not-found response with HTTP status 404.
* The JSON content of the successful response is specified in the example field, providing sample data for a user.

## Answer

[Click to see the answers.](ANSWERS.md)