---
swagger: "2.0"
x-collection-name: Facebook
x-complete: 0
info:
  title: Facebook Delete User Permissions
  description: De-authorizes an application or revokes a specific extended permissions
    on behalf of a user
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
x-streamrank:
  polling_total_time_average: 0
  polling_size_download_average: 0
  streaming_total_time_average: 0
  streaming_size_download_average: 0
  change_yes: 0
  change_no: 0
  time_percentage: 0
  size_percentage: 0
  change_percentage: 0
  last_run: ""
  days_run: 0
  minute_run: 0
---