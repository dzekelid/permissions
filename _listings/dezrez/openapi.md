swagger: "2.0"
x-collection-name: Dezrez
x-complete: 1
info:
  title: Dezrez.Rezi.Client.Api
  version: 1.0.0
host: api.dezrez.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /api/teamsecurity/permissionsforgroup:
    get:
      summary: This returns security permissions that a group has on other groups
      description: This returns security permissions that a group has on other groups.
      operationId: TeamGroupSecurity_GetSecurityPermissionsForGroupByteamId
      x-api-path-slug: apiteamsecuritypermissionsforgroup-get
      parameters:
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      - in: query
        name: teamId
        description: The id of the group to find permissions for
      responses:
        200:
          description: OK
      tags:
      - This
      - Returns
      - Security
      - Permissions
      - That
      - Group
      - Has
      - "On"
      - Other
      - Groups
  /api/teamsecurity/permissionsongroup:
    get:
      summary: This returns security permissions that other groups have on specified
        group
      description: This returns security permissions that other groups have on specified
        group.
      operationId: TeamGroupSecurity_GetSecurityPermissionsThatApplyToGroupByteamId
      x-api-path-slug: apiteamsecuritypermissionsongroup-get
      parameters:
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      - in: query
        name: teamId
        description: The id of the group to find other groups permissions
      responses:
        200:
          description: OK
      tags:
      - This
      - Returns
      - Security
      - Permissions
      - That
      - Other
      - Groups
      - Have
      - "On"
      - Specified
      - Group
  /api/teamsecurity/savepermission:
    post:
      summary: Save a new security permission for a group
      description: Save a new security permission for a group.
      operationId: TeamGroupSecurity_SavePermissionBydataContract
      x-api-path-slug: apiteamsecuritysavepermission-post
      parameters:
      - in: body
        name: dataContract
        schema:
          $ref: '#/definitions/holder'
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Save
      - New
      - Security
      - Permissiona
      - Group