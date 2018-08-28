---
swagger: "2.0"
x-collection-name: Google Doubleclick
x-complete: 0
info:
  title: Google Doubleclick API Get User Role Permission
  version: 1.0.0
  description: Gets one user role permission by ID.
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /userprofiles/{profileId}/accountPermissions:
    get:
      summary: Get Account Permissions
      description: Retrieves the list of account permissions.
      operationId: dfareporting.accountPermissions.list
      x-api-path-slug: userprofilesprofileidaccountpermissions-get
      parameters:
      - in: path
        name: profileId
        description: User profile ID associated with this request
      responses:
        200:
          description: OK
      tags:
      - Advertising
      - Permissions
  /userprofiles/{profileId}/accountPermissions/{id}:
    get:
      summary: Get Account Permissions
      description: Gets one account permission by ID.
      operationId: dfareporting.accountPermissions.get
      x-api-path-slug: userprofilesprofileidaccountpermissionsid-get
      parameters:
      - in: path
        name: id
        description: Account permission ID
      - in: path
        name: profileId
        description: User profile ID associated with this request
      responses:
        200:
          description: OK
      tags:
      - Advertising
      - Permissions
  /userprofiles/{profileId}/userRolePermissions:
    get:
      summary: Get User Role Permissions
      description: Gets a list of user role permissions, possibly filtered.
      operationId: dfareporting.userRolePermissions.list
      x-api-path-slug: userprofilesprofileiduserrolepermissions-get
      parameters:
      - in: query
        name: ids
        description: Select only user role permissions with these IDs
      - in: path
        name: profileId
        description: User profile ID associated with this request
      responses:
        200:
          description: OK
      tags:
      - Advertising
      - Users
      - Roles
      - Permissions
  /userprofiles/{profileId}/userRolePermissions/{id}:
    get:
      summary: Get User Role Permission
      description: Gets one user role permission by ID.
      operationId: dfareporting.userRolePermissions.get
      x-api-path-slug: userprofilesprofileiduserrolepermissionsid-get
      parameters:
      - in: path
        name: id
        description: User role permission ID
      - in: path
        name: profileId
        description: User profile ID associated with this request
      responses:
        200:
          description: OK
      tags:
      - Advertising
      - Users
      - Roles
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