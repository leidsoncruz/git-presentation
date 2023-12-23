# Description (Optional)

The most important rule is WHY instead of HOW. Looking at the diff, we know how you made the changes. The important is the motivation for these changes. Make clear the reason that the change was needed. You can provide the previous behaviour to explain why was wrong.

Another rule is to wrap the body at 72 column characters.

## Challenge

[Previously](https://github.com/leidsoncruz/git-presentation/tree/exercise-1_title), you created the API specification file. Now, you will repeat the process and add a commit description.

1. Create an OpenAPI specification file in JSON format to define a basic API with a single endpoint. 
2. Commit this file with title and description.

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