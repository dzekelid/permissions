---
swagger: "2.0"
x-collection-name: Google Tag Manager
x-complete: 0
info:
  title: Google Tag Manager API Update User
  description: Updates a user's Account & Container Permissions.
  contact:
    name: Google
    url: https://google.com
  version: v1
host: www.googleapis.com
basePath: /tagmanager/v1
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /accounts/{accountId}/permissions:
    get:
      summary: Get User Permissions
      description: List all users that have access to the account along with Account
        and Container Permissions granted to each of them.
      operationId: tagmanager.accounts.permissions.list
      x-api-path-slug: accountsaccountidpermissions-get
      parameters:
      - in: path
        name: accountId
        description: The GTM Account ID
      responses:
        200:
          description: OK
      tags:
      - User Permission
    post:
      summary: Create User Permission
      description: Creates a user's Account & Container Permissions.
      operationId: tagmanager.accounts.permissions.create
      x-api-path-slug: accountsaccountidpermissions-post
      parameters:
      - in: path
        name: accountId
        description: The GTM Account ID
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - User Permission
  /accounts/{accountId}/permissions/{permissionId}:
    get:
      summary: Get User
      description: Gets a user's Account & Container Permissions.
      operationId: tagmanager.accounts.permissions.get
      x-api-path-slug: accountsaccountidpermissionspermissionid-get
      parameters:
      - in: path
        name: accountId
        description: The GTM Account ID
      - in: path
        name: permissionId
        description: The GTM User ID
      responses:
        200:
          description: OK
      tags:
      - User
    put:
      summary: Update User
      description: Updates a user's Account & Container Permissions.
      operationId: tagmanager.accounts.permissions.update
      x-api-path-slug: accountsaccountidpermissionspermissionid-put
      parameters:
      - in: path
        name: accountId
        description: The GTM Account ID
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: permissionId
        description: The GTM User ID
      responses:
        200:
          description: OK
      tags:
      - User
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