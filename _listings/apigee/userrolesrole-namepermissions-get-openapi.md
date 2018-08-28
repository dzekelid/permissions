---
swagger: "2.0"
x-collection-name: Apigee
x-complete: 0
info:
  title: Apigee Edge Get Userroles Role Name Permissions
  description: Gets permission for a specific resource at global level.
  version: 1.0.0
host: api.enterprise.apigee.com
basePath: /v1/
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /organizations/{org_name}/userroles/{role_name}/permissions:
    get:
      summary: Get Organizations Name Userroles Role Name Permissions
      description: Gets a list of permissions associated with the specified resource
        for a single resource.
      operationId: getOrganizationsOrgNameUserrolesRoleNamePermissions
      x-api-path-slug: organizationsorg-nameuserrolesrole-namepermissions-get
      parameters:
      - in: query
        name: Content-Type
        description: Specify content type
      - in: path
        name: org_name
        description: Mention the organization name
      - in: query
        name: path
        description: Specify the resource path
      - in: path
        name: role_name
        description: Mention the role name
      responses:
        200:
          description: OK
      tags:
      - Organizations
      - Userroles
      - Role
      - Permissions
    post:
      summary: Post Organizations Name Userroles Role Name Permissions
      description: Associates permissions for a resource with a user role.
      operationId: postOrganizationsOrgNameUserrolesRoleNamePermissions
      x-api-path-slug: organizationsorg-nameuserrolesrole-namepermissions-post
      parameters:
      - in: query
        name: Content-Type
        description: Specify the content type
      - in: path
        name: org_name
        description: Mention the organization name
      - in: path
        name: role_name
        description: Mention the role name
      responses:
        200:
          description: OK
      tags:
      - Organizations
      - Userroles
      - Role
      - Permissions
  /organizations/{org_name}/userroles/{role_name}/permissions/get:
    get:
      summary: Get Organizations Name Userroles Role Name Permissions Get
      description: Checks the particular userrole permission of a resource at organization
        level.
      operationId: getOrganizationsOrgNameUserrolesRoleNamePermissionsGet
      x-api-path-slug: organizationsorg-nameuserrolesrole-namepermissionsget-get
      parameters:
      - in: query
        name: Content-Type
        description: Specify content type
      - in: path
        name: org_name
        description: Mention the organization name
      - in: query
        name: path
        description: Specify the resource path
      - in: path
        name: role_name
        description: Mention the role name
      responses:
        200:
          description: OK
      tags:
      - Organizations
      - Userroles
      - Role
      - Permissions
      - Get
    delete:
      summary: Delete Organizations Name Userroles Role Name Permissions Get
      description: Deletes particular userrole permission at organization level.
      operationId: deleteOrganizationsOrgNameUserrolesRoleNamePermissionsGet
      x-api-path-slug: organizationsorg-nameuserrolesrole-namepermissionsget-delete
      parameters:
      - in: query
        name: Content-Type
        description: Specify content type
      - in: path
        name: org_name
        description: Mention the organization name
      - in: query
        name: path
        description: Specify the resource path
      - in: path
        name: role_name
        description: Mention the role name
      responses:
        200:
          description: OK
      tags:
      - Organizations
      - Userroles
      - Role
      - Permissions
      - Get
  /userroles/{role_name}/permissions:
    get:
      summary: Get Userroles Role Name Permissions
      description: Gets permission for a specific resource at global level.
      operationId: getUserrolesRoleNamePermissions
      x-api-path-slug: userrolesrole-namepermissions-get
      parameters:
      - in: query
        name: Content-Type
        description: Specify Content Type
      - in: query
        name: path
        description: Specify the resource path
      - in: path
        name: role_name
        description: Mention the role name
      responses:
        200:
          description: OK
      tags:
      - Userroles
      - Role
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