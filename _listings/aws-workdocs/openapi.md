---
swagger: "2.0"
x-collection-name: AWS WorkDocs
x-complete: 1
info:
  title: AWS WorkDocs API
  version: 1.0.0
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /?Action=AddResourcePermissions:
    get:
      summary: Add Resource Permissions
      description: Creates a set of permissions for the specified folder or document.
      operationId: addResourcePermissions
      x-api-path-slug: actionaddresourcepermissions-get
      parameters:
      - in: query
        name: ResourceId
        description: The ID of the resource
        type: string
      responses:
        200:
          description: OK
      tags:
      - Permissions
  /?Action=DescribeResourcePermissions:
    get:
      summary: Describe Resource Permissions
      description: Describes the permissions of a specified resource.
      operationId: describeResourcePermissions
      x-api-path-slug: actiondescriberesourcepermissions-get
      parameters:
      - in: query
        name: ResourceId
        description: The ID of the resource
        type: string
      responses:
        200:
          description: OK
      tags:
      - Permissions
  /?Action=RemoveAllResourcePermissions:
    get:
      summary: Remove All Resource Permissions
      description: Removes all the permissions from the specified resource.
      operationId: removeAllResourcePermissions
      x-api-path-slug: actionremoveallresourcepermissions-get
      parameters:
      - in: query
        name: ResourceId
        description: The ID of the resource
        type: string
      responses:
        200:
          description: OK
      tags:
      - Permissions
  /?Action=RemoveResourcePermission:
    get:
      summary: Remove Resource Permission
      description: Removes the permission for the specified principal from the specified
        resource.
      operationId: removeResourcePermission
      x-api-path-slug: actionremoveresourcepermission-get
      parameters:
      - in: query
        name: PrincipalId
        description: The principal ID of the resource
        type: string
      - in: query
        name: PrincipalType
        description: The principal type of the resource
        type: string
      - in: query
        name: ResourceId
        description: The ID of the resource
        type: string
      responses:
        200:
          description: OK
      tags:
      - Permissions
---