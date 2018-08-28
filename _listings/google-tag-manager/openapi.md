swagger: "2.0"
x-collection-name: Google Tag Manager
x-complete: 1
info:
  title: Tag Manager
  description: accesses-tag-manager-accounts-and-containers-
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