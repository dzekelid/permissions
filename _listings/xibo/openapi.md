swagger: "2.0"
x-collection-name: Xibo
x-complete: 1
info:
  title: Xibo API
  description: xibo-cms-api
  termsOfService: http://xibo.org.uk/legal
  version: 1.0.0
basePath: /api
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /user/permissions/{entity}/{objectId}:
    get:
      summary: Permission Data
      description: Permission data for the Entity and Object Provided.
      operationId: userPermissionsSearch
      x-api-path-slug: userpermissionsentityobjectid-get
      parameters:
      - in: path
        name: entity
        description: The Entity
      - in: path
        name: objectId
        description: The ID of the Object to return permissions for
      responses:
        200:
          description: OK
      tags:
      - Permission
      - Data
    post:
      summary: Permission Set
      description: Set Permissions to users/groups for the provided entity.
      operationId: userPermissionsSet
      x-api-path-slug: userpermissionsentityobjectid-post
      parameters:
      - in: path
        name: entity
        description: The Entity
      - in: formData
        name: groupIds
        description: Array of permissions with groupId as the key
      - in: path
        name: objectId
        description: The ID of the Object to set permissions on
      - in: formData
        name: ownerId
        description: Change the owner of this item
      responses:
        200:
          description: OK
      tags:
      - Permission
      - Set