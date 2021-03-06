# GET /organizations/{name}/users
This operation retrieves the users associated with an organization within CAVE. The response contains the user information and their roles, in JSON format.

The operation can be executed only by users that are administrators or members of the organization.

### Resource URL

`https://api.cavellc.io/organizations/{name}/users`

### Resource Information

The request must be authenticated with a valid user token, as obtained from a login operation. See [POST /users/login](../users/login.md) for details. The token can be passed as the username (with an empty password) following the Basic Authentication scheme of the HTTP protocol. Alternatively, the same token can be accepted as a Bearer Token, similar to the OAuth2 specification.

### Example Request

    curl -i -u 8b896055-c295-4a30-a29c-5a97d15f1818: https://api.cavellc.io/organizations/acme/users


### Example Response

    HTTP/1.1 200 OK
    Content-Type: application/json; charset=utf-8
    Content-Length: 104
    Connection: keep-alive
    
    [
      {
        "user": {
          "first_name": "Joe",
          "last_name": "Appleseed",
          "email": "joe.appleseed@gmail.com"
        },
        "role": "admin"
      }
    ]
    
### See Also

* [Create organization](create-org.md)
* [Retrieve organization info](get-org.md)
* [Update organization](update-org.md)
* [Delete organization](delete-org.md)
* [Add user to organization](add-org-user.md)
* [Modify role for user in organization](modify-org-user.md)
* [Remove user from organization](remove-org-user.md)

[Back to Organizations](README.md)

[Back to API Main Page](../api.md)
