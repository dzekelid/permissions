swagger: "2.0"
x-collection-name: Facebook
x-complete: 1
info:
  title: Facebook
  version: 1.0.0
host: graph.facebook.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /{user}/permissions:
    get:
      summary: Get User Permissions
      description: The permissions that user has granted the application.
      operationId: getUserPermissions
      x-api-path-slug: userpermissions-get
      parameters:
      - in: path
        name: user
        description: Represents the ID of the user object
      responses:
        200:
          description: OK
      tags:
      - User
      - Permissions
    delete:
      summary: Delete User Permissions
      description: De-authorizes an application or revokes a specific extended permissions
        on behalf of a user
      operationId: deleteUserPermissions
      x-api-path-slug: userpermissions-delete
      parameters:
      - in: query
        name: permission
        description: The permission you wish to revoke
      - in: path
        name: user
        description: Represents the ID of the user object
      responses:
        200:
          description: OK
      tags:
      - User
      - Permissions